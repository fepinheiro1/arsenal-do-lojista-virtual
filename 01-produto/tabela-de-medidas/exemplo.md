# Tabela de Medidas — exemplos ilustrativos

> Casos de demonstração: cada afirmação da saída vem da entrada — o que não veio vira pergunta ou pendência.

## Exemplo A — Corpo ou peça? (a skill pergunta)
Entrada:
```
Camiseta
P 48
M 51
G 54
```
Como a skill age: um número só por tamanho, sem rótulo e sem unidade. Antes de montar qualquer tabela, ela confirma o que esses números significam e em que unidade estão — não presume centímetro.

Saída:
```
Antes de montar o guia, preciso confirmar uma coisa:

Esses números (48, 51, 54) são:
(a) a largura da peça, medida de axila a axila com a camiseta esticada na mesa; ou
(b) a circunferência do corpo (busto) indicada para cada tamanho?
E estão em centímetros?

É a diferença entre um "guia da peça" e um "guia do corpo", e cada um leva uma
instrução de medição diferente. Me diga qual é e eu monto a tabela certa.
```

## Exemplo B — Guia do corpo (com opção de polegadas)
Entrada:
```
Guia do CORPO, sistema BR. Vestido feminino.
P: busto 84, cintura 66, quadril 92
M: busto 88, cintura 70, quadril 96
G: busto 92, cintura 74, quadril 100
(medidas em cm)
```
Como a skill age: rotula como corpo, mantém a unidade, e não arrisca recomendação de caimento sem regra de modelagem (nada de "escolha o maior").

Saída:
```
## Guia de tamanhos
As medidas abaixo são do corpo (a sua, não a da peça). Sistema BR.

| Tamanho | Busto (cm) | Cintura (cm) | Quadril (cm) |
|---|---:|---:|---:|
| P | 84 | 66 | 92 |
| M | 88 | 70 | 96 |
| G | 92 | 74 | 100 |

### Como medir
- Busto: passe a fita na parte mais cheia do busto, sem apertar.
- Cintura: na parte mais fina do tronco.
- Quadril: na parte mais larga do quadril.

### Sobre o caimento
Se ficar entre dois tamanhos, compare suas medidas com a tabela e considere o
caimento que você prefere — mais justo ou mais soltinho.
```
(Quer a versão com uma coluna em polegadas? É conversão física segura — posso adicionar.)

## Exemplo C — Conversão internacional sem fonte (recusa honesta)
Entrada:
```
Tênis BR 40. Adiciona US e EU.
```
Como a skill age: conversão de tamanho comercial não é conta fixa — varia por marca. Sem tabela oficial, não inventa.

Saída:
```
A equivalência entre BR, US e EU de calçado não é uma conta fixa — muda de marca
para marca (o "US" de uma não é o "US" de outra). Por isso eu não vou chutar um
número que pode fazer a pessoa comprar errado.

Duas formas de resolver:
1. Me mande a tabela de conversão oficial da marca (quase toda tem) e eu monto a
   equivalência certinha.
2. Ou, se você tiver a medida de cada número em centímetros (o comprimento interno
   ou da palmilha, por exemplo), publicamos a tabela em cm, que não depende de sistema.
   Sem essa medida, eu não monto tabela em cm — não tenho de onde tirar os valores.
```

## Exemplo D — Calçado com comprimento interno (não é o tamanho do pé)
Entrada:
```
Tênis. Tabela oficial de comprimento interno:
38 = 24,0 cm · 39 = 24,7 cm · 40 = 25,4 cm · 41 = 26,1 cm
```
Como a skill age: comprimento interno é medida do produto (o espaço dentro do calçado), não do pé — então ela preserva a grandeza como veio. Não manda medir o pé e escolher pela tabela, porque o pé precisa de folga lá dentro e quanto de folga é regra da marca, que não veio. E não chama a numeração de "BR": o sistema não foi informado.

Saída:
```
## Guia de tamanhos
As medidas abaixo são o comprimento interno do calçado (o espaço por dentro,
do calcanhar à ponta) — não o tamanho do pé.

| Tamanho | Comprimento interno (cm) |
|---|---:|
| 38 | 24,0 |
| 39 | 24,7 |
| 40 | 25,4 |
| 41 | 26,1 |

### Como usar esta tabela
- Pegue um calçado seu que veste bem e meça por dentro, do calcanhar à ponta
  (se a palmilha sair, meça a palmilha).
- Compare essa medida com a coluna acima.
```
Antes de publicar, confirme:
- o sistema da numeração 38–41 (BR? EU?) — veio sem sistema;
- se a marca indica quanto de folga deixar ou tem uma tabela pelo comprimento do pé.
  Com isso eu acrescento o "meça o seu pé" com a regra certa; sem isso, recomendar
  tamanho pelo pé faria a pessoa comprar apertado.

> Referência: sempre rotular corpo/peça/produto e manter a grandeza que veio
> (comprimento interno não vira pé), não presumir unidade nem sistema, converter só o
> físico (cm↔pol) e nunca inventar equivalência internacional nem "suba um tamanho" sem regra.
