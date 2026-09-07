# Estrutura de Campanha e Grupos de Anúncios — exemplo real

## Entrada
```
Catálogo: loja de calçados esportivos. Categorias: tênis de corrida,
  tênis casual, chuteiras. Carro-chefe: tênis de corrida NimbusFlow X1.
Objetivo: vender tênis de corrida (categoria de maior margem)
Orçamento aproximado: R$ 60/dia
Marca: PisoLeve
Termos que trazem prejuízo: "grátis", "usado", "conserto de tênis"
```

## Saída
```
CAMPANHA 1 — Marca (PisoLeve)
  Grupo: Marca exata
    Intenção: marca
    Palavras-chave: variações do nome "PisoLeve"
    Ângulo do anúncio: reforçar que é a loja oficial, frete e condições reais

CAMPANHA 2 — Tênis de Corrida (genérica/comercial) — PRIORIDADE
  Grupo: Corrida masculino
    Intenção: comercial
    Palavras-chave: "tênis de corrida masculino" e variações de gênero
    Ângulo: amortecimento e leveza para o corredor amador
  Grupo: Corrida feminino
    Intenção: comercial
    Palavras-chave: "tênis de corrida feminino" e variações
    Ângulo: mesmo benefício, linguagem para o público feminino
  Grupo: Amortecimento / longa distância
    Intenção: comercial
    Palavras-chave: "tênis com amortecimento", "tênis para maratona"
    Ângulo: estabilidade do 1º ao último quilômetro

CAMPANHA 3 — Produto NimbusFlow X1 (carro-chefe)
  Grupo: NimbusFlow X1
    Intenção: comercial de produto
    Palavras-chave: "nimbusflow x1", "tênis nimbusflow"
    Ângulo: modelo específico, diferenciais e prova social [preencher]

Palavras negativas entre campanhas
- Nas campanhas 2 e 3, negativar "pisoleve" para não competir com a Campanha de Marca (clique mais caro à toa).
- Em todas: "grátis", "usado", "conserto de tênis" (termos que trazem prejuízo).
- Na campanha 2, negativar "casual" e "chuteira" para não invadir outra categoria.

Ordem de prioridade
1. Campanha 2 (Tênis de Corrida) — é o objetivo declarado e a maior margem. Começa aqui.
2. Campanha 1 (Marca) — barata, protege o topo; ligar logo em seguida.
3. Campanha 3 (Produto) — abrir depois, quando houver dado de qual modelo converte melhor.

Com R$ 60/dia, comece só pela Campanha 2 e pela de Marca. Abra a 3 quando o orçamento sobrar — conta espalhada demais aprende devagar.
```

> Referência: separa por intenção (marca, comercial, produto), cada grupo tem tema fechado que pede um único conjunto de títulos, deixa explícito onde entram as negativas entre campanhas, e a recomendação de orçamento é honesta — mandou concentrar em vez de pulverizar. O dado que faltava (prova social do produto) virou `[preencher]`, não foi inventado.
