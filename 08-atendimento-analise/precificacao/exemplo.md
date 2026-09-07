# Precificação — exemplo real

## Entrada
```
Produto: caneca térmica de inox 500ml
Custo para mim: R$28 (inclui produto R$24 + embalagem R$4). NÃO inclui imposto
  nem taxa de cartão.
Margem que quero: 60% sobre o preço de venda
Referência de mercado: concorrentes vendem entre R$79 e R$99
Custos variáveis conhecidos: taxa de gateway 4% sobre a venda
```

## Saída
```
Números recebidos: custo R$28 (produto + embalagem); margem-alvo 60% sobre o preço de
venda; taxa de gateway 4%; referência de mercado R$79–R$99.
Faltando: [preencher: imposto sobre a venda] e [preencher: custo de frete, se você absorve].

Interpretação usada: margem de 60% SOBRE O PREÇO DE VENDA (não markup sobre custo).
Isso significa que custo + taxas precisam caber nos 40% restantes do preço.

Conta passo a passo:
- Custos que saem do preço: custo R$28 + gateway 4% do preço.
- Preço (P) tal que custo + 4%·P = 40%·P
  → 28 = 40%·P − 4%·P = 36%·P
  → P = 28 / 0,36 = R$77,78
- Arredondando para venda: R$79,00.

Preço sugerido: R$79,00
- Gateway (4%): R$3,16
- Custo do produto: R$28,00
- Margem: R$79,00 − R$28,00 − R$3,16 = R$47,84 (≈ 60,6% do preço). ✓

Comparação com o mercado:
R$79 fica no piso da faixa observada (R$79–R$99). Há espaço para subir até ~R$89–R$99
mantendo a margem e ainda dentro do mercado — teste qual preço o seu público aceita.

Faixa de manobra (se você aceitar margem mínima de 40% do preço):
- Preço mínimo p/ promoção: ≈ R$51,00 (margem ~40%, já com gateway). Abaixo disso,
  a margem cai rápido.
- Teto sugerido: R$99 (topo do mercado observado).

Alertas:
- Você NÃO informou imposto. Se houver, ele sai da sua margem — a margem real pode ser
  menor que 60%. Recalcule com o imposto para não se enganar. [preencher: imposto]
- Confira se absorve frete: se sim, ele também reduz a margem. [preencher: frete]
```

> Referência de qualidade: mostra a conta inteira, distingue margem-sobre-venda de
> markup, usa só os números dados, marca `[preencher]` para imposto e frete em vez de
> chutar, e alerta que a margem real pode ser menor — sem prometer preço "imperdível".
