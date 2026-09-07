---
name: otimizacao-de-checkout
description: Diagnostica o fluxo de checkout (etapas, campos, frete, meios de pagamento, confiança) e devolve as mudanças que mais reduzem abandono, em ordem de prioridade. Use quando muita gente adiciona ao carrinho mas poucos finalizam a compra.
---

# Otimização de Checkout

## O que faz
Percorre o caminho do carrinho até o "pedido confirmado" e aponta onde a pessoa desiste — campo demais, frete que aparece tarde, falta do meio de pagamento que ela usa, cadastro obrigatório. Devolve as correções na ordem que mais recupera venda. É o ponto mais quente do funil: quem chegou ao checkout já quer comprar; o trabalho é tirar o atrito do caminho.

## Quando usar
- A taxa "adicionou ao carrinho → finalizou" está baixa.
- Depois de uma mudança na loja (novo tema, novo gateway) que pode ter criado atrito.
- Antes de escalar tráfego — cada real de anúncio rende mais com um checkout limpo.

## O que a IA precisa de você
- `[fluxo atual]` — descreva as etapas do checkout: quantas telas, o que pede cada uma, se exige criar conta.
- `[campos do formulário]` — lista dos campos pedidos (nome, CPF, telefone, endereço, etc.).
- `[frete]` — como e quando o frete aparece: calculado no carrinho, só no fim, tem grátis a partir de valor?
- `[meios de pagamento]` — o que a loja aceita (Pix, cartão, boleto, carteiras, parcelamento).
- `[plataforma]` (opcional) — Nuvemshop, Shopify, Tray, etc., para respeitar o que dá para mudar.
- `[dados de abandono]` (opcional) — em que etapa a maioria some, se você tiver esse número.

## Instruções (o cérebro da skill)
Analise o checkout nestes **8 pontos** e diga, em cada um, o atrito encontrado e a correção.

1. **Número de etapas** — quantas telas até confirmar? Menos passos, menos desistência. Aponte etapas que dá para juntar.
2. **Login obrigatório** — exige criar conta antes de comprar? Ofereça compra como convidado; conta vira opcional no fim.
3. **Campos do formulário** — todo campo pedido é necessário? Corte o que não for essencial para faturar e entregar. Marque campos que podem ser preenchidos sozinhos (endereço pelo CEP).
4. **Frete** — o custo aparece cedo (no carrinho), não só no fim? Frete surpresa na última tela é a causa nº 1 de abandono. Se há frete grátis por valor, mostre quanto falta para chegar lá.
5. **Meios de pagamento** — a loja oferece o que o público usa (Pix, cartão parcelado, boleto)? Falta de opção derruba venda. As condições de parcelamento estão claras?
6. **Custo total transparente** — a pessoa vê o total (produto + frete + taxas) antes de pagar, sem surpresa? Custo escondido quebra a confiança na hora H.
7. **Confiança no pagamento** — selo de segurança, ambiente do gateway, política de troca visível reduzem o receio de digitar o cartão.
8. **Erros e recuperação** — mensagens de erro claras (o que corrigir), e um caminho para retomar carrinho abandonado (e-mail/WhatsApp de lembrete honesto, sem pressão).

Depois, monte a **lista priorizada** por impacto no abandono × esforço de implementação, considerando o que a `[plataforma]` permite.

## Regras de qualidade
- Recomende só o que reduz atrito de verdade — não invente etapa "de segurança" que atrapalha.
- Lembrete de carrinho é convite, não cobrança: nada de "você esqueceu" com culpa, nem contador falso de "sua reserva expira".
- Não invente prazo de frete, taxa ou condição de parcelamento — se o dado não veio, marque `[preencher]`.
- Respeite o que a plataforma do lojista permite mudar; não recomende o impossível.
- Priorize por impacto real. Frete e meios de pagamento costumam pesar mais que cor de botão.

## Formato da saída
1. **Resumo** (2–3 linhas): onde está o maior vazamento do checkout.
2. **Tabela dos 8 pontos**: Ponto | Atrito encontrado | Correção.
3. **Plano priorizado**: correções da que mais recupera venda para a que menos, com esforço (baixo/médio/alto).

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
