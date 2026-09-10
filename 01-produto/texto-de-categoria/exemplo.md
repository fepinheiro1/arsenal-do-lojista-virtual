# Texto de Categoria — exemplos reais

## Exemplo A — PLP com orientação (sem parede de texto)
Entrada:
```
Categoria: Cafeteiras
Sortimento: elétricas, italianas (moka), prensa francesa, de cápsula; R$ 80 a R$ 900
Filtros reais: tipo de preparo, capacidade (xícaras), com/sem timer
```
Como a skill age: PLP com variedade real → intro curta + um "como escolher" pelos atributos que existem, mantendo o texto leve para não empurrar o grid para baixo.

Saída:
```
## Cafeteiras
Da italiana clássica à de cápsula: aqui você escolhe pelo tipo de café que quer
fazer em casa e pelo tamanho que atende o seu dia.

### Como escolher
- Quer praticidade no dia a dia? Cafeteira elétrica ou de cápsula.
- Gosta do café encorpado tradicional? Cafeteira italiana (moka).
- Prefere controlar a extração? Prensa francesa.
- Faz café para a família? Veja a capacidade em xícaras no filtro ao lado.

[Grid de produtos entra aqui]

Ver também: [Cápsulas e filtros] · [Xícaras e canecas]
```
(Os links são sugestões de destino — troque pelas URLs reais das suas subcategorias.)

## Exemplo B — Vale a pena ter texto? (comportamento adaptativo)
Entrada:
```
Página: filtro "Cafeteiras > cor preta > ordenar por menor preço"
```
Como a skill age: isso é um estado de filtro/ordenação, não uma categoria com intenção própria. A skill recomenda NÃO criar texto e levanta o alerta técnico.

Saída:
```
Recomendação: não criar texto para esta página.

"Cor preta + ordenar por menor preço" é um estado de filtro, não uma categoria com
intenção de busca própria — texto aqui vira filler e ainda arrisca criar uma página
que concorre com a categoria principal "Cafeteiras".

Alerta técnico (para quem cuida do SEO): combinações de filtro + ordenação costumam
gerar muitas URLs parecidas; vale revisar se essas páginas devem ser indexáveis.
Se existir uma intenção real e recorrente (ex.: "cafeteira italiana pequena"), aí sim
pode valer uma landing própria — me diga que eu ajudo a montar.
```

## Exemplo C — Otimizar template genérico (sem inventar)
Entrada:
```
Melhore este texto da categoria Tênis de Corrida:
"Aqui você encontra os melhores tênis de corrida com os melhores preços. Compre já
o seu tênis de corrida na nossa loja de tênis de corrida!"
```
Como a skill age: remove o template e a repetição, troca por orientação real — e não inventa tipo de pisada (neutra/pronada), que não foi informado.

Saída:
```
## Tênis de corrida
Modelos para diferentes ritmos e terrenos. A escolha certa depende de onde e de
quanto você corre.

### Como escolher
- Corre no asfalto, no dia a dia? Priorize amortecimento.
- Treina em trilha? Procure solado com mais aderência.
- Foca em provas rápidas? Modelos mais leves ajudam.

Use os filtros de terreno e amortecimento ao lado para reduzir as opções.

—
Removido: "melhores tênis / melhores preços / loja de tênis de corrida" (repetição
sem informação). Se você me passar a indicação de pisada oficial dos modelos, incluo
esse critério — sem isso, não afirmo tipo de pisada.
```

> Referência: a skill entrega só o que ajuda a escolher, ancora no sortimento real,
> não força tamanho nem inventa atributo — e às vezes recomenda não ter texto.
