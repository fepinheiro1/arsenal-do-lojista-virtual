---
name: precificacao
description: Apoia a decisão de preço de um produto a partir do custo, da margem-alvo e da referência de mercado que o lojista informar — calcula com os números dados e nunca inventa custo, preço de concorrente ou demanda. Use ao precificar um produto novo, revisar um preço que não fecha a conta ou montar preço promocional sem destruir a margem.
---

# Precificação

## O que faz
Ajuda a chegar a um preço com base em conta, não em achismo: parte do custo real, da margem que você quer e da referência de mercado que você trouxer, e mostra o preço sugerido, a margem que ele gera e o espaço que sobra para promoção. Só usa os números que você informar — o que faltar, ela pede.

## Quando usar
- Ao precificar um produto novo.
- Quando um preço atual "não fecha a conta" e você quer revisar.
- Para montar um preço promocional sem descobrir depois que vendeu no prejuízo.

## O que a IA precisa de você
- `[produto]` — o que é.
- `[custo]` — quanto o produto custa para você (produto + o que você quiser incluir: embalagem, imposto, taxa de gateway, frete que você absorve). Diga o que já está incluído.
- `[margem-alvo]` — a margem ou o lucro que você quer (em % ou em R$).
- `[referência de mercado]` (opcional) — a que preço concorrentes vendem algo parecido, se você souber.
- `[custos variáveis conhecidos]` (opcional) — comissão de marketplace, parcelamento, etc.

Todos os números vêm de você. A IA não estima custo, preço de concorrente nem volume de vendas.

## Instruções (o cérebro da skill)
1. **Confirme os números** que o lojista deu e liste em uma linha o que ele **não** deu. Se faltar custo ou margem-alvo, marque `[preencher]` e explique que sem esses dois não dá para calcular com segurança — não chute.
2. **Deixe explícito** se a margem-alvo é sobre o custo (markup) ou sobre o preço de venda, e calcule pela interpretação escolhida (diga qual usou).
3. **Calcule o preço sugerido** aplicando a margem-alvo ao custo, somando os custos variáveis informados. Mostre a conta passo a passo, com os números.
4. **Mostre a margem em R$ e em %** que esse preço gera.
5. **Compare com a referência de mercado** só se o lojista a informou: onde o preço sugerido fica (abaixo, na média, acima) e o que isso implica. Sem referência, não invente — sugira o lojista pesquisar.
6. **Faixa de manobra**: mostre o **preço mínimo** (onde a margem chega ao limite que o lojista aceita) e o teto sugerido, para orientar promoção sem vender no prejuízo.
7. **Aponte riscos** de forma objetiva: se algum custo comum não foi informado (imposto, taxa de cartão, frete), lembre que a margem real pode ser menor e peça para conferir.

## Regras de qualidade
- Nunca invente custo, preço de concorrente, imposto ou volume de vendas — o que faltar vira `[preencher]`.
- Mostre a conta. O lojista precisa entender de onde saiu o número, não receber um preço mágico.
- Deixe claro markup vs. margem sobre venda — a confusão entre os dois é o erro nº 1.
- Não é consultoria financeira nem recomendação de investimento: é apoio à decisão de preço com os dados do lojista.
- Sem "preço imperdível" ou apelo de urgência. Preço é conta, não grito.

## Formato da saída
- **Números recebidos** e **o que falta** (`[preencher]`).
- **Conta passo a passo** até o preço sugerido.
- **Preço sugerido**, com margem em R$ e %.
- **Comparação com o mercado** (só se houver referência).
- **Faixa de manobra**: preço mínimo e teto.
- **Alertas** de custos não informados que podem comer a margem.

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
