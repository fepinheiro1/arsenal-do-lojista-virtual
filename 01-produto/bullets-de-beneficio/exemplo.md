# Bullets de Benefício — exemplos reais

## Exemplo A — Criar (sem inventar)
Entrada:
```
Produto: Tênis de corrida
Características:
- mesh respirável
- 268 g
- solado em borracha
```
Como a skill age: cria só com o que foi dado; usa claims proporcionais (mesh → ventilação, não "elimina suor") e não inventa amortecimento, garantia ou tecnologia.

Saída:
```
• Mais ventilação durante o treino — cabedal em mesh respirável.
• Mais leveza nas passadas — apenas 268 g no tamanho informado.
• Mais aderência no uso urbano — solado em borracha.
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
mesh + espuma EVA", vira:
• Mais ventilação no uso — cabedal em mesh respirável.
```

## Exemplo C — Bullet que mata objeção (usando a FAQ)
Entrada:
```
Produto: Cafeteira italiana
Característica: compatível com indução
Pergunta frequente no anúncio: funciona em fogão por indução?
```
Como a skill age: uma dúvida que trava a compra vira o bullet de maior prioridade.

Saída:
```
• Funciona no seu fogão por indução — base preparada para esse tipo de aquecimento.
• Café pronto em poucos minutos — formato moka italiano clássico.
```

## Exemplo D — Google Merchant (product_highlight)
Entrada:
```
Formato Google Merchant highlights:
Notebook 14", Ryzen 7, 16 GB RAM, SSD 1 TB
```
Como a skill age: entrega destaques factuais e escaneáveis para o feed — sem preço, promoção, frete ou nome da loja.

Saída:
```
product_highlight:
- Roda vários programas ao mesmo tempo com 16 GB de RAM
- Sistema e arquivos abrem em segundos com SSD de 1 TB
- 1 TB de espaço para arquivos, fotos e projetos
- Tela de 14" num corpo leve para levar para qualquer lugar
```

> Referência: só argumentos que ajudam a decidir, claim proporcional à prova, um
> benefício por bullet, e o que falta vira pedido — nunca invenção.
