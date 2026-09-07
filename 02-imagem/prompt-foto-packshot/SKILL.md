---
name: prompt-foto-packshot
description: Monta um prompt de imagem em inglês para uma foto de produto em fundo limpo, padrão e-commerce (packshot/still de estúdio, luz de softbox). Use quando não há foto profissional do produto e você precisa da imagem principal do anúncio.
---

# Prompt de Foto Packshot

## O que faz
Transforma a descrição do seu produto em um prompt pronto para colar numa IA de imagem (Midjourney, DALL·E, Nano Banana/Gemini) e gerar a foto principal do anúncio: produto isolado, fundo limpo, luz de estúdio — o padrão que marketplace e loja pedem. As instruções e o preenchimento são em português; **o prompt final sai em inglês**, porque modelos de imagem respondem melhor assim.

## Quando usar
- Você ainda não tem foto profissional do produto e precisa da imagem de capa.
- Quer padronizar o catálogo com o mesmo fundo e a mesma luz.
- Vai testar variações de ângulo antes de fotografar de verdade.

## O que a IA precisa de você
- `[produto]` — o que é, cor, material e acabamento reais (ex.: "caneca de cerâmica branca fosca, 350ml").
- `[detalhes que importam]` — alça, textura, estampa, tampa, o que precisa aparecer.
- `[ângulo desejado]` (opcional) — frontal, 3/4 (hero) ou de cima (flat lay). Se não souber, a IA sugere.
- `[fundo]` (opcional) — branco puro, cinza-claro ou leve gradiente. Padrão: cinza-claro.
- `[proporção]` (opcional) — 1:1 para marketplace, 4:5 para feed.

## Instruções (o cérebro da skill)
Monte **um prompt em inglês** juntando estes seis blocos, nesta ordem. Descreva o produto com fidelidade — nunca invente cor, material ou detalhe que o lojista não informou.

1. **Sujeito (subject):** o produto descrito com precisão — tipo, cor, material, acabamento, detalhes que importam. Sempre isolado, uma unidade.
2. **Ângulo (angle/composition):** traduza o pedido do lojista — `front-facing`, `slight 30-degree eye-level hero angle` ou `top-down flat lay`. Produto centralizado.
3. **Luz (light):** `soft even softbox studio lighting`, sombra suave e natural embaixo, reflexo sutil e realista.
4. **Fundo (background):** `seamless [cor] background`, limpo, sem outros objetos disputando atenção.
5. **Estilo (style):** `commercial product photography, ultra sharp focus, high detail, photorealistic, e-commerce catalog style`.
6. **Proporção (aspect ratio):** feche com `aspect ratio 1:1` (ou o pedido) e o parâmetro do Midjourney `--ar 1:1`.

No fim do prompt, some as travas técnicas: `no text, no logo, no watermark, no extra objects, realistic colors`.

## Regras de qualidade
- Descreva o produto real. Se a IA "melhorar" cor ou formato, a foto engana o cliente na entrega.
- Sem texto, preço ou selo dentro da imagem — isso entra depois, por cima, se você quiser.
- Um produto por foto. Fundo limpo é o que faz o marketplace aprovar.
- A imagem representa a loja do lojista, não a Performa. Nenhuma marca aparece na arte.

## Formato da saída
1. **O prompt em inglês**, em um bloco de código, pronto para colar.
2. **2 variações** para testar (ex.: um ângulo hero 3/4 e um flat lay de cima).
3. Uma linha em português com a dica de proporção e, se o modelo aceitar imagem de referência, o lembrete de anexar uma foto real do produto para manter cor e formato.

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
