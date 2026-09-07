---
name: prompt-mockup-embalagem
description: Monta um prompt de imagem em inglês para um mockup realista da embalagem ou rótulo do produto (caixa, pote, frasco, sachê, tubo). Use para mostrar como o produto se apresenta na prateleira ou na foto do anúncio, sem produzir embalagem física.
---

# Prompt de Mockup de Embalagem

## O que faz
Gera um prompt pronto para uma IA de imagem que cria um mockup realista da sua embalagem — a caixa, o pote, o frasco, o sachê ou o rótulo, com material, acabamento e luz de estúdio. Serve para visualizar o produto "de verdade" antes de imprimir, ou para ter uma imagem de apresentação. Instruções em português; **o prompt final sai em inglês**.

## Quando usar
- Quer ver como a embalagem fica antes de mandar imprimir.
- Precisa de uma imagem de apresentação do produto embalado.
- Vai testar formatos ou acabamentos (fosco x brilhante) antes de decidir.

## O que a IA precisa de você
- `[tipo de embalagem]` — caixa, pote, frasco, sachê, tubo, bisnaga, lata, com tamanho.
- `[material e acabamento]` — papelão kraft, plástico brilhante, vidro âmbar, rótulo fosco, etc.
- `[nome da marca]` (opcional) — o nome real, se você quer que apareça no rótulo.
- `[o que o rótulo mostra]` — só o que você informar. Composição, tabela nutricional, registro, alegações: **não inventar** → `[preencher]`.
- `[proporção]` (opcional) — 1:1 ou 4:5.

## Instruções (o cérebro da skill)
Monte **um prompt em inglês** com estes blocos. Descreva o formato e o material com fidelidade; **nunca escreva no rótulo alegação, composição, número de registro ou selo que o lojista não forneceu**.

1. **Objeto (subject):** o tipo de embalagem, tamanho, material e acabamento reais — `a matte kraft cardboard box`, `an amber glass jar with a matte label`.
2. **Rótulo (label):** se o lojista deu o nome da marca, `clean minimal label showing the brand name "[nome]"`. Sem dado do lojista, use `blank placeholder label area, no invented text` — a arte final do rótulo entra depois.
3. **Ângulo (angle):** `hero 3/4 angle at eye level`, embalagem em pé, uma unidade (ou o pedido).
4. **Luz (light):** `soft studio softbox lighting, gentle reflection, subtle shadow`.
5. **Fundo (background):** neutro ou superfície discreta que combine (`on a clean surface, seamless soft background`).
6. **Estilo + proporção:** `realistic product packaging mockup, high detail, photorealistic, sharp focus`, e `aspect ratio 1:1 --ar 1:1` (ou o pedido).

Feche com as travas: `no invented claims, no fake nutrition facts, no watermark`.

## Regras de qualidade
- **Nunca inventar o que vai no rótulo**: composição, tabela nutricional, número de registro (Anvisa/MAPA), peso, alegação de saúde. Se o lojista não deu, deixa área em branco e marca `[preencher]`.
- Formato e material fiéis ao produto real.
- Sem selo de "aprovado", "nº 1", prêmio ou qualquer alegação não comprovada dentro da arte.
- Texto que a IA gera em rótulo costuma sair torto/errado — prefira nome curto ou área em branco, e finalize o rótulo no editor.
- A embalagem é da marca do lojista; nenhuma identidade da Performa entra.

## Formato da saída
1. **O prompt em inglês**, em bloco de código, pronto para colar.
2. **2 variações** de ângulo ou acabamento (ex.: fosco x brilhante, uma unidade x conjunto).
3. Uma linha em português avisando que composição/registro/alegações e a arte fina do rótulo se resolvem no editor, com dados reais — a IA não inventa.

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
