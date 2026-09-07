---
name: copy-performance-max
description: Gera o conjunto completo de assets de texto de uma campanha Performance Max — títulos (até 30), títulos longos (até 90), descrições (até 90, a curta até 60) e nome da empresa (até 25) — cada um com a contagem de caracteres. Use ao montar ou reforçar um grupo de recursos do PMax.
---

# Copy para Performance Max

## O que faz
Escreve todos os textos que o Performance Max combina automaticamente entre os canais do Google (Pesquisa, Display, YouTube, Gmail, Discover). Como o PMax mistura os assets sozinho, cada linha precisa fazer sentido isolada e caber no limite. A skill entrega o conjunto inteiro, variado e dentro das regras, com a contagem de caracteres em cada item.

## Quando usar
- Ao criar um grupo de recursos (asset group) novo em uma campanha Performance Max.
- Ao reforçar uma campanha com "força do anúncio" baixa por falta de variedade de texto.
- Ao adaptar a copy de um tema/coleção específica dentro do PMax.

## O que a IA precisa de você
- `[produto ou coleção]` — o que o grupo de recursos promove.
- `[público]` — para quem fala.
- `[benefícios e diferenciais reais]` — o que sustenta a copy (frete, garantia, condições — só o que existe).
- `[palavras-chave / temas]` — os termos que o público associa ao produto.
- `[nome da empresa]` — a marca, para o campo próprio (até 25 caracteres).
- `[tom da marca]` — como a loja fala.

## Instruções (o cérebro da skill)
Gere o conjunto completo respeitando os limites do Performance Max. **Conte os caracteres de cada linha** (espaços contam) e mostre a contagem entre parênteses.

1. **15 títulos, até 30 caracteres cada.** Variados: com palavra-chave, com benefício, com diferencial real, com convite à ação. Cada um se sustenta sozinho — o PMax os combina fora de ordem.
2. **5 títulos longos, até 90 caracteres cada.** Mais espaço para juntar benefício + prova ou benefício + condição real. Não repita o que já está nos títulos curtos.
3. **Descrições:**
   - **1 descrição curta, até 60 caracteres** (o PMax usa uma versão curta em alguns espaços).
   - **4 descrições, até 90 caracteres cada.** Benefício primeiro, característica depois.
4. **Nome da empresa, até 25 caracteres** — a marca informada, sem slogan.
5. Sugira **1 chamada para ação** entre as opções que o Google oferece (ex.: Comprar, Saiba mais, Ver mais) — a que combina com a etapa do público.
6. Cubra ângulos diferentes entre os itens (economia de tempo, qualidade, condição de compra, adequação ao público) para o PMax ter material com que trabalhar.
7. Diferencial não informado (prazo, desconto, número de vendas) vira `[preencher]` — nunca é inventado.

## Regras de qualidade
- Benefício antes de característica. Frases curtas.
- Sem "melhor do mundo", "imperdível", "última chance", "explosão de vendas" ou garantia de resultado.
- Sem urgência ou escassez falsa; oferta só aparece se for real e informada.
- Todo item **dentro do limite** — 30, 90, 60 e 25 caracteres conforme o campo. O que estourar é reescrito, não cortado.
- Variedade real: assets parecidos demais derrubam a força do anúncio e não ajudam o PMax.
- Copy no `[tom da marca]` do lojista. Sem emojis.

## Formato da saída
Cinco blocos rotulados — **Títulos (até 30)**, **Títulos longos (até 90)**, **Descrição curta (até 60)**, **Descrições (até 90)** e **Nome da empresa (até 25)** — cada linha numerada com a contagem entre parênteses. Depois, a **Chamada para ação** sugerida e um aviso se algo ficou como `[preencher]`.

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
