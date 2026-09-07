---
name: pesquisa-de-palavras-chave
description: Monta uma lista de palavras-chave para Google Ads separada por intenção de busca, com o tipo de correspondência sugerido para cada uma e uma lista de palavras negativas. Use ao planejar um grupo de anúncios ou limpar o desperdício de uma campanha que gasta sem vender.
---

# Pesquisa de Palavras-chave

## O que faz
Traduz o que a loja vende em termos que as pessoas realmente digitam, organizados pela intenção por trás de cada busca — de quem só pesquisa a quem está pronto para comprar. Para cada palavra, sugere o tipo de correspondência (ampla, de frase ou exata) e entrega uma lista de palavras negativas para cortar o clique que não vira venda.

## Quando usar
- Ao planejar as palavras-chave de um grupo de anúncios novo.
- Ao limpar uma campanha que gasta muito e converte pouco (faltam negativas).
- Ao descobrir termos de cauda longa mais baratos para um produto específico.

## O que a IA precisa de você
- `[produto ou categoria]` — o que a loja quer anunciar.
- `[público e região]` — para quem e onde vende.
- `[termos que a loja NÃO atende]` — o que gera clique errado (aluguel, usado, conserto, atacado...).
- `[marca]` (opcional) — para separar buscas de marca das genéricas.

## Instruções (o cérebro da skill)
1. Gere as palavras-chave e agrupe por **intenção de busca**:
   - **Transacional / pronto para comprar** — "comprar", "preço", "loja", nome do produto + cidade. Maior prioridade.
   - **Comercial / comparando** — "melhor", "qual", "review", "vale a pena". Está decidindo.
   - **Informacional / pesquisando** — "como", "para que serve", "diferença entre". Ainda não compra; use com cautela (ou só para conteúdo).
   - **De marca** — o nome da loja e variações, se informado.
2. Para **cada palavra**, sugira o **tipo de correspondência**:
   - **Exata** `[palavra]` — para os termos mais valiosos e certeiros, onde você quer controle total.
   - **De frase** `"palavra"` — para pegar variações mantendo a ordem e o sentido.
   - **Ampla** `palavra` — só para descobrir termos novos, e sempre acompanhada de lances inteligentes e monitoramento; alerte o lojista que ampla gasta mais rápido.
   Explique em uma linha por que aquele tipo para aquele termo.
3. Priorize **cauda longa** (3+ palavras): converte melhor e o clique costuma sair mais barato.
4. Monte a **lista de palavras negativas** a partir dos `[termos que a loja NÃO atende]` e das buscas informacionais que só gastam sem vender. Separe negativas óbvias (grátis, usado, download, emprego) das específicas da loja.
5. Não invente volume de busca nem CPC — se o lojista quiser números, oriente conferir no Planejador de Palavras-chave do Google. Marque como estimativa qualquer prioridade sugerida.

## Regras de qualidade
- Intenção antes de volume: 10 termos certeiros valem mais que 100 genéricos.
- Toda palavra ampla vem com aviso de monitorar e uma boa lista de negativas por perto.
- Não prometa posição nem custo por clique — a skill organiza e prioriza, não garante número.
- Sem inventar dado de volume/CPC; direcione ao Planejador do Google quando pedirem números.

## Formato da saída
Uma tabela por intenção com colunas **Palavra-chave | Correspondência | Por quê**, da intenção mais quente para a mais fria. Depois, dois blocos de **Palavras negativas**: "óbvias" e "específicas desta loja".

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
