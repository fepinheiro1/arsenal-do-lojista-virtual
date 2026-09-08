---
name: titulo-que-rankeia
description: Cria, otimiza e padroniza títulos de produto para e-commerce, adaptando naming, atributos, variantes e comprimento ao canal — loja própria, SEO, Google Merchant e marketplaces — com foco em clareza, busca e precisão factual. Aceita dados soltos, um título atual, uma URL ou um catálogo inteiro. Use ao cadastrar produtos, corrigir títulos fracos ou padronizar o catálogo.
---

# Título que Rankeia

## O que faz
Nomeia o produto do jeito certo para cada lugar onde ele aparece. Não existe um título único ideal para todos os canais — o nome na página (H1), o título de SEO, o do Google Merchant e o de cada marketplace seguem lógicas diferentes. A skill entende o produto, escolhe a ordem e os atributos que importam, e entrega o título recomendado — sem keyword stuffing e sem inventar atributo.

Regra de ouro: **simples na superfície, especialista por baixo.** O lojista informa o produto; a skill decide como ele deve ser nomeado.

## Quando usar
- Cadastrar um produto novo (a partir de dados soltos ou de uma ficha).
- Corrigir um título fraco, poluído ou cheio de palavra repetida.
- Preparar o título para um canal específico (loja, Google Shopping, Mercado Livre...).
- Padronizar um catálogo inteiro no mesmo padrão (modo em lote).

## O que a IA precisa de você
No mínimo, **uma** destas coisas:
- os **dados do produto** (marca, modelo, tipo, atributos — o que você tiver), ou
- um **título atual** para melhorar, ou
- uma **URL** do produto (se você tiver web disponível; se não, cole as informações), ou
- um **catálogo** (CSV/tabela com vários SKUs) para padronizar de uma vez.

Opcional (afina o resultado): canal de destino, palavra-chave alvo, variantes. Se você não disser o canal, a skill gera o título para a **loja própria** e, quando útil, oferece a versão para Google Merchant. Só pergunta 1–2 coisas quando a falta realmente impede um bom título.

## Como funciona (por baixo)

**1. Detecta o modo, sozinha.**
- **Criar** — recebeu dados → monta o título do zero.
- **Otimizar** — recebeu um título pronto ou URL → preserva os fatos, remove termo inútil, subjetivo e repetição, corrige a ordem e adequa ao canal.
- **Em lote** — recebeu vários SKUs → detecta o padrão atual, propõe um template por categoria, aplica e mantém os SKUs distinguíveis (sem duplicar).

**2. Um título não serve para todo canal.** A skill distingue:

| Objeto | Foco | Referência de tamanho |
|---|---|---|
| Nome / H1 da página | clareza na página do produto | curto e direto |
| SEO title | relevância + clique | ~50–60 caracteres (referência, não lei) |
| Google Merchant `title` | riqueza de informação no feed | até 150; o que importa nos primeiros ~70 |
| Merchant `short_title` | formatos visuais / mobile | curto (~até 65, muitas vezes < 40) |
| Marketplace | regra do canal | conferir a doc oficial vigente |

> Os limites de marketplace mudam com frequência. A skill usa essas referências como ponto de partida, mas prioriza **precisão e clareza sobre encaixar num número** — e, para um canal específico, confere a documentação oficial vigente antes de cravar um limite.

**3. Infere com segurança.** Categoria, marca/modelo, intenção de busca e palavra-chave, a partir do que recebeu. Palavra-chave explícita do lojista tem prioridade.

**4. Decide a ordem pelo contexto — não começa sempre pelo tipo.** Marca forte e modelo conhecido vêm na frente (*Nike Air Max 90*); marca fraca ou desconhecida cede a frente para o tipo (*Cafeteira Italiana Moka BrewCo Classic*). A ordem por categoria é referência, não fórmula cega:

| Categoria | Ordem de referência |
|---|---|
| Moda | tipo → marca → linha → gênero → material → cor → tamanho |
| Calçados | marca → modelo → tipo → uso → gênero → cor → tamanho |
| Eletrônicos | marca → modelo → tipo → capacidade → memória → tela → conectividade → cor |
| Beleza | marca → produto → função → ativo factual → volume → variante |
| Casa & móveis | tipo → marca → material → dimensões → cor → estilo |
| Alimentos | produto → marca → sabor → peso → quantidade → variante |
| Infantil | produto → marca → faixa etária → material → tamanho → variante |

**5. Escolhe os atributos — não joga tudo no título.** Para cada atributo pergunta: identifica o produto? casa com a busca? influencia a escolha? distingue a variante? é filtro comum? cabe sem sujar a clareza? Só entra o que passa. O essencial fica nos **primeiros ~70 caracteres** (continua compreensível se o canal truncar); o complementar vem depois.

**6. Trata variantes.** Cor, tamanho, voltagem, capacidade, sabor — em catálogo/feed, os SKUs precisam ser distinguíveis (*Camiseta Algodão Masculina Preta P* ≠ *... Preta M*). Nunca inventa valor de variante.

## Instruções (o cérebro da skill)
1. Identifique o **modo** (criar / otimizar / lote) e organize o que recebeu.
2. Classifique a **categoria** e infira **marca/modelo, intenção e palavra-chave**.
3. Decida a **ordem** pelo contexto (força da marca, categoria, canal) e **selecione os atributos** que passam no ranking.
4. Monte o título com o essencial nos primeiros ~70 caracteres.
5. Rode o **Quality Gate** (abaixo) e corrija antes de entregar.
6. Entregue **um título recomendado** com a contagem de caracteres. Alternativas só quando agregarem de verdade; multicanal só quando pedido.

## Regras de qualidade
- **Nunca invente** material, tecnologia, certificação, modelo, capacidade, compatibilidade, tamanho, origem, garantia, versão ou atributo. "Panela inox" não vira "Panela Inox 304 Profissional"; "resistente à água" não vira "impermeável".
- **Sem keyword stuffing**: nada de repetir tipo/marca, empilhar sinônimos ou singular+plural (*"Tênis Masculino Tênis Corrida Tênis Esportivo"* é proibido).
- **Sem promoção no título**, especialmente no Merchant: fora "frete grátis", "promoção", "50% OFF", "compre agora", "oferta", "mais barato", "última chance".
- **Dados conflitantes** (ex.: "128 GB" e "256 GB"): não escolha no silêncio — pergunte de forma curta qual é o certo.
- **Sem termo subjetivo vazio**: "confortável", "original", "top" não identificam o produto nem ajudam na busca; corte.
- No **modo em lote**, diferencie SKUs por um atributo real — não invente código interno só para forçar unicidade.

### Quality Gate (silencioso, antes de entregar)
Dá para entender o que é na hora? · Marca/modelo/tipo claros? · Corresponde ao jeito que a pessoa busca? · Os atributos importam? · Tudo é factual? · Respeita o canal? · O essencial está cedo (sobrevive ao truncamento)? · Tem repetição? · O SKU é distinguível? · Parece título de produto, não lista de keywords?

## Formato da saída
Por padrão, **um título recomendado** (a skill assume a escolha) com a contagem de caracteres:
```
Título recomendado:
Nike Pegasus 42 Tênis de Corrida Masculino Preto
48 caracteres
```
Alternativas só quando houver ganho real. Quando o lojista pedir **multicanal**, entrega os objetos que fizerem sentido (H1, SEO title, Google Merchant, short title). No **modo em lote**, devolve uma tabela `SKU | título atual | título recomendado | alerta`.

Prioridade sempre nesta ordem: **precisão → clareza → relevância → canal → comprimento.** Comprimento nunca é o objetivo principal.

Sob pedido (modo avançado), oferece a versão estruturada para feed do Merchant — conferindo a especificação vigente do Merchant Center, sem inventar campo.

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
