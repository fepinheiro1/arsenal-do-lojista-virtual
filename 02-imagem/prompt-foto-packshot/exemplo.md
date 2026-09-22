# Prompt de Foto Packshot — exemplos reais

## Exemplo A — Você tem foto real (modo editar)
Entrada:
```
Produto: caneca de cerâmica branca fosca, 350ml, alça arredondada, sem estampa
Foto real: sim (uma foto boa, frontal, em cima da mesa)
Canal: minha loja (Shopify)
```
Saída:
```
Modo: editar foto real (preferido)

Edit the attached product photo. Keep the product exactly as photographed: matte white
ceramic mug, 350ml, smooth rounded handle, no print — same shape, proportions, color and
finish. Do not redesign or recolor. Only change the presentation: replace the background
with a clean seamless soft-white studio background, apply soft even studio lighting with a
gentle natural contact shadow beneath the mug, remove dust and desk marks, keep the product
centered with safe margins (do not crop the handle or rim). Photorealistic, commercial
e-commerce catalog style. Square 1:1 composition. No added text, no added logo, no
watermark, no invented parts, no color change.
```
Proporção/resolução: 1:1, mire em 2048×2048 para a loja.
(Loja própria aceita mais liberdade que marketplace — dá para usar um fundo levemente degradê.)

## Exemplo B — Você só tem a descrição (conceito, com aviso)
Entrada:
```
Produto: caneca de cerâmica branca fosca, 350ml, alça arredondada
Foto real: não tenho
Canal: minha loja
```
Saída:
```
Modo: conceito (sem foto — fidelidade baixa para o produto real)

Studio packshot of a matte white ceramic mug, 350ml, with a smooth rounded handle, no
print. Single unit, centered and isolated on a seamless soft-white background, soft even
softbox studio lighting, gentle natural shadow beneath, subtle realistic reflection.
Photorealistic commercial product photography, sharp focus, high detail, e-commerce catalog
style. Square 1:1 composition. No added text, no added logo, no watermark, no extra objects,
realistic colors.
```
Atenção: sem uma foto real, a IA vai desenhar UMA caneca plausível — não necessariamente a
que você vende (o formato da alça e o tom do branco podem sair diferentes). Ótimo para testar
layout; arriscado como imagem definitiva. Assim que tiver uma foto real, use o modo editar
para travar o produto certo.

## Exemplo C — Embalagem com rótulo (fidelity lock forte)
Entrada:
```
Produto: sérum facial, frasco âmbar 30ml com conta-gotas, rótulo com o nome da marca
Foto real: sim
Canal: Google Shopping
```
Saída:
```
Modo: editar foto real (obrigatório aqui — o rótulo é o produto)

Edit the attached photo of the amber 30ml serum bottle with dropper. Preserve the bottle
shape, amber glass color, dropper cap and the printed label EXACTLY as shown — do not
regenerate, rewrite or restyle any text on the label; keep every printed word, logo and claim
identical. Only change the presentation: clean seamless white background, soft even studio
lighting that reveals the amber glass without false color, keep glass transparency and
realistic refraction, gentle contact shadow. Product clearly shown, centered. Photorealistic,
e-commerce catalog. No added text, no added graphics, no watermark, no color change.
```
Proporção/resolução: quadrada, 1500×1500 ou mais (recomendação do Google Shopping).
Atenção: nunca deixe a IA "reescrever" o texto do rótulo — modelos erram letra. Sempre
editando a foto real. E, se o canal pedir identificação de conteúdo gerado por IA, não
remova a metadata de origem da imagem.

## Exemplo D — Mesmo produto, canal Amazon
Entrada:
```
Produto: caneca de cerâmica branca fosca, 350ml (tenho foto real)
Canal: Amazon (imagem principal)
```
Saída:
```
Modo: editar foto real

Edit the attached mug photo for an Amazon MAIN image. Keep the product exactly as
photographed (matte white ceramic mug, 350ml, rounded handle, no print). Replace the
background with pure white (RGB 255,255,255). The mug should fill about 85% of the frame,
centered, sharp and high-resolution for zoom. Soft even lighting, minimal natural shadow.
No text, no logo overlay, no watermark, no props, no border, no color change.
```
Proporção/resolução: quadrada, lado maior 1600 px ou mais (para o zoom da Amazon).
(As regras da Amazon mudam por categoria e com o tempo — confirme o requisito atual da sua
categoria antes de subir.)

> Referência: prioriza editar a foto real, o fundo e o enquadramento vêm do canal (loja ≠
> Amazon ≠ Google), o rótulo e o logo reais são preservados, e sem foto a skill avisa que é
> só conceito.
