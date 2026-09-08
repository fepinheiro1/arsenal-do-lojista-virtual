# Título que Rankeia — exemplos reais

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
Como a skill age: preserva os fatos, remove o subjetivo, tira a repetição e reordena com marca/modelo na frente.

Saída:
```
Título recomendado:
Nike Pegasus 42 Tênis de Corrida Masculino Preto
48 caracteres

Ajustes: removidos "confortável" e "original" (subjetivos, não ajudam na busca);
a numeração (tam. 42) sai do título principal — tamanho é variante que a pessoa
seleciona na página, não parte do nome.
```

## Exemplo C — Multicanal (sob pedido)
Entrada:
```
Me dá os títulos para loja e Google Shopping:
Nike Pegasus 42, tênis de corrida masculino, preto, malha, tam 42
```
Saída:
```
Loja / H1:
Nike Pegasus 42 Tênis de Corrida Masculino Preto            (48 caracteres)

SEO title:
Nike Pegasus 42 Tênis de Corrida Masculino Preto | Minha Loja   (61 caracteres)

Google Merchant:
Nike Pegasus 42 Tênis de Corrida Masculino Preto em Malha       (57/150 caracteres)

Short title:
Nike Pegasus 42 Masculino                                   (25 caracteres)
```
Repare: o Merchant carrega mais atributo (malha) nos primeiros ~70; o short title fica enxuto para formatos visuais.

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
```

> Referência: um título recomendado por vez (a skill assume a escolha), o essencial
> cedo, cada canal com sua lógica, e zero termo inventado, repetido ou subjetivo.
