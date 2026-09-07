---
name: prompt-banner-campanha
description: Monta um prompt de imagem em inglês para um banner/hero de campanha com espaço negativo reservado para o texto entrar depois — composição, não texto embutido na arte. Use para topo de site, hero de coleção ou peça de campanha.
---

# Prompt de Banner de Campanha

## O que faz
Gera um prompt pronto para uma IA de imagem que cria a **arte de fundo** de um banner de campanha — com o produto ou a cena posicionados de um lado e um espaço limpo reservado do outro, para você colocar o texto por cima depois. A IA de imagem escreve texto mal (letras tortas, palavra errada) e um preço ou promessa embutido vira risco de propaganda enganosa. Por isso: **o texto não entra na imagem** — entra por cima, no editor, controlado por você. Instruções em português; **o prompt final sai em inglês**.

## Quando usar
- Topo de site (hero), banner de coleção, peça de lançamento ou data comercial.
- Você tem o texto/oferta e precisa de um fundo bonito com lugar para ele respirar.
- Quer padronizar a campanha nas cores da sua marca.

## O que a IA precisa de você
- `[conceito da campanha]` — a ideia/clima (ex.: "coleção de inverno, aconchego").
- `[produto ou cena]` — o que aparece na arte, com cor e material reais.
- `[lado do espaço negativo]` — onde o texto vai entrar (esquerda, direita, centro, base).
- `[cores da marca]` — paleta ou clima de cor da sua loja (a arte usa as SUAS cores, não as da Performa).
- `[proporção]` — 16:9 hero de site, 1:1 feed, 9:16 stories.
- `[texto do banner]` — só para você ter em mãos; **não vai dentro da imagem** → `[preencher]` no editor depois.

## Instruções (o cérebro da skill)
Monte **um prompt em inglês** com estes blocos. O texto nunca entra na arte.

1. **Conceito e clima (concept + mood):** traduza a ideia da campanha em atmosfera visual.
2. **Sujeito e posição (subject + placement):** produto/cena de um lado, descrito com fidelidade — `product positioned on the right third of the frame`.
3. **Espaço negativo (negative space):** deixe explícito o lado limpo — `clean empty negative space on the left half for text overlay, uncluttered`.
4. **Fundo e cor (background + color):** paleta da marca — `soft gradient background in [cores]`, coerente e não poluído.
5. **Luz e estilo (light + style):** `soft directional light, premium advertising look, photorealistic, high detail`.
6. **Proporção (aspect ratio):** `wide hero banner composition, aspect ratio 16:9 --ar 16:9` (ou o pedido).

Feche com as travas: `no text, no letters, no words, no logo, no watermark` — para garantir a arte limpa.

## Regras de qualidade
- **Nenhum texto, preço, porcentagem ou selo dentro da imagem.** Isso entra por cima, depois, e o que for número real você preenche — nunca a IA inventa.
- Sem "imperdível", "última chance", "explosão de vendas" — nem no texto que você colocar depois, nem no clima da arte.
- Espaço negativo de verdade: o lado do texto fica limpo e legível.
- A arte usa as cores da marca do lojista. Nenhuma identidade da Performa aparece.
- Produto descrito com fidelidade (cor, material).

## Formato da saída
1. **O prompt em inglês**, em bloco de código, pronto para colar.
2. **2 variações** de composição (ex.: espaço à esquerda x espaço na base) para testar.
3. Uma linha em português lembrando que o texto/oferta entra por cima no editor, com os números reais preenchidos por você.

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
