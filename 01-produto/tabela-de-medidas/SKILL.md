---
name: tabela-de-medidas
description: Monta um guia de tamanhos claro e uma orientação de "como medir" para produtos com numeração, reduzindo troca e devolução. Use em moda, calçados, cama e qualquer item com variação de tamanho.
---

# Tabela de Medidas

## O que faz
Organiza as medidas do produto numa tabela fácil de ler e escreve o passo a passo de "como se medir" — o que reduz a dúvida na hora da compra e a troca por tamanho errado depois.

## Quando usar
- Roupas, calçados, roupa de cama, anéis — qualquer produto com tamanho.
- Quando a troca por numeração está alta.

## O que a IA precisa de você
- `[produto]` — o que é.
- `[medidas por tamanho]` — os números que você tem (ex.: P/M/G com busto, cintura, quadril; ou 34–44 com comprimento do pé).
- `[modelagem]` (opcional) — se veste justo, solto, no ponto.

## Instruções (o cérebro da skill)
1. Organize as medidas numa tabela: uma linha por tamanho, uma coluna por medida.
2. Escreva um bloco curto **"Como medir"**, com o passo a passo para cada medida usada (ex.: "Busto: passe a fita na parte mais larga, sem apertar").
3. Se houver `[modelagem]`, adicione a dica: "Se você fica entre dois tamanhos, [modelagem]...".
4. Feche com a orientação de "na dúvida entre dois, escolha o maior/menor" conforme a peça.

## Regras de qualidade
- Não invente medida que você não passou — use só os números fornecidos.
- Unidade sempre visível (cm, mm).
- Linguagem de quem orienta, não de manual técnico.

## Formato da saída
Tabela em markdown + bloco "Como medir" + dica de escolha entre tamanhos.

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
