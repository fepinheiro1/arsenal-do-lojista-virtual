---
name: precificacao
description: Calcula preço, preço mínimo de promoção, desconto máximo seguro e margem por canal a partir dos números reais do lojista — separando custo por unidade, custo por pedido e taxas que são porcentagem do preço (imposto, gateway, comissão), com a conta mostrada e feita por código. Distingue margem de contribuição, markup e lucro, trata imposto e taxa como dado do lojista (nunca chutados), bloqueia o preço final quando falta um dado crítico e mostra cenários de sensibilidade no lugar. Use para precificar produto novo, revisar preço, montar promoção, comparar canais, montar kit, simular cenários ou auditar a conta.
---

# Precificação

## O que faz
Chega ao preço pela **conta**, não pelo achismo — com os números que o lojista informa, cada um rotulado como **confirmado**, **estimado por você** ou **ausente**. Separa o que é custo fixo por unidade, o que é custo por pedido e o que é **porcentagem do preço** (imposto sobre a venda, taxa do gateway, comissão do marketplace), mostra a fórmula e o resultado, e diz com clareza **o que esse resultado cobre e o que não cobre**. Também calcula o preço mínimo de uma promoção, o desconto máximo seguro, quantas vendas a mais uma promoção precisa para empatar e a diferença de margem entre canais.

Regra de ouro: **nada de custo, taxa, imposto, preço de concorrente ou demanda inventados — e nada de preço final quando falta um dado crítico.** Nesse caso, a skill mostra a conta condicionada e cenários de sensibilidade, e diz o que falta. Margem de contribuição não é lucro, e preço sugerido não é preço garantido. A conta é feita por código sempre que possível; a IA explica e pede dados, não é a calculadora.

## Quando usar
- Precificar um produto novo ou revisar um preço que "não fecha a conta".
- Montar promoção, cupom ou frete grátis sem vender no prejuízo.
- Comparar o mesmo produto na loja própria e no marketplace.
- Precificar kits, variações com custos diferentes, liquidação de estoque.
- Simular cenários (custo, câmbio, taxa, devolução) ou auditar uma planilha de preço.

## O que a IA precisa de você
- `[produto, canal e moeda]` — e o objetivo (preço novo, revisão, promoção, comparação).
- `[custo de aquisição por unidade]` — mercadoria, frete de entrada, seguro, tributo não recuperável, importação (sem contar duas vezes).
- `[custos por unidade ou pedido]` — embalagem, etiqueta, preparação, brinde real, tarifa fixa por transação, frete que você paga.
- `[porcentagens sobre a venda]` — imposto sobre a venda (**alíquota efetiva informada por você ou pelo contador**), taxa do gateway por meio de pagamento (Pix, débito, cartão, parcelado), comissão do marketplace — e **sobre o que cada uma incide** (preço do item, frete incluso, valor com desconto).
- `[meta]` — margem de contribuição desejada sobre o preço (ou markup sobre o custo — diga qual).
- (opcional) taxa de devolução histórica, frete que você subsidia, custo de mídia por pedido (CAC), preços de concorrentes com data, custos fixos mensais e volume (se a pergunta for de lucro).

A skill pergunta só os campos essenciais que faltarem.

## Como funciona (por baixo)

**1. Cada número com origem e data.** Entradas **confirmadas**, **estimadas por você** ou **ausentes** — nunca preenchidas por suposição (alíquota, comissão, preço de mercado). Custos, câmbio, taxas e preços de concorrente têm data: dado antigo gera alerta. Conferência de qualidade: moeda, unidade, número negativo, porcentagem acima de 100%, imposto duplicado, custo já incluído em outro campo.

**2. Separar os três tipos de custo.** **Por unidade** (aquisição, embalagem do item), **por pedido** (tarifa fixa de transação, antifraude, etiqueta, caixa — rateada pelos itens do pedido quando preciso) e **porcentagem do preço** (imposto sobre a venda, gateway, comissão, royalty). Porcentagem **não se soma ao custo fixo**: ela é uma fração do próprio preço. E custos fixos do negócio (aluguel, equipe, sistemas) ficam fora da contribuição por unidade.

**3. Margem, markup e lucro não são a mesma coisa.**
- **Markup** sobre o custo: (P − C) ÷ C.
- **Margem** sobre o preço: (P − C) ÷ P.
- **Margem de contribuição**: o que sobra do preço depois de **todos os custos variáveis** (custo, taxas, frete subsidiado, devolução esperada…) — e ela **ainda precisa pagar os custos fixos**. Não é lucro líquido.
- Pediu meta de **lucro**? A skill pede volume e custos fixos; não transforma meta de lucro em margem de contribuição sem esses dados.

**4. As fórmulas (mostradas sempre).** Com custo C por unidade, taxas sobre o preço t e meta de contribuição m sobre o preço:
- **Preço-alvo**: P = C ÷ (1 − t − m). Se t + m ≥ 100%, **não existe preço que resolva** — a skill explica e pede para revisar as premissas.
- **Preço de equilíbrio** (contribuição zero): P₀ = C ÷ (1 − t) — e ele **não cobre** os custos fixos.
- **Preço mínimo de promoção**, com o piso de contribuição que você escolhe: Pmín = C ÷ (1 − t − m_mín). Piso gerencial ≠ limite legal ou contratual.
- Exemplo verificável: C = R$ 60, t = 20%, m = 20% → P = 60 ÷ 0,60 = **R$ 100**, contribuição R$ 20.
Contas com precisão decimal; arredondamento só na apresentação, com a regra dita.

**5. Imposto e meio de pagamento.** Regime tributário (Simples, não cumulativo, outros) muda tudo — a skill usa a **alíquota efetiva e a base de incidência que você ou o contador informam**, não faz apuração tributária e não incorpora ao custo imposto que pode ser recuperado sem checar o regime. Pix, débito, cartão e parcelado têm taxas diferentes: cenários por meio de pagamento, **sem presumir o mix**. Parcelamento e antecipação entram quando são custo efetivo — fluxo de caixa é uma coisa, resultado é outra.

**6. Os custos que escondem a margem.** **Frete subsidiado**: o que o cliente paga, o que a transportadora cobra e a diferença que sai do seu bolso. **Devoluções e cancelamentos**: custo esperado a partir da **sua** taxa histórica (frete, embalagem e taxas que não voltam). **Comissão de marketplace** por categoria e canal, com mínimos e tetos e a vigência conferida. **Mídia**: custo de aquisição por pedido novo, dito como média histórica (não custo marginal); **ROAS de equilíbrio = 1 ÷ margem antes da mídia**, se receita e gasto estão na mesma base — margem de 20% → ROAS 5; não vale se a margem é ≤ 0. **Carrinho**: vários itens no pedido e custos por pedido rateados — a margem de um item não é a margem do carrinho.

**7. Promoção sem se enganar.** Simular percentual, valor fixo, combo, cupom e frete grátis **separadamente**, com cumulatividade e base de incidência (o desconto muda a base do imposto e da comissão?). **Desconto máximo seguro** sai do piso de contribuição. **Preço menor não garante lucro maior**: para manter a contribuição total, a quantidade precisa crescer na proporção Q₂ ÷ Q₁ = MC₁ ÷ MC₂ — no exemplo acima, vender a R$ 90 derruba a contribuição de R$ 20 para R$ 12 e exige **66,7% mais vendas** só para empatar. **Preço "de" (riscado) só com histórico real** — desconto fictício é publicidade enganosa.

**8. Canais, variações, kits e estoque.** Loja própria, marketplace e venda assistida têm custos e preço mínimo diferentes — **o mesmo preço não dá a mesma margem**. Variação com custo diferente (tamanho, capacidade) não precisa ter preço único. Kit: soma dos custos reais, taxas por pedido e o desconto alocado com critério. Liquidação: giro, capital parado e obsolescência — aceitar margem menor é **decisão estratégica dita**, não acidente. Regras de preço mínimo e paridade de marketplace: conferir a política vigente, sem supor.

**9. Mercado e valor — sem inventar disposição a pagar.** Preço mínimo matemático, preço-alvo e **faixa de mercado observada** são coisas diferentes; **o teto comercial não sai do custo nem da faixa do concorrente**. Preço de concorrente só com fonte e data, e só entre equivalentes (produto, tamanho, quantidade, garantia, frete, parcelamento) — `analise-de-concorrente`. Preço premium cabe com diferencial **comprovado**, e disposição a pagar se **testa**, não se afirma. Final .90/.99 e âncoras são hipóteses de teste, sem padrão manipulador.

**10. Cenários e reprecificação.** Sensibilidade a custo, frete, câmbio, taxa e devolução; cenários **conservador, base e otimista** com as entradas à vista — hipóteses, não previsão. Gatilhos de revisão (mudou custo, comissão, imposto, mercado) — **nunca alterar preço sozinho, sem autorização**.

## Instruções (o cérebro da skill)
1. Identifique o **modo** (criar / auditar / repreçar / promoção / comparar canais / kit / cenários / lote).
2. Monte o **Pricing Truth Lock**: cada entrada com valor, moeda, base de incidência, se o imposto está incluso, origem e data. Confira a qualidade dos dados.
3. Classifique os custos (unidade, pedido, porcentagem) e deixe explícita a convenção (margem sobre o preço × markup).
4. **Calcule por código** (precisão decimal), checando se o denominador é positivo.
5. Se faltar **dado crítico** (custo, imposto/taxa sobre a venda, comissão do canal), **não entregue preço final**: mostre a conta condicionada e uma tabela de sensibilidade, rotulada como simulação.
6. Rode o **Quality Gate** e entregue com o que o resultado cobre e não cobre.

## Regras de qualidade
- **Nada inventado**: custo, taxa, imposto, comissão, preço de concorrente, demanda, disposição a pagar.
- **Origem de cada número**; dado ausente ou antigo sinalizado.
- **Porcentagem é fração do preço**, não custo fixo; base de incidência dita.
- **Margem de contribuição ≠ markup ≠ lucro**; dizer o que a margem ainda precisa pagar.
- **Preço final bloqueado** com dado crítico ausente; cenários rotulados no lugar.
- **Conta mostrada e feita por código**; denominador checado; arredondamento só no fim.
- **Imposto pela alíquota efetiva informada**; sem apuração tributária.
- **Canal a canal**; meio de pagamento a meio de pagamento; carrinho ≠ item.
- **Promoção com piso**, unidades para empatar e sem preço "de" inventado.
- **Teto não sai do custo**; premium só com diferencial comprovado e teste.
- **Nunca mudar preço sem autorização.** Apoio à decisão, não consultoria financeira, contábil ou jurídica.
- **Sem "preço imperdível"**: preço é conta, não grito.

### Pricing Quality Gate (silencioso — bloqueia)
Algum campo crítico ausente com preço final entregue? · Taxa percentual somada ao custo? · Base de incidência definida? · Imposto ou custo contado duas vezes? · Convenção (margem × markup) dita? · Denominador positivo? · Arredondamento só no fim? · Contribuição apresentada como lucro? · Desconto respeita o piso? · Preço "de" com histórico? · Canal e meio de pagamento separados? · Dados com data? · Teto deduzido do custo ou do concorrente? — se falhar, corrija ou bloqueie.

## Formato da saída
**Padrão:** os **números recebidos** (com origem) e **o que falta** · a **fórmula** e a **conta** · **preço de equilíbrio**, **preço-alvo** e **preço mínimo** (ou, se faltar dado crítico, a **tabela de sensibilidade** no lugar) · a **margem efetiva** em R$ e % · **o que essa margem ainda precisa cobrir** · **alertas**.

Sob pedido: promoção (desconto máximo, unidades para empatar), comparação entre canais, kit, cenários conservador/base/otimista, ROAS de equilíbrio, gatilhos de reprecificação, auditoria de uma planilha.

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
