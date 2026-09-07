---
name: estrutura-de-campanha
description: Monta a estrutura de uma conta de Google Ads — campanhas e grupos de anúncios organizados por tema e intenção — a partir do catálogo e do objetivo da loja. Use antes de criar os anúncios, para o dinheiro não se misturar e cada grupo falar com uma busca só.
---

# Estrutura de Campanha e Grupos de Anúncios

## O que faz
Desenha o esqueleto da conta antes de escrever qualquer anúncio: quais campanhas criar, quais grupos de anúncios dentro de cada uma, e por que separar assim. Cada grupo fica com um tema único e uma intenção clara, para que o texto do anúncio e a palavra-chave conversem — o que melhora o índice de qualidade e barateia o clique.

## Quando usar
- Ao abrir uma conta nova de Google Ads ou reorganizar uma bagunçada.
- Ao entrar com uma nova linha de produtos que precisa de campanha própria.
- Antes de escrever títulos e palavras-chave — a estrutura vem primeiro.

## O que a IA precisa de você
- `[catálogo]` — categorias e principais produtos da loja.
- `[objetivo]` — o que a campanha precisa entregar (vender X, girar categoria Y, capturar marca).
- `[orçamento aproximado]` (opcional) — para sugerir quantas campanhas fazem sentido começar.
- `[marca]` — o nome da loja (para separar a campanha de marca).
- `[termos que trazem prejuízo]` (opcional) — buscas que a loja não quer pagar.

## Instruções (o cérebro da skill)
1. Separe por **intenção**, não só por produto. As camadas típicas:
   - **Campanha de Marca** — quem já busca o nome da loja. Barata, protege o topo do resultado.
   - **Campanhas de Categoria/Genéricas** — quem busca o tipo de produto sem citar a loja. É onde está o volume e o custo.
   - **Campanha de Produto específico** — para carros-chefe com busca própria e margem que justifica.
2. Dentro de cada campanha, quebre em **grupos de anúncios por tema fechado**: cada grupo reúne palavras-chave que pedem o mesmo anúncio. Um grupo = uma ideia = um conjunto de títulos. Não misture "tênis de corrida" com "tênis casual" no mesmo grupo.
3. Para cada grupo, entregue: **nome do grupo**, **intenção** (marca / comercial / genérica), **tema das palavras-chave** que vão dentro, e **o ângulo do anúncio** que aquele grupo pede.
4. Aponte **onde entram palavras negativas entre campanhas** (ex.: negativar o nome da marca nas campanhas genéricas para não competir consigo mesma; negativar termos informacionais em campanha de venda).
5. Sugira uma **ordem de prioridade** de lançamento conforme o `[objetivo]` e o `[orçamento aproximado]` — começar por onde o retorno é mais provável, não tudo de uma vez.
6. Se um dado necessário não foi informado (margem, produto campeão, orçamento), marque `[preencher]` em vez de assumir.

## Regras de qualidade
- Estrutura enxuta. Não crie 20 campanhas onde 3 resolvem — conta espalhada dilui o orçamento e o aprendizado.
- Cada grupo com tema fechado o suficiente para um único conjunto de títulos servir bem.
- Sem prometer CPA, ROAS ou posição — a skill organiza, não garante resultado.
- Recomendação honesta: se o orçamento é pequeno, diga para concentrar, não para pulverizar.

## Formato da saída
Uma árvore legível: **Campanha → Grupos de anúncios**, cada grupo com intenção, tema de palavras-chave e ângulo do anúncio. Depois, um bloco **Palavras negativas entre campanhas** e um bloco **Ordem de prioridade** com a justificativa curta de cada passo.

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
