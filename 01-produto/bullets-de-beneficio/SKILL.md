---
name: bullets-de-beneficio
description: Cria, extrai e otimiza bullets de produto que transformam características em argumentos de venda claros e comprováveis — priorizando impacto na decisão, relevância, objeções e precisão factual — para PDP, Google Merchant e marketplaces. Aceita características cruas, uma descrição longa, bullets atuais, uma URL ou um catálogo. Use ao montar a seção de benefícios de um produto ou melhorar uma fraca.
---

# Bullets de Benefício

## O que faz
Decide **quais argumentos merecem ocupar espaço** na decisão de compra e transforma só esses em bullets claros e comprováveis. Não é "pegue cada spec e escreva uma frase bonita" — é descobrir o que realmente ajuda a pessoa a decidir, ranquear os candidatos e escrever os melhores, começando pelo benefício e ancorando na característica que o sustenta.

Regra de ouro: **simples na superfície, especialista por baixo.**

## Quando usar
- Montar a seção de benefícios de um produto novo (a partir de características cruas).
- Melhorar bullets fracos ou genéricos que já estão no ar.
- Extrair bullets de uma descrição longa.
- Preparar destaques para Google Merchant (`product_highlight`) ou marketplace.
- Padronizar os bullets de um catálogo inteiro (modo em lote).

## O que a IA precisa de você
No mínimo, o suficiente para entender o produto:
- as **características** (specs, diferenciais), ou
- uma **descrição** para extrair os bullets, ou
- os **bullets atuais** para melhorar, ou
- uma **URL** (se você tiver web; se não, cole o conteúdo), ou
- um **catálogo** (tabela de SKUs).

Opcional e valioso: público, canal de destino, **reviews** e **FAQ** (as dúvidas reais dos clientes). Se você não informar, a skill infere categoria e público prováveis e só pergunta 1–2 coisas quando a falta impede um bom resultado.

## Como funciona (por baixo)

**1. Detecta o modo, sozinha.** Criar (recebeu características) · Otimizar (recebeu bullets) · Extrair (recebeu descrição longa) · Em lote (recebeu catálogo).

**2. Separa benefício de especificação.** O que ajuda a decidir vira bullet; o que é só factual (código interno, dimensão de embalagem) fica na ficha técnica. *Peso: 268 g* pode virar bullet se for relevante; *SKU ABC132* não.

**3. Transforma com evidência — Feature → Advantage → Benefit → Evidence** (raciocínio interno, não aparece). O bullet final junta o ganho e a prova: *"Mais tranquilidade na multitarefa — 16 GB de RAM para manter vários apps abertos."*

**4. Mede a confiança do claim e só usa o que se sustenta.**
- **Alta** — direto do fato ("1 TB SSD" → muito espaço de armazenamento). Pode afirmar.
- **Média** — inferência plausível ("mesh respirável" → favorece a ventilação). Usar com linguagem proporcional.
- **Baixa** — salto grande sem prova ("mesh respirável" → "elimina o suor"). **Não entra.**

Quanto mais distante o benefício do fato, maior o risco — prefira sempre o claim proporcional à evidência.

**5. Gera mais candidatos do que precisa e ranqueia.** Não usa as primeiras 4–6 características que chegaram. Pontua cada candidato por impacto na decisão + relevância ao público + diferenciação + evidência + clareza + resolução de objeção − risco de claim − redundância. Escolhe os melhores.

**6. Busca variedade de argumento.** Classifica os candidatos por tipo (resultado, redução de problema, conveniência, performance, conforto, durabilidade, compatibilidade, versatilidade, estética, segurança) para não entregar 4 bullets dizendo a mesma coisa.

**7. Usa reviews e FAQ como ouro, quando houver.** Elogio recorrente sobe no ranking; dúvida decisiva ("serve em indução?", "é bivolt?") vira um **bullet que mata objeção** — que costuma valer mais que um benefício genérico. Nunca inventa review nem resposta.

**8. Adapta ao público e à categoria.** A mesma feature gera benefício diferente por público (16 GB de RAM: "roda seus jogos" para o gamer, "multitarefa sem travar" para o profissional). Cada categoria tem seu foco (moda: conforto/caimento; calçado: amortecimento/aderência; eletrônico: performance/autonomia; e assim por diante).

**9. Adapta a forma ao canal.** Na PDP própria, benefício antes da característica. Em alguns marketplaces, a característica na frente funciona melhor — a ordem é definida pelo canal.

## Instruções (o cérebro da skill)
1. Identifique o **modo** e extraia as **features** do que recebeu.
2. Classifique a **categoria** e infira o **público**.
3. Para cada feature relevante, rode o value map: o que permite? que problema reduz? para quem importa? tem evidência? resolve objeção? merece virar bullet?
4. Gere candidatos, **meça a confiança** (descarte os de confiança baixa), **ranqueie** e **diversifique** por tipo de benefício.
5. Escreva os melhores no formato do canal, um benefício por bullet, mobile-first.
6. Rode o **Quality Gate** e reescreva o que falhar.
7. Entregue só os bullets prontos (mais specs separadas, se útil).

**Estrutura do bullet (PDP):** `Benefício concreto — característica que o sustenta.`
**Quantidade:** 3 a 6 na PDP (use 3 se só há 3 bons — sem enchimento); 4 a 6 highlights no Merchant quando houver material.

## Regras de qualidade
- **Nunca invente** material, tecnologia, efeito, compatibilidade, certificação, durabilidade, performance, benefício de saúde, autonomia, resistência, garantia, teste ou resultado. Faltou o dado? Omita ou sinalize que informá-lo melhora os bullets.
- **Sem bullet de enchimento**: "alta qualidade", "design moderno", "excelente desempenho", "produto premium" — se não há especificidade e prova, não entra. Todo bullet responde *por que isso importa?* e *o que sustenta isso?*.
- **Um benefício por bullet**: o "e" ligando dois benefícios diferentes é sinal de que precisa dividir.
- **Claim proporcional à evidência**: "solado em borracha" → "mais aderência", nunca "nunca escorrega".
- **Claims sensíveis** (saúde, beleza, suplemento, infantil, segurança): nada de "cura", "elimina", "garante", "100% seguro", "protege totalmente" sem base.
- **Não misture produto com política comercial**: frete, preço, desconto, parcelamento, prazo e promoção não são bullets de produto — pertencem a outra área da página.
- **Dados conflitantes** (ex.: "4000 mAh" e "5000 mAh"): pergunte curto qual é o certo, não escolha no silêncio.
- **Mobile-first**: o benefício vem antes do travessão e é compreensível mesmo se o resto for cortado.

### Quality Gate (silencioso, antes de entregar)
O cliente entende por que importa? · Tem feature sustentando? · É concreto? · É defensável? · A promessa é proporcional à evidência? · Repete outro bullet? · Merece o espaço? · É rápido de escanear? · Combina com a categoria e o público? · Respeita o canal? · Um benefício só por bullet?

## Formato da saída
Por padrão, **só os bullets prontos para colar**. Se sobraram specs úteis que não viraram benefício, uma lista curta à parte ("Specs para a ficha técnica"). Nada de diagnóstico, framework ou score.

Sob pedido, entrega em outro formato: **Google Merchant `product_highlight`** (4–6 destaques factuais, até 150 caracteres cada, sem preço, promoção, frete, nome da loja, comparação nem repetição do título); **bullets no padrão Amazon** (feature + benefício — conferindo a política vigente da Amazon, que muda); versão curta; ou o antes/depois dos bullets atuais. No **modo em lote**, uma tabela `SKU | bullets | alertas`, com estilo consistente mas sem repetir o mesmo argumento em todos os produtos.

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
