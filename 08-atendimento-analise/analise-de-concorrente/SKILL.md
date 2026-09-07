---
name: analise-de-concorrente
description: Guia a IA a analisar um concorrente de e-commerce — sortimento, preço, posicionamento, pontos fortes e fracos — e devolver o que dá para aprender e aplicar na sua loja. Use ao estudar um concorrente novo, entender por que ele vende ou decidir onde a sua loja pode se diferenciar.
---

# Análise de Concorrente

## O que faz
Organiza o que você observou de um concorrente num diagnóstico claro: o que ele vende, como precifica, como se posiciona, o que faz bem e onde deixa brecha. Fecha com um plano curto de "o que aprender" e "onde nos diferenciar" — voltado para a decisão, não para copiar.

## Quando usar
- Ao mapear um concorrente novo ou um que passou a aparecer no seu mercado.
- Antes de decidir preço, sortimento ou posicionamento.
- Para achar a brecha onde a sua loja pode se destacar em vez de brigar de igual para igual.

## O que a IA precisa de você
- `[concorrente]` — nome e link, se tiver.
- `[o que você observou]` — cole o que viu: produtos, faixas de preço, frete, textos do site, redes, avaliações, prazos. Quanto mais concreto, melhor.
- `[sua loja]` — o que você vende e para quem.
- `[seu objetivo]` — o que você quer decidir com essa análise (preço? entrar numa categoria? mudar o posicionamento?).

## Instruções (o cérebro da skill)
Trabalhe **somente com o que o lojista observou**. Onde faltar dado, marque `[preencher]` ou classifique como "não observado" — nunca preencha com suposição apresentada como fato.

Estruture o diagnóstico em 6 blocos:

1. **Sortimento** — o que o concorrente vende, amplitude e profundidade, categorias em que aposta e o que claramente não cobre.
2. **Preço** — faixa observada, onde parece barato/caro, sinais de estratégia (isca, premium, kits, frete embutido). Compare com a sua loja quando o dado existir.
3. **Posicionamento** — para quem ele fala e como (linguagem, promessa, provas que usa). Uma frase que resume o posicionamento dele.
4. **Pontos fortes** — o que ele faz bem e por que isso atrai o cliente.
5. **Pontos fracos / brechas** — onde ele deixa a desejar (atendimento, prazo, informação do produto, experiência). Cada brecha é uma oportunidade sua.
6. **O que fazer** — 3 a 5 recomendações ligadas ao `[seu objetivo]`, separando **o que aprender com ele** (adaptar, nunca copiar) de **onde se diferenciar** (o espaço que ele deixou aberto).

## Regras de qualidade
- Só afirme o que foi observado. Sem inventar número de vendas, faturamento, avaliações ou preço não visto — marque `[preencher]`.
- Diferencie fato ("o site anuncia frete grátis acima de R$X") de leitura ("parece mirar público premium") — deixe claro o que é cada um.
- Nunca criar copy que critica ou difama o concorrente. A análise é interna, para decisão.
- Recomende adaptar e se diferenciar, não copiar.
- Foco na decisão do lojista, não num relatório longo por vaidade.

## Formato da saída
Diagnóstico com os 6 blocos acima (títulos curtos), seguido de:
- **Resumo em 1 frase**: como esse concorrente se posiciona.
- **Quadro final "Aprender × Diferenciar"**: duas colunas curtas com as ações priorizadas.
- Lista dos `[preencher]` / itens não observados que valem a pena checar depois.

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
