# Prompt de Troca de Fundo — exemplos ilustrativos

> Casos de demonstração: a instrução só usa o que veio na entrada — o que a entrada não diz (a sombra original, o tamanho de cada item) não é presumido.

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
(A sombra real, que você disse ser boa, foi preservada e limpa — não inventei uma nova.)
Atenção: calçado tem regra própria de imagem principal na Amazon (posição e quantidade de
pés, por exemplo) — confira a regra vigente da sua categoria antes de subir.

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
and the printed label exactly. Replace only the surrounding background. If the original photo
has a clean contact shadow, keep a soft version of it; if it has none, do not invent one.
Precise edges with no halo. Do not add new text, preserve existing label text exactly, no
added logo, no watermark.
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
- Enquadramento: produto centralizado, com a mesma margem em volta. Dentro de uma mesma
  família (ex.: canecas de 300 e 500 ml), escala coerente entre si — a menor não é ampliada
  para parecer do tamanho da maior.
- Base: todos alinhados na mesma linha de base (baseline)
- Sombra: decidida foto a foto — a sombra real de contato é preservada e limpa quando é boa;
  onde falta ou está ruim, uma sombra de contato leve, na mesma direção do resto. Nunca
  sombra projetada inventada.
- Cor: white balance neutro, sem grading; cada produto mantém a cor real
- Proporção: 1:1

Instrução por foto (em inglês):
Edit the attached photo. Preserve the product pixel for pixel (shape, color, texture, label,
logo) and do not resize it relative to other items of the same product family. Replace only
the background with pure clean white, center the product with even margins, align it to the
same baseline. If the original contact shadow is clean, keep a soft version of it; if it is
missing or messy, add only a light soft contact shadow under the base, same direction as the
rest of the catalog. Neutral white balance. Square 1:1. Do not add new text, preserve existing
product text exactly, no added logo, no watermark.

Exceções para revisar à mão (saem do fluxo automático): itens de vidro/transparentes, com
pelo/pelúcia, muito reflexivos (metal espelhado), com rótulo complexo, ou fotos de baixa
resolução.

Conferência: ao final, confira se saíram as 40 imagens, cada uma com o mesmo nome de
arquivo/SKU da original — nenhuma trocada, nenhuma faltando.
```

> Referência: o produto é preservado pixel a pixel; a sombra é decidida foto a foto
> (preservada quando boa, nunca inventada por padrão); padronizar não faz itens de tamanhos
> diferentes parecerem iguais; vidro/pelo/reflexo viram exceção sinalizada; e o lote é
> conferido no fim — sem mudar cada SKU.
