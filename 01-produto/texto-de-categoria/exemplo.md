# Texto de Categoria — exemplos ilustrativos

> Casos de demonstração: o texto só cita sortimento, filtro e link que vieram na entrada — o resto vira pergunta.

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
- Faz café para a família? Use o filtro de capacidade (em xícaras).

[Grid de produtos entra aqui]
```
Links internos sugeridos — só se essas páginas existirem na sua loja (me passe as
URLs e eu monto o "Ver também"):
- Cápsulas e filtros
- Xícaras e canecas

## Exemplo B — Vale a pena ter texto? (comportamento adaptativo)
Entrada:
```
Página: filtro "Cafeteiras > cor preta > ordenar por menor preço"
```
Como a skill age: pelo formato, parece um estado de filtro/ordenação, não uma categoria com intenção própria. A skill recomenda não criar texto e levanta o alerta técnico — como hipótese, porque não viu dado de busca nem de indexação.

Saída:
```
Recomendação: não criar texto para esta página.

"Cor preta + ordenar por menor preço" tem cara de estado de filtro, não de uma
categoria que as pessoas procuram — texto aqui tende a virar filler e ainda pode
criar uma página que concorre com a categoria principal "Cafeteiras".

Alerta técnico (hipótese, para quem cuida do SEO): combinações de filtro + ordenação
costumam gerar muitas URLs parecidas. Vale conferir no Search Console se esta URL
está indexada ou recebe buscas antes de decidir sobre indexação.
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
Como a skill age: remove o template e a repetição e troca por orientação geral, qualificada com "em geral" — a entrada não traz o sortimento, então o texto não afirma que a loja tem modelos para cada uso, não cita filtros e não inventa tipo de pisada.

Saída:
```
## Tênis de corrida
A escolha certa depende de onde e de quanto você corre.

### Como escolher
- Corre no asfalto, no dia a dia? Em geral, o amortecimento pesa mais.
- Treina em trilha? Em geral, vale procurar solado com mais aderência.
- Foca em provas rápidas? Em geral, modelos mais leves.
```
Antes de publicar:
- Deixe só as linhas que o seu sortimento cobre (sem tênis de trilha, tire a de trilha).
- Se a página tiver filtros (terreno, amortecimento, peso), me diga quais e eu aponto
  para eles — não citei nenhum porque não sei quais existem.
- Removido: "melhores tênis / melhores preços / loja de tênis de corrida" (repetição
  sem informação). Com a indicação de pisada oficial dos modelos, incluo esse critério.

> Referência: a skill entrega só o que ajuda a escolher, ancora no sortimento real,
> não cita filtro, link ou modelo que não veio, trata alerta técnico sem dado como
> hipótese, não força tamanho — e às vezes recomenda não ter texto.
