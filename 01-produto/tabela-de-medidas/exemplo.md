# Tabela de Medidas — exemplos reais

## Exemplo A — Corpo ou peça? (a skill pergunta)
Entrada:
```
Camiseta
P 48
M 51
G 54
```
Como a skill age: um número só por tamanho, sem rótulo. Antes de montar qualquer tabela, ela confirma o que esses números significam — porque muda tudo.

Saída:
```
Antes de montar o guia, preciso confirmar uma coisa:

Esses números (48, 51, 54 cm) são:
(a) a largura da peça, medida de axila a axila com a camiseta esticada na mesa; ou
(b) a circunferência do corpo (busto) indicada para cada tamanho?

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
2. Ou publicamos a tabela em comprimento do pé (cm), que vale para qualquer sistema
   e é a informação mais segura para o cliente acertar.
```

## Exemplo D — Calçado (medir o pé; número só com tabela oficial)
Entrada:
```
Tênis. Tabela oficial de comprimento interno:
38 = 24,0 cm · 39 = 24,7 cm · 40 = 25,4 cm · 41 = 26,1 cm
```
Como a skill age: como a tabela oficial comprimento→número foi fornecida, monta a equivalência e ensina a medir o pé do jeito certo.

Saída:
```
## Guia de tamanhos
A medida abaixo é o comprimento do pé (do calcanhar à ponta do dedo maior). Sistema BR.

| Tamanho | Comprimento do pé |
|---|---:|
| 38 | 24,0 cm |
| 39 | 24,7 cm |
| 40 | 25,4 cm |
| 41 | 26,1 cm |

### Como medir
- De pé sobre uma folha, marque do calcanhar até a ponta do dedo maior.
- Meça os dois pés e use o maior (é normal um ser um pouco maior que o outro).
- Escolha o tamanho cujo comprimento seja igual ou logo acima da sua medida.
```

> Referência: sempre rotular corpo/peça/produto, converter só o físico (cm↔pol),
> e nunca inventar equivalência internacional nem "suba um tamanho" sem regra.
