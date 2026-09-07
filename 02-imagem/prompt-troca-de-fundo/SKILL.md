---
name: prompt-troca-de-fundo
description: Monta um prompt de edição em inglês para remover ou trocar o fundo de uma foto de produto que o lojista já tem, mantendo o produto intacto. Use quando a foto é boa mas o fundo é poluído, escuro ou fora do padrão do marketplace.
---

# Prompt de Troca de Fundo

## O que faz
Gera um prompt de **edição** (não de criação do zero) para uma IA que edita imagem a partir de uma foto sua — Nano Banana/Gemini, preenchimento generativo do Photoshop, ou uma ferramenta de remoção de fundo. Ele instrui a IA a manter o produto exatamente como está e trocar só o fundo: branco limpo para marketplace, ou uma cena para dar contexto. Instruções em português; **o prompt final sai em inglês**.

## Quando usar
- A foto do produto é boa, mas o fundo é bagunçado, escuro ou não bate com o padrão do marketplace.
- Você quer padronizar todo o catálogo no mesmo fundo.
- Precisa de uma versão em cena (lifestyle) a partir de uma foto que já tem.

> Requer uma IA que **edita** a sua imagem (você anexa a foto). Não serve para modelo que
> só cria do zero sem receber a imagem.

## O que a IA precisa de você
- `[foto do produto]` — a imagem que você já tem (anexada na IA de edição).
- `[produto]` — o que é, para a IA saber o que preservar.
- `[novo fundo]` — branco puro / cinza-claro / gradiente / cena específica (ex.: "bancada de mármore").
- `[objetivo]` — marketplace (fundo neutro) ou social (fundo com contexto).
- `[proporção]` (opcional) — manter a original ou ajustar (1:1, 4:5).

## Instruções (o cérebro da skill)
Monte **um prompt de edição em inglês** com estes blocos. O produto é intocável; só o fundo muda.

1. **Preservar o produto (preserve):** primeiro e mais importante — `keep the product exactly as it is, do not alter its shape, color, texture or details`.
2. **Trocar o fundo (replace):** `remove the current background and replace it with [novo fundo]`.
3. **Integração de luz e sombra (blend):** `match the lighting direction of the product and add a soft realistic contact shadow beneath it` — é o que evita o efeito recorte colado.
4. **Bordas limpas (edges):** `clean, precise edges around the product, no halo, no leftover background`.
5. **Proporção (aspect ratio):** manter a original ou `aspect ratio 1:1` conforme o objetivo.

Feche com as travas: `no text, no logo, no watermark, photorealistic result`.

## Regras de qualidade
- O produto não muda. Se a IA "melhorar" a cor ou o formato, a foto passa a mentir sobre a entrega — rejeite o resultado.
- Sombra de contato e luz coerentes: sem isso, o produto parece flutuando/recortado.
- Fundo branco para marketplace = branco realmente limpo, sem sujeira nem gradiente forte.
- A imagem é da loja do lojista; nenhum elemento da Performa entra.

## Formato da saída
1. **O prompt de edição em inglês**, em bloco de código, pronto para colar na IA que recebe a sua foto.
2. **2 variações** de fundo (ex.: uma versão branca de marketplace e uma versão em cena).
3. Uma linha em português lembrando de anexar a foto original e de conferir se o produto ficou idêntico ao real.

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
