# Bullets de Benefício — exemplos ilustrativos

> Casos de demonstração: cada bullet sai da entrada — o que não veio vira pedido, não bullet.

## Exemplo A — Criar (sem inventar)
Entrada:
```
Produto: Tênis de corrida
Características:
- mesh respirável
- 268 g
- solado em borracha
```
Como a skill age: cria só com o que foi dado e com claim proporcional (mesh respirável → favorece a ventilação, não "elimina suor"). "268 g" não vira "leve": peso de tênis muda com a numeração e a entrada não diz qual foi medida — então o peso vai para a ficha e vira pergunta. Dois bullets bons valem mais que três com um inventado.

Saída:
```
• Favorece a ventilação no treino — cabedal em mesh respirável.
• Aderência no piso — solado em borracha.

Specs para a ficha técnica:
- Peso: 268 g

Para ganhar mais bullets, me diga:
- em qual numeração os 268 g foram medidos (aí o peso vira argumento com base);
- entressola/amortecimento e para qual piso o tênis é indicado, se você tiver.
```

## Exemplo B — Otimizar (bullets genéricos)
Entrada:
```
Melhore estes bullets:
- Alta qualidade
- Muito confortável
- Design moderno
```
Como a skill age: reconhece que são vazios (sem especificidade nem prova) e não finge sustentá-los. Pede o mínimo para transformá-los em algo real.

Saída:
```
Esses três não se sustentam sozinhos — "alta qualidade", "confortável" e "design
moderno" não dizem por que a pessoa deve comprar, nem têm prova.

Me passe 2 ou 3 características concretas (material, peso, tecnologia, medidas) e eu
transformo em bullets que realmente ajudam a decidir. Por exemplo, com "cabedal em
mesh respirável + entressola em EVA", vira:
• Favorece a ventilação no uso — cabedal em mesh respirável.
```

## Exemplo C — Bullet que mata objeção (usando a FAQ)
Entrada:
```
Produto: Cafeteira italiana
Característica: compatível com indução
Pergunta frequente no anúncio: funciona em fogão por indução?
```
Como a skill age: uma dúvida que trava a compra vira o bullet de maior prioridade. Não acrescenta "café pronto em poucos minutos": tempo de preparo não veio na entrada.

Saída:
```
• Funciona no seu fogão por indução — base compatível com indução.

Para mais bullets, me passe: capacidade (xícaras), material do corpo e se pode ir à
lava-louças.
```

## Exemplo D — Google Merchant (product_highlight)
Entrada:
```
Formato Google Merchant highlights:
Notebook 14", Ryzen 7, 16 GB RAM, SSD 1 TB
```
Como a skill age: entrega destaques factuais e escaneáveis para o feed — sem preço, promoção, frete ou nome da loja. Não promete tempo ("abre em segundos") sem teste, nem "corpo leve" sem o peso, e não repete o SSD em dois destaques.

Saída:
```
product_highlight:
- Tela de 14 polegadas
- Processador Ryzen 7
- 16 GB de RAM para trabalhar com vários programas abertos
- SSD de 1 TB: espaço para sistema, arquivos, fotos e projetos
```
Peso, autonomia de bateria e a geração do processador deixariam os destaques mais
úteis — não entraram porque não vieram. (Limites do Merchant: conferir a regra vigente.)

> Referência: só argumentos que ajudam a decidir, claim proporcional à prova, um
> benefício por bullet, menos bullets quando a entrada é curta, e o que falta vira
> pedido — nunca invenção (nada de "leve", "rápido" ou "em segundos" sem dado).
