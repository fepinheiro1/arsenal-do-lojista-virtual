---
name: prompt-foto-lifestyle
description: Monta um prompt de imagem em inglês para o produto em contexto real de uso — ambiente, clima e luz natural, com o produto como protagonista (sem pessoa em foco, ou com pessoa só de apoio). Use para dar vida ao catálogo e mostrar o produto no dia a dia de quem compra.
---

# Prompt de Foto Lifestyle

## O que faz
Gera um prompt pronto para uma IA de imagem que coloca o seu produto num cenário real — a cozinha, a mesa do café, o criado-mudo — com luz natural e clima. É a foto que faz a pessoa se imaginar usando. O produto continua sendo o protagonista; se houver pessoa, ela entra só como apoio (mão, silhueta, fora de foco). Instruções em português; **o prompt final sai em inglês**.

## Quando usar
- O produto já tem packshot e você quer imagens que contam o contexto de uso.
- Vai montar feed, banner ou página que precisa de clima, não só do produto no branco.
- Quer mostrar a escala e o momento de uso sem contratar produção.

## O que a IA precisa de você
- `[produto]` — o que é, cor e material reais.
- `[público / momento de uso]` — para quem e em que hora do dia (ex.: "mãe, manhã, café antes do trabalho").
- `[ambiente]` — onde a cena acontece (cozinha de madeira clara, mesa de café, quarto minimalista).
- `[clima desejado]` — aconchegante, clean, sofisticado, natural.
- `[proporção]` (opcional) — 4:5 para feed, 16:9 para banner.

## Instruções (o cérebro da skill)
Monte **um prompt em inglês** com estes blocos. Descreva o produto com fidelidade; o cenário pode ser criativo, o produto não.

1. **Sujeito (subject):** o produto como herói da cena, em primeiro plano e nítido, descrito com fidelidade.
2. **Cenário (setting):** o ambiente coerente com o público e o momento — `on a light wooden kitchen counter`, `on a bedside table`, etc.
3. **Clima e luz (mood + light):** `warm natural morning light from a window`, `golden hour`, `soft cozy atmosphere` — conforme o pedido.
4. **Composição (composition):** produto em foco com `shallow depth of field`, fundo levemente desfocado, regra dos terços. Se houver pessoa, `a person softly out of focus in the background` ou só `a hand` — nunca roubando o foco.
5. **Apoio de cena (props):** 1 ou 2 objetos que combinam com o contexto, sem competir com o produto.
6. **Estilo + proporção:** `lifestyle product photography, photorealistic, high detail, natural colors`, e `aspect ratio 4:5 --ar 4:5` (ou o pedido).

Feche com as travas: `no text, no logo, no watermark`.

## Regras de qualidade
- O produto é sempre o protagonista. Cenário e props existem para valorizá-lo, não para disputar.
- Descreva o produto real — cor e material batem com o que chega na casa do cliente.
- Sem texto ou selo dentro da imagem.
- Clima verdadeiro, sem exagero de propaganda. A cena representa a marca do lojista, não a Performa.

## Formato da saída
1. **O prompt em inglês**, em bloco de código, pronto para colar.
2. **2 variações** de ambiente ou clima para testar (ex.: manhã aconchegante x mesa clean de meio-dia).
3. Uma linha em português com a dica de proporção e, se o modelo aceitar referência, o lembrete de anexar a foto real do produto.

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
