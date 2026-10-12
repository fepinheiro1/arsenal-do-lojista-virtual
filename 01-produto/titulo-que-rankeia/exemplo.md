# Título que Rankeia — exemplos ilustrativos

> Casos de demonstração: todo atributo do título vem da entrada; o que é ambíguo vira pergunta.

## Exemplo A — Entrada mínima (criar)
Entrada:
```
Cafeteira BrewCo Classic
moka
6 xícaras
alumínio
```
Como a skill age: infere a categoria e a palavra-chave sem perguntar; marca fraca, então o tipo lidera.

Saída:
```
Título recomendado:
Cafeteira Italiana Moka BrewCo Classic 6 Xícaras Alumínio
57 caracteres
```

## Exemplo B — Otimizar (título poluído)
Entrada:
```
Melhore:
Tênis Masculino Nike Preto Pegasus Corrida Confortável Original 42
```
Como a skill age: preserva os fatos, remove o subjetivo e reordena com marca/modelo na frente. Mas o "42" solto no fim é ambíguo — pode ser o modelo (Pegasus 42) ou a numeração — e isso muda o título. Em vez de escolher em silêncio, pergunta e já entrega as duas versões.

Saída:
```
Uma confirmação antes de fechar: o "42" no fim é o modelo (Pegasus 42) ou a numeração?

Se for o modelo:
Nike Pegasus 42 Tênis de Corrida Masculino Preto
48 caracteres

Se for a numeração:
Nike Pegasus Tênis de Corrida Masculino Preto
45 caracteres
(o tamanho sai do título principal — é variante que a pessoa escolhe na página)

Nos dois casos: removidos "confortável" e "original" — são opinião, não identificam
o produto.
```

## Exemplo C — Multicanal (sob pedido)
Entrada:
```
Me dá os títulos para loja e Google Shopping:
Nike Pegasus 42, tênis de corrida masculino, preto, malha, tam 42
```
Como a skill age: aqui a entrada separa as duas coisas — "Pegasus 42" é o modelo e "tam 42" é a numeração —, então o 42 do modelo fica e o tamanho é tratado como variante.

Saída:
```
Loja / H1:
Nike Pegasus 42 Tênis de Corrida Masculino Preto            (48 caracteres)

SEO title:
Nike Pegasus 42 Tênis de Corrida Masculino Preto            (48 caracteres)
(se quiser o nome da loja no fim, ele entra depois de " | " — me diga qual é)

Google Merchant (item da numeração 42):
Nike Pegasus 42 Tênis de Corrida Masculino Preto em Malha Tam. 42   (65/150 caracteres)

Short title:
Nike Pegasus 42 Masculino                                   (25 caracteres)
```
Repare: o Merchant carrega mais atributo (malha) nos primeiros ~70 e, como cada numeração é um item do feed, o tamanho distingue a variante (e vai também no atributo `size`); o short title fica enxuto para formatos visuais. Limites e regras do Merchant: conferir a especificação vigente.

## Exemplo D — Catálogo (modo em lote)
Entrada:
```
Padronize:
SKU1 | Camiseta Nike Dri-Fit Masculina Preta
SKU2 | Adidas Camiseta Branca Homem
SKU3 | T-Shirt Puma Azul Masculina
```
Como a skill age: detecta a inconsistência (ordem e termos diferentes), fixa um padrão de categoria e aplica, preservando marca e cor reais.

Saída:
```
Padrão aplicado (moda): Tipo + Marca + Linha + Gênero + Cor

SKU  | Título recomendado                      | Alerta
SKU1 | Camiseta Nike Dri-Fit Masculina Preta   | —
SKU2 | Camiseta Adidas Masculina Branca        | "Homem" → "Masculina" (padronizado)
SKU3 | Camiseta Puma Masculina Azul            | "T-Shirt" → "Camiseta" (padronizado)

Conferência: 3 SKUs recebidos, 3 entregues, na mesma ordem; nenhum título duplicado.
"Dri-Fit" ficou só no SKU1 — é da Nike e não vale para os outros.
```

> Referência: um título recomendado por vez (a skill assume a escolha), o essencial
> cedo, cada canal com sua lógica, número ambíguo vira pergunta, lote conferido item a
> item, e zero termo inventado, repetido ou subjetivo.
