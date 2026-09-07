---
name: auditoria-pagina-de-produto
description: Audita uma página de produto por um checklist guiado (título, fotos, prova, preço, botão, frete, objeções) e devolve melhorias em ordem de impacto. Use quando um produto recebe visitas mas converte pouco, ou antes de investir em tráfego para essa página.
---

# Auditoria de Página de Produto

## O que faz
Passa a página de produto por um checklist de conversão, item por item, e devolve um diagnóstico com as melhorias que mais destravam venda primeiro. Não reescreve a página: aponta o que corrigir, por que aquilo trava a compra e como arrumar — para o lojista decidir a ordem de execução.

## Quando usar
- Um produto tem tráfego, mas a taxa de conversão dele está abaixo do resto da loja.
- Antes de colocar dinheiro de anúncio numa página específica (não vale pagar para levar gente a uma página que não converte).
- Ao padronizar as páginas do catálogo depois de encontrar um modelo que vende bem.

## O que a IA precisa de você
- `[link ou conteúdo da página]` — cole o texto do produto: título, descrição, bullets, specs. Se puder, descreva as fotos (quantas, o que mostram) e o vídeo.
- `[produto e público]` — o que é e para quem vende.
- `[preço e condições]` — preço, parcelamento, frete e prazo reais. Se não souber informar agora, deixe `[preencher]`.
- `[prova social disponível]` — avaliações, número de vendas, depoimentos, selos que a loja realmente tem.
- `[dúvidas do atendimento]` (opcional) — perguntas que mais chegam antes da compra.

## Instruções (o cérebro da skill)
Avalie a página nos **9 pontos** abaixo, nesta ordem. Para cada ponto, dê um status (OK / Ajustar / Falta), uma frase do porquê e a recomendação concreta.

1. **Título** — diz o benefício e o que é, com o termo que a pessoa busca? Ou é só código/nome interno?
2. **Fotos e vídeo** — mostram o produto em uso, escala, detalhe e variações? Fundo limpo? Dá para ampliar? Foto fraca é o item que mais derruba conversão — priorize.
3. **Primeira dobra** — nos primeiros segundos a pessoa vê nome, preço, foto principal e botão de compra sem rolar?
4. **Descrição e bullets** — começam pelo benefício antes da característica? Escaneável no celular?
5. **Prova social** — a página exibe a prova que a loja tem, de forma honesta? (avaliações, vendas, depoimentos). Nunca recomende inventar número; se não há prova, sugira como começar a coletar.
6. **Preço e condições** — preço claro, parcelamento visível, frete e prazo fáceis de achar? Custo escondido é motivo nº 1 de abandono.
7. **Botão de compra (CTA)** — texto claro ("Comprar agora"), cor de destaque, visível sem rolar e repetido ao longo da página?
8. **Objeções** — a página responde as dúvidas que travam a compra (tamanho, garantia, troca, compatibilidade)? Cruze com as `[dúvidas do atendimento]`.
9. **Confiança e segurança** — selo de compra segura, política de troca visível, canal de contato? Reduz o medo de comprar de quem não conhece a loja.

Depois de avaliar os 9 pontos, monte a **lista priorizada**: ordene as correções por impacto na conversão × esforço. O que é fácil e destrava muito vem primeiro.

## Regras de qualidade
- Priorize por impacto real, não por quantidade de achados. Melhor 3 correções que importam do que 20 cosméticas.
- Nunca mande inventar avaliação, número de vendas ou depoimento. Se falta prova, o caminho é coletar, não fabricar.
- Não invente preço, frete, prazo ou política — se o dado não veio, marque `[preencher]` na recomendação.
- Recomendação concreta e acionável ("troque o título X por um que diga o benefício"), não conselho genérico.
- Aponte também o que já está bom — a auditoria confirma acertos, não só procura erro.

## Formato da saída
1. **Resumo** (2–3 linhas): o estado geral da página e a maior alavanca de conversão.
2. **Tabela dos 9 pontos**: Ponto | Status | Observação | O que fazer.
3. **Plano priorizado**: lista numerada das correções, da que mais destrava para a que menos, com esforço estimado (baixo/médio/alto).

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
