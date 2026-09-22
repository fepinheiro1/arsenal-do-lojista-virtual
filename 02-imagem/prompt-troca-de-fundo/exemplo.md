# Prompt de Troca de Fundo — exemplos reais

## Exemplo A — Fundo branco de marketplace (Amazon MAIN)
Entrada:
```
Produto: tênis branco de couro (foto sobre mesa de madeira bagunçada, com sombra boa)
Objetivo: fundo neutro
Canal: Amazon (imagem principal)
```
Saída:
```
Modo: fundo neutro (Amazon MAIN)

Edit the attached product photo. Protect the product region — a white leather sneaker — and
preserve it pixel for pixel: exact shape, color, leather texture, stitching, laces, logo and
any printed text. Replace ONLY the background with pure white (RGB 255,255,255), clean and
even, no props. The original photo already has a good contact shadow: keep a soft clean
version of that real contact shadow under the sneaker (do not invent a new cast shadow, do
not make it float). Precise edges, no halo, no leftover wood-color spill on the edges. Crop
to square with safe margins (do not cut the sole or toe). High resolution for zoom. Do not
add new text, preserve existing product text and labels exactly, no added logo, no watermark,
photorealistic result.
```
Modo: fundo neutro · Canal: Amazon MAIN (branco puro, alta resolução para zoom).
(A sombra real, que era boa, foi preservada e limpa — não inventei uma nova.)

## Exemplo B — Produto difícil (vidro transparente)
Entrada:
```
Produto: perfume em frasco de vidro transparente com líquido âmbar
Objetivo: fundo neutro claro
Canal: minha loja
```
Saída:
```
Modo: fundo neutro — ATENÇÃO: item transparente (revisão recomendada)

Edit the attached photo of the transparent glass perfume bottle with amber liquid. This is a
transparent product: preserve the glass transparency, the refraction and the highlights, and
let the new clean light-gray background show THROUGH the glass plausibly — do not fill the
glass with a flat false color and do not make it opaque. Keep the amber liquid color, the cap
and the printed label exactly. Replace only the surrounding background, keep a soft real
contact shadow, precise edges with no halo. Do not add new text, preserve existing label text
exactly, no added logo, no watermark.
```
Modo: fundo neutro · Canal: loja própria.
Atenção: vidro/transparência é o caso mais difícil de recorte. Use uma ferramenta com máscara
e confira a olho — se o fundo não aparecer através do vidro de forma natural, vale edição
manual. (Melhor ainda: fotografar o frasco já num fundo claro.)

## Exemplo C — Normalizar o catálogo
Entrada:
```
Tenho 40 fotos de produtos com fundos diferentes (mesa, parede, chão). Quero todas iguais
para a loja.
```
Saída:
```
Modo: normalizar catálogo

Padrão de catálogo (aplique o MESMO em todas as fotos, sem alterar cada produto):
- Fundo: branco puro e limpo
- Enquadramento: produto centralizado, ocupando ~80% da altura, margem igual em volta
- Base: todos alinhados na mesma linha de base (baseline)
- Sombra: contato leve e na mesma direção em todas
- Cor: white balance neutro, sem grading; cada produto mantém a cor real
- Proporção: 1:1

Instrução por foto (em inglês):
Edit the attached photo. Preserve the product pixel for pixel (shape, color, texture, label,
logo). Replace only the background with pure clean white, center the product at ~80% height
with even margins, align it to the same baseline, keep a light soft contact shadow, neutral
white balance. Square 1:1. Do not add new text, preserve existing product text exactly, no
added logo, no watermark.

Exceções para revisar à mão (saem do fluxo automático): itens de vidro/transparentes, com
pelo/pelúcia, muito reflexivos (metal espelhado), com rótulo complexo, ou fotos de baixa
resolução.
```

> Referência: o produto é preservado pixel a pixel; a sombra é decidida (preservada, não
> inventada); vidro/pelo/reflexo viram exceção sinalizada; e o maior valor costuma ser
> padronizar o catálogo inteiro no mesmo fundo — sem mudar cada SKU.
