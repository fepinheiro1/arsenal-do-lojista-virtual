---
name: titulos-e-descricoes
description: Gera títulos (até 30 caracteres) e descrições (até 90 caracteres) para um anúncio responsivo da Rede de Pesquisa do Google, cada um com a contagem de caracteres ao lado. Use ao montar um anúncio de Search novo ou renovar um que já roda.
---

# Títulos e Descrições (Rede de Pesquisa)

## O que faz
Escreve o texto de um anúncio responsivo de Pesquisa (RSA): um conjunto de títulos e descrições que o Google combina na hora da busca. Cada linha já vem com a contagem de caracteres, dentro dos limites do Google, começando pelo benefício e usando a palavra-chave que a pessoa digitou.

## Quando usar
- Ao criar um anúncio de Search para um produto, categoria ou promoção real.
- Ao renovar um anúncio que está com baixo índice de qualidade ou CTR fraco.
- Ao gerar variações para testar títulos diferentes no mesmo grupo de anúncios.

## O que a IA precisa de você
- `[produto ou oferta]` — o que está sendo anunciado.
- `[palavra-chave principal]` — o termo que a pessoa digita (ex.: "tênis de corrida masculino").
- `[público]` — para quem o anúncio fala.
- `[diferenciais reais]` — frete, prazo, garantia, condições (só o que existe de verdade).
- `[tom da marca]` — como a loja fala.
- `[URL de destino]` (opcional) — para sugerir os caminhos de exibição.

## Instruções (o cérebro da skill)
Gere o texto de um anúncio responsivo respeitando os limites do Google Ads. **Conte os caracteres de cada linha** (espaços contam) e mostre a contagem entre parênteses no fim de cada uma.

1. **15 títulos, até 30 caracteres cada.** Ordene por força e varie o ângulo:
   - 3–4 com a `[palavra-chave principal]` (para casar com a busca).
   - 3–4 com o benefício central (o ganho para a pessoa).
   - 2–3 com um diferencial real informado (frete, prazo, garantia) — nunca inventado.
   - 2–3 com um convite objetivo à ação ("Peça o seu", "Veja os modelos").
   - 1–2 com a marca da loja, se fizer sentido.
2. **4 descrições, até 90 caracteres cada.** Cada uma: benefício primeiro, depois a característica ou condição que o sustenta. Uma delas pode reforçar um diferencial real.
3. **2 caminhos de exibição, até 15 caracteres cada** (a parte depois do domínio, ex.: `/tenis-corrida`). Use a categoria ou o termo, não invente uma promoção.
4. Não repita a mesma ideia em títulos diferentes — o Google precisa de variedade para combinar.
5. Se um diferencial não foi informado (prazo, desconto, condição), **não invente**: marque `[preencher]` no lugar para o lojista completar.

## Regras de qualidade
- Benefício antes de característica.
- Sem "melhor do mundo", "imperdível", "última chance", "explosão de vendas" ou garantia de resultado.
- Sem urgência ou escassez falsa. Contagem regressiva e "só hoje" só entram se forem verdade e informados pelo lojista.
- Todo título e descrição **dentro do limite** — 30 e 90 caracteres. Linha que estourar precisa ser reescrita, não cortada no meio.
- A copy é da marca do lojista, no `[tom da marca]` informado.
- Sem emojis (a Rede de Pesquisa não os exibe de forma confiável e o Google pode reprovar).

## Formato da saída
Três blocos rotulados — **Títulos (até 30)**, **Descrições (até 90)** e **Caminhos (até 15)** — cada linha numerada com a contagem de caracteres entre parênteses. No fim, uma linha avisando se algo ficou marcado como `[preencher]`.

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
