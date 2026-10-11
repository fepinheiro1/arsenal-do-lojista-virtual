# Precificação — exemplos reais

> Todas as contas abaixo foram feitas por código, com precisão decimal, arredondando só no fim.

## Exemplo A — Falta o imposto: sem preço final, com simulação
Entrada:
```
Produto: caneca térmica de inox 500 ml · Canal: loja própria · BRL
Custo por unidade: R$ 28 (produto R$ 24 + embalagem R$ 4) — confirmado
Gateway: 4% sobre a venda — confirmado
Imposto sobre a venda: não sei (ainda não falei com o contador)
Meta: 60% de margem sobre o preço
Frete: às vezes subsidio, não sei quanto · Concorrentes: entre R$ 79 e R$ 99 (vi semana passada)
```
Saída:
```
Recebido: custo R$ 28 (confirmado), gateway 4% (confirmado), meta 60% sobre o preço.
Falta — CRÍTICO: imposto sobre a venda (alíquota efetiva e base). Falta também: frete subsidiado.
→ Sem o imposto, não dá para entregar um preço final com segurança.

Fórmula: Preço = Custo ÷ (1 − taxas sobre a venda − meta) = 28 ÷ (1 − 0,04 − imposto − 0,60)

Simulação (NÃO é a sua alíquota — é para ver o peso do imposto):
Imposto sobre a venda | Preço para bater 60%
0%                    | R$ 77,78
5%                    | R$ 90,32
10%                   | R$ 107,69
20%                   | R$ 175,00
36% ou mais           | impossível (taxas + meta chegam a 100%)

Leitura: com uma meta de 60%, cada ponto de imposto pesa muito no preço. Antes de fixar o preço,
pegue a alíquota efetiva com o contador. Talvez a meta de 60% precise ser revista.

O que esses 60% ainda precisam pagar: frete que você subsidia, devoluções, anúncio e os custos
fixos da loja. Não são lucro.
Sobre os concorrentes (R$ 79 a R$ 99): é uma faixa observada há uma semana, não um teto, e só vale
para comparar se o produto for equivalente (mesmo inox, mesma capacidade, mesmas condições).
→ analise-de-concorrente.
```

## Exemplo B — Promoção, ROAS de equilíbrio e canais
Entrada:
```
Produto: luminária de mesa · Custo por unidade: R$ 60 (mercadoria + embalagem) — confirmado
Loja própria: imposto efetivo 15% (do contador) + gateway 5% = 20% sobre a venda — confirmado
Marketplace: imposto 15% + comissão 16% sobre a venda + tarifa fixa de R$ 5 por pedido
  (conferi a tabela do marketplace hoje)
Meta: 20% de margem de contribuição sobre o preço · Piso aceito em promoção: 10%
Quero fazer uma promoção de R$ 100 por R$ 90 na loja própria
```
Saída:
```
LOJA PRÓPRIA (taxas sobre a venda: 20%)
Preço-alvo = 60 ÷ (1 − 0,20 − 0,20) = 60 ÷ 0,60 = R$ 100,00 → contribuição R$ 20,00 (20%)
Equilíbrio = 60 ÷ (1 − 0,20) = R$ 75,00 (contribuição zero; não cobre custos fixos)
Promoção a R$ 90: contribuição = 90 × 0,80 − 60 = R$ 12,00 (13,33% do preço)
  → para manter a contribuição total, precisa vender 20 ÷ 12 = 1,67 vez mais: +66,7% de unidades,
    só para empatar.
Preço mínimo com piso de 10% = 60 ÷ (1 − 0,20 − 0,10) = R$ 85,71 → desconto máximo seguro sobre
  R$ 100: 14,29%. A promoção de R$ 90 está acima do piso.
Preço "de R$ 100": só se R$ 100 for mesmo o preço praticado antes (com histórico).
ROAS de equilíbrio na mídia (margem antes da mídia de 20%, mesma base de receita e gasto):
  1 ÷ 0,20 = 5. Abaixo de 5, o anúncio come a contribuição.

MARKETPLACE (taxas sobre a venda: 31%; custo por pedido: R$ 60 + R$ 5)
Preço-alvo = 65 ÷ (1 − 0,31 − 0,20) = 65 ÷ 0,49 = R$ 132,65
Se vender a R$ 100 também no marketplace: contribuição = 100 × 0,69 − 65 = R$ 4,00 (4%).
→ O mesmo preço nos dois canais dá margens muito diferentes. Confira se o marketplace exige
  paridade de preço antes de decidir.

O que a contribuição ainda precisa pagar: frete subsidiado e devoluções (não informados) e os
custos fixos. Nenhum preço foi alterado: a decisão é sua.
```

> Referência: cada número tem origem; porcentagem entra como fração do preço; a conta é mostrada e
> conferida por código; sem imposto não há preço final (há simulação rotulada); margem de
> contribuição não é chamada de lucro; promoção vem com piso e com as vendas necessárias para
> empatar; e cada canal tem a sua conta.
