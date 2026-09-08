---
name: faq-do-produto
description: Descobre, prioriza e responde as dúvidas e objeções que realmente travam a compra de um produto — usando PDP, especificações, atendimento, reviews e Q&A — com controle de evidência, atualização contínua e prevenção de respostas inventadas. Aceita produto, URL, uma FAQ atual, uma descrição longa ou o histórico de perguntas dos clientes. Use ao criar a FAQ de um produto, melhorar uma fraca ou transformar dúvidas reais de atendimento em respostas prontas.
---

# FAQ do Produto

## O que faz
Descobre o que faz a pessoa hesitar antes de comprar e responde só o que tem evidência. Não é "inventar 6 a 8 perguntas plausíveis" — é um motor de objeções: encontra as dúvidas que travam a compra (das perguntas reais dos clientes, do atendimento, dos reviews e da própria página), prioriza as que mais pesam na decisão e responde com precisão. Boa FAQ vende (tira o receio), alivia o atendimento (a resposta já está na página) e reduz devolução (a pessoa compra sabendo o que leva).

Princípio: **pergunta real quando possível, resposta comprovável sempre, invenção nunca.** Simples na superfície, especialista por baixo.

## Quando usar
- Criar a FAQ de um produto (novo ou que já vende).
- Melhorar uma FAQ fraca, repetitiva ou com resposta vaga.
- Transformar dúvidas reais (WhatsApp, chat, tickets, Q&A) em FAQ pronta.
- Atualizar uma FAQ com as novas perguntas que começaram a chegar.
- Padronizar a FAQ de um catálogo inteiro (modo em lote).

## O que a IA precisa de você
No mínimo, uma destas coisas:
- o **produto** (nome + o que você souber), ou
- uma **URL** (se você tiver web; se não, cole o conteúdo), ou
- as **perguntas reais** dos seus clientes (atendimento, Q&A), ou
- uma **FAQ atual** para melhorar, ou
- um **catálogo** (tabela de SKUs).

Opcional e muito valioso: as **fontes oficiais** (rótulo, manual, ficha técnica, política da loja) — é o que permite responder com fato em vez de deixar como pendência. Se você não informar, a skill **descobre** as perguntas importantes mesmo assim e, quando não tem como provar a resposta, entrega a pergunta como pendência em vez de inventar.

## Como funciona (por baixo)

**1. Detecta o modo, sozinha.**
- **Criar** — a partir do produto/URL.
- **Otimizar** — recebeu uma FAQ pronta → tira o irrelevante, o repetido, a resposta vaga ou desatualizada, o claim sem prova e a pergunta promocional; preserva o que está bom.
- **Minerar** — recebeu atendimento/reviews/Q&A → extrai as perguntas, agrupa as iguais, mede frequência, vira FAQ.
- **Atualizar** — FAQ atual + perguntas novas → incorpora as recorrentes, consolida redundâncias, remove o obsoleto, sinaliza o que precisa reconfirmar.
- **Em lote** — catálogo → uma FAQ por SKU, consistente sem ficar idêntica.

**2. Descobre as objeções — não repete o óbvio.** Antes de incluir uma pergunta, checa se ela acrescenta algo que o título, a descrição, os bullets e as specs ainda não deixam claro. Classifica os candidatos por tipo (adequação, compatibilidade, tamanho, uso/instalação, performance, material, segurança/restrições, manutenção, conteúdo da embalagem, garantia, troca, entrega, variantes, autenticidade) para não gerar cinco perguntas do mesmo tipo e esquecer as outras.

**3. Prioriza as fontes certas.** Pergunta real de cliente > atendimento/suporte > Q&A existente > review > PDP/specs > dúvida típica da categoria > inferência da IA. Uma pergunta que veio de gente de verdade pesa mais que uma hipótese.

**4. Separa "quem revela a pergunta" de "quem prova a resposta".** O review e o atendimento revelam a dúvida; a resposta factual vem da fonte adequada — specs do manual/fabricante, política da política oficial da loja, compatibilidade da documentação oficial. Review individual não prova compatibilidade, e "ninguém reclamou" não prova claim.

**5. Mede a evidência antes de responder.**
- Hierarquia da fonte: **A** oficial (manual, rótulo, fabricante, política) → **B** explícito na PDP → **C** reviews/Q&A (revelam, não provam tema técnico) → **D** inferência segura (sugere a pergunta, não sustenta fato forte) → **E** desconhecido (não responder como fato).
- Confiança da resposta: **confirmada** (fonte oficial) e **apoiada** (boa evidência) podem ser publicadas; **incerta** e **desconhecida** viram pendência ou pergunta ao lojista — nunca fato.

**6. Prioriza por impacto na compra.** Ranqueia as perguntas por: impacto na decisão + frequência real + quanto reduz a incerteza + relevância ao público + evidência disponível + diferenciação + prevenção de devolução/de ticket/de quebra de confiança − duplicação − risco da resposta. A FAQ reflete a decisão de compra, não a lista de dados disponíveis.

**7. Deduplica, checa contradição e atualidade.** "Serve no iPhone 15?", "Funciona no iPhone 15?" e "É compatível com iPhone 15?" viram um cluster (escolhe a formulação mais natural). Se descrição, ficha e manual divergem, não escolhe no silêncio — sinaliza o conflito. Compatibilidade, software, garantia e políticas envelhecem: prefere a fonte oficial mais nova.

## Instruções (o cérebro da skill)
1. Identifique o **modo** e reúna as fontes (produto, URL, atendimento, reviews, specs, políticas).
2. Classifique a **categoria** e infira o **público**.
3. **Descubra** os candidatos a pergunta (das fontes reais primeiro), **deduplique** em clusters e **ranqueie** por impacto na compra.
4. Para cada pergunta, **case com a evidência**: só responde como fato o que é confirmado/apoiado; o resto vira pendência.
5. Escreva no formato: **resposta direta primeiro**, contexto necessário depois, condição/limitação quando houver. Simples: 1–2 frases; técnica pode usar lista curta.
6. **Quantidade adaptativa**: 3–5 (produto simples), 5–8 (intermediário), 8–12+ agrupadas (complexo/alto risco). Nunca crie pergunta só para preencher número.
7. Se a FAQ ficar longa, **agrupe** por seção (Tamanho/Ajuste, Compatibilidade, Uso, Cuidados, Garantia...). Ordene por impacto — **nunca** alfabeticamente.
8. Rode o **Quality Gate** e corrija/retire o que falhar.
9. Entregue a FAQ pronta + (se houver) a lista curta de pendências a confirmar antes de publicar.

## Regras de qualidade
- **Invenção nunca.** Não invente voltagem, compatibilidade, medida, conteúdo da caixa, certificação, dose, preparo, indicação, origem, garantia ou política. Faltou o dado? Vira **pendência** ("Antes de publicar, confirme..."), não uma resposta.
- **Conhecimento geral da categoria não é fato daquele SKU.** "Whey 900 g" não autoriza afirmar dose, número de porções, preparo, horário, lactose/glúten ou indicação — isso vem do rótulo/fabricante. (Corrige o erro clássico da V1.)
- **Categorias sensíveis** (saúde, suplemento, cosmético, infantil, segurança, alimento/alergênico, elétrico, regulado): exigência de evidência elevada. Nada de promessa terapêutica ou claim sem fonte.
- **Compatibilidade**: distinga documentada, inferida e desconhecida. "USB-C" não prova compatibilidade com todo iPhone/Mac, Thunderbolt, vídeo ou carga rápida.
- **Variantes**: se a resposta muda por tamanho, voltagem, capacidade ou sabor, não generalize uma variante para todas.
- **Contexto regional**: garantia, certificação, voltagem e devolução podem depender do país — não importe regra de outro mercado.
- **Produto × política**: dúvida do produto é uma coisa; política global de frete/devolução é outra (aponte a política oficial, não a repita em toda página). Só a exceção específica daquele produto entra.
- **Honestidade**: se não serve, diga. Não esconda limitação conhecida ("não acompanha carregador", "não é bivolt", "exige montagem") — isso reduz devolução e suporte. Quando há exceção, resposta condicional, nunca "sim" absoluto.
- **Voz real do cliente**: "Funciona no Mac?", não "Qual o nível de interoperabilidade com sistemas Apple?".
- **Sem pergunta promocional**: "Por que é o melhor?", "Por que você vai amar?", "Por que comprar agora?" são copy, não FAQ — proibidas.
- **Contradição entre fontes**: pergunte de forma curta qual é a correta, não escolha em silêncio.
- **Links**: pode resumir e apontar para o manual/política oficial; nunca invente um link.

### Quality Gate (silencioso, antes de entregar)
É pergunta real? · Tem impacto na compra? · Tem evidência? · A resposta é exata e defensável? · É específica? · Repete outra? · Está atualizada? · Vale para a variante certa? · O escopo de política está correto? · Claim sensível tem prova? · Voz natural? · Concisa? · Ajuda a agir? — se falhar, corrige ou retira.

## Formato da saída
Por padrão, **a FAQ pronta para publicar** — pergunta na voz do cliente, resposta direta:
```
**Funciona no Mac?**
Sim, nos modelos oficialmente compatíveis com [requisito confirmado].

**O carregador acompanha?**
Não. A embalagem inclui [conteúdo confirmado].
```
Se houver dúvidas importantes que você ainda não pode responder com fato, uma lista curta no fim:
```
Antes de publicar, confirme:
- voltagem (verificar no rótulo);
- compatibilidade com X (verificar no manual do fabricante).
```
Sem relatório técnico, score ou framework.

Sob pedido (modo avançado), também: FAQ Schema `FAQPage` JSON-LD (com a ressalva de que o Google raramente exibe FAQ rich results para e-commerce comum — o schema reflete o conteúdo visível), pares Q&A em JSON para base de conhecimento/chatbot, os clusters de frequência do atendimento, o antes/depois de uma FAQ existente, ou a tabela por SKU no modo em lote.

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
