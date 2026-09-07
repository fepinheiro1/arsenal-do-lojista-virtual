---
name: prompt-cena-de-uso
description: Monta um prompt de imagem em inglês com uma pessoa usando o produto, focando o benefício em ação. Use para mostrar o produto resolvendo algo na vida real — o momento que faz a pessoa entender para que serve.
---

# Prompt de Cena de Uso

## O que faz
Gera um prompt pronto para uma IA de imagem que mostra uma pessoa usando o seu produto e colhendo o benefício na hora. É a foto que responde "como isso funciona na minha vida?" sem uma palavra. Instruções em português; **o prompt final sai em inglês**.

## Quando usar
- O benefício do produto fica claro quando alguém está usando (não só olhando).
- Você quer imagens para anúncio, página ou social que mostrem o produto em ação.
- Precisa de gente real na cena sem contratar modelo e estúdio.

## O que a IA precisa de você
- `[produto]` — o que é, cor e material reais.
- `[benefício em ação]` — o que a cena precisa mostrar acontecendo (ex.: "café ainda quente na segunda xícara", "pé firme na trilha").
- `[quem usa]` — perfil genérico da pessoa (faixa de idade, contexto). Sem citar celebridade ou pessoa real.
- `[cenário]` — onde acontece.
- `[enquadramento]` (opcional) — mãos + produto, plano médio, close no momento.
- `[proporção]` (opcional) — 4:5 para feed, 9:16 para stories/reels.

## Instruções (o cérebro da skill)
Monte **um prompt em inglês** com estes blocos. O benefício mostrado precisa ser real; nunca encene um resultado que o produto não entrega.

1. **Sujeito e ação (subject + action):** a pessoa (perfil genérico) usando o produto, com o benefício visível acontecendo — `a woman in her 30s sipping coffee that is still steaming`.
2. **Produto (product):** claramente em uso e reconhecível, descrito com fidelidade.
3. **Emoção (expression):** natural e autêntica — `relaxed, genuine expression`. Sem sorriso de propaganda exagerado.
4. **Cenário e luz (setting + light):** ambiente coerente, `natural soft light`.
5. **Enquadramento (framing):** o pedido do lojista — `close-up on the hands and the product`, `medium shot`, focando o momento do benefício.
6. **Estilo + proporção:** `authentic lifestyle photography, photorealistic, high detail, natural skin tones, natural hands with correct anatomy`, e `aspect ratio 4:5 --ar 4:5` (ou o pedido).

Feche com as travas: `no text, no logo, no watermark, natural realistic proportions`.

## Regras de qualidade
- O benefício encenado é real. A imagem não promete o que o produto não faz.
- Pessoas representadas de forma natural e respeitosa; sem padrão de corpo irreal, sem citar pessoa real.
- Descreva o produto real — cor e material batem com a entrega.
- Sem texto ou selo dentro da imagem. A cena é da marca do lojista, não da Performa.
- Sempre inclua `natural hands with correct anatomy` — mãos são o erro nº 1 de IA de imagem.

## Formato da saída
1. **O prompt em inglês**, em bloco de código, pronto para colar.
2. **2 variações** de enquadramento ou perfil de pessoa para testar.
3. Uma linha em português com a dica de proporção e o lembrete de que, se a IA aceitar referência, anexar a foto real do produto ajuda a manter o item fiel.

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
