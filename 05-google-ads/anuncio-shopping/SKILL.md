---
name: anuncio-shopping
description: Otimiza o título e a descrição de um produto no feed do Google Shopping para ele aparecer nas buscas certas, com os atributos na ordem que o Google lê primeiro e a contagem de caracteres. Use ao cadastrar ou revisar produtos no Merchant Center.
---

# Anúncio de Shopping (feed do Merchant Center)

## O que faz
No Shopping, quem escreve o anúncio é o feed do produto — não há título e descrição digitados como no Search. O que faz o produto aparecer e ser clicado é como o **título** e a **descrição** do feed estão montados. A skill reescreve os dois com os atributos que o comprador digita, na ordem que o Google lê, para casar com mais buscas relevantes.

## Quando usar
- Ao cadastrar produtos no Google Merchant Center pela primeira vez.
- Ao revisar um feed com produtos que aparecem pouco ou em buscas erradas.
- Ao padronizar o título de um catálogo inteiro numa fórmula consistente.

## O que a IA precisa de você
- `[produto]` — nome e o que é.
- `[atributos]` — marca, tipo de produto, gênero, cor, tamanho/numeração, material, modelo, medida ou capacidade — o que existir.
- `[como o cliente busca]` — o termo que a pessoa digita (ex.: "tênis de corrida masculino preto").
- `[categoria]` — a categoria do produto na loja.
- `[dados de política]` (opcional) — garantia, conteúdo da embalagem, cuidados.

## Instruções (o cérebro da skill)
1. **Título do feed** — monte na fórmula que o Google lê da esquerda para a direita, do mais importante ao menos:
   `Marca + Tipo de produto + Atributos-chave (gênero, cor, tamanho, material, modelo)`.
   - Ponha na frente o que o cliente digita: o Google dá mais peso às primeiras palavras, e cerca dos **primeiros ~70 caracteres** é o que aparece na maioria das telas.
   - Limite técnico do título: **150 caracteres**. Preencha com atributos úteis, sem empilhar palavra-chave repetida.
   - Sem MAIÚSCULAS gritadas, sem texto promocional ("promoção", "frete grátis") — o Google reprova no título.
2. **Descrição do feed** — 1 a 3 parágrafos curtos: benefício de uso primeiro, depois os atributos e as especificações que ajudam a busca e a decisão. Limite técnico de **5.000 caracteres**, mas o essencial nos primeiros ~500. Repita naturalmente os atributos importantes (cor, material, uso).
3. Mostre a **contagem de caracteres** do título e informe quanto dele cabe nos primeiros ~70 visíveis.
4. Nunca invente atributo (material, medida, gênero, garantia). Faltou dado? Marque `[preencher]` — feed com informação errada gera reprovação e devolução.
5. Ofereça **2 variações de título** com ordem de atributos diferente, para o lojista testar qual casa com mais buscas.

## Regras de qualidade
- O título descreve o produto com precisão — não é espaço de propaganda. Texto promocional é reprovado pelo Merchant Center.
- Atributo antes de adjetivo: "tênis de corrida masculino preto 42" vale mais que "incrível tênis super leve".
- Sem "melhor do mundo", "imperdível" ou garantia de resultado; sem urgência.
- Não inventar dado de composição, medida ou política — marcar `[preencher]`.
- A descrição é da marca do lojista, informativa e escaneável.

## Formato da saída
**Título otimizado** (com contagem de caracteres e nota de quanto cabe nos ~70 visíveis), **Descrição do feed** (parágrafos curtos) e **2 variações de título** para teste. Ao final, lista dos atributos marcados como `[preencher]`, se houver.

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
