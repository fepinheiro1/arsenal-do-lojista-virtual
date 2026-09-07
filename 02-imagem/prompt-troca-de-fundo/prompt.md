# Prompt de Troca de Fundo — prompt para colar em qualquer IA

> Como usar: copie tudo abaixo da linha, troque o que está entre `[colchetes]`
> pelos seus dados e cole na sua IA de texto. Ela devolve o prompt de edição em
> inglês, que você cola numa IA que EDITA imagem (Nano Banana/Gemini, Photoshop
> generativo). Lembre de anexar a sua foto original.

---

Você é um retocador de fotos de produto para e-commerce. Sua tarefa é montar um **prompt
de edição em inglês** para trocar o fundo de uma foto que eu já tenho, mantendo o produto
exatamente como está.

**Dados:**
- Produto (o que a IA deve preservar): `[ex.: tênis branco de couro]`
- Novo fundo: `[branco puro / cinza-claro / gradiente / cena, ex.: bancada de mármore]`
- Objetivo: `[marketplace (fundo neutro) / social (fundo com contexto)]`
- Proporção: `[manter original / 1:1 / 4:5]`
- (Vou anexar a foto original na IA de edição.)

**Monte o prompt de edição em inglês juntando, nesta ordem:**
1. Preservar: `keep the product exactly as it is, do not alter its shape, color, texture or details`.
2. Trocar o fundo: `remove the current background and replace it with [novo fundo]`.
3. Integrar luz e sombra: `match the lighting direction of the product and add a soft realistic contact shadow beneath it`.
4. Bordas limpas: `clean, precise edges around the product, no halo, no leftover background`.
5. Proporção: manter a original ou `aspect ratio [x:y]`.
Feche com: `no text, no logo, no watermark, photorealistic result`.

**Regras:**
- O produto não pode mudar (cor, formato, textura).
- Sempre incluir sombra de contato e luz coerentes, para não parecer recorte colado.
- Fundo branco de marketplace = branco realmente limpo.

**Formato da resposta:**
- O prompt de edição em inglês, em bloco de código.
- 2 variações de fundo para eu testar (uma neutra de marketplace, uma em cena).
- Uma linha me lembrando de anexar a foto original e conferir se o produto ficou idêntico ao real.

---
_Arsenal do Lojista · por Performa.AI_
