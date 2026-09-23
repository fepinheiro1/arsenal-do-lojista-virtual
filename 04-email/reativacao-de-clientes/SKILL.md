---
name: reativacao-de-clientes
description: Desenha a reativação a partir do ciclo de recompra esperado e do estado do cliente (novo/ativo/no prazo/atrasado/inativo/dormente), separando winback (parou de comprar quando era razoável recomprar) de re-engagement (parou de interagir) e de replenishment (lembrete de recompra no ciclo). Reacende pelo que é novo/relevante e real, com incentivo só quando faz sentido, e protege a saúde da base (supressão, sunset, entregabilidade) em vez de insistir. Aceita histórico/categoria, sinais de engajamento, novidades reais e a plataforma. Use para criar, segmentar, otimizar ou auditar a reativação.
---

# Reativação de Clientes

## O que faz
Cria a reativação que primeiro pergunta **quem faz sentido recuperar** — e como. Antes de mandar "volte", decide se a pessoa está mesmo **atrasada em relação ao comportamento esperado** dela (o ciclo de recompra daquele produto), e qual é o problema real: parou de **comprar** (winback), parou de **interagir** (re-engagement) ou só está **na hora natural de repor** (replenishment). Cada um pede uma conversa diferente.

Regra de ouro: **reativação inteligente não tenta ressuscitar todo contato — identifica quem vale a pena recuperar, respeita quem perdeu o interesse e protege a saúde da base.** Reacende pelo que é novo/relevante e verdadeiro, nunca pela cobrança da ausência. A voz é da marca do lojista.

## Quando usar
- Montar (ou melhorar) o e-mail/fluxo para a base que esfriou.
- Decidir o **limite de inatividade por categoria** (consumível ≠ durável ≠ sazonal) e separar winback de re-engagement de replenishment.
- Auditar um fluxo existente (threshold, tom, incentivo, supressão, sunset, entregabilidade).

## O que a IA precisa de você
- `[estado do cliente]` — recorrência, valor, última compra e categoria (RFM quando houver). Sem dados, classificação conservadora.
- `[ciclo de recompra esperado]` — o intervalo natural daquele produto (por histórico/categoria/consumo). Sem base, não inventa janela.
- `[sinais de engajamento]` — clique, visita, compra, visualização, resposta (não só "abriu"). Só os que existem.
- `[o que há de novo / recomendação]` — novidade real (coleção, categoria, melhoria, reposição) ou base real de recomendação (compra, afinidade, curadoria). Sem isso, `[preencher]` / estratégia sem novidade.
- `[incentivo]` (opcional) — cupom/condição real, e a política.
- `[plataforma]` — o que suporta (preference center, supressão, sunset, deep link). Sem isso, linguagem conservadora.

## Como funciona (por baixo)

**1. Ciclo esperado antes de tudo — "X dias" não é universal.** 90 dias é crítico para um consumível e irrelevante para um colchão. A skill parte do **intervalo de recompra esperado** daquele produto (consumível/reposição, discricionário repetível, sazonal, durável/longo ciclo) e só chama de "atrasado" quem passou da **própria** janela. Sazonal fora de época **não é** churn.

**2. Três problemas diferentes.** *Winback* (deixou de comprar quando havia expectativa razoável de recompra) · *Re-engagement* (deixou de interagir com os e-mails — problema de relação com a comunicação, não necessariamente de compra) · *Replenishment* (está só na hora natural de repor — é lembrete, não "reativação"). Confundir os três gera a mensagem errada. E "risco de churn" (heurística/modelo) **não é** "churn de fato".

**3. Estado do cliente e RFM, sem inventar.** Novo / ativo / no prazo / atrasado / lapso / dormente / reativado — limites vindos do negócio e dos dados. Recência é sinal, não diagnóstico; um recorrente que parou é diferente de quem comprou uma vez; valor histórico ajuda a **priorizar** investimento/incentivo, sem tratamento manipulativo e sem LTV fabricado. Um cliente pode estar inativo **numa categoria** e ativo em outra — winback por categoria costuma ser melhor.

**4. Engajamento vai além de "abriu".** Abertura é imperfeita (proteções de privacidade inflam/escondem o open) — **não** definir inatividade nem disparar o próximo e-mail só por "não abriu" (erro da V1). Preferir clique, visita ao site, visualização de produto, compra e resposta, respeitando consentimento.

**5. O que dizer: novidade real, recomendação real, ou benefício.** Novidade precisa ser verdadeira e relevante (coleção, categoria, melhoria, reposição de fato ocorrida). Sem novidade, a estratégia é replenishment, caso de uso, educação, complemento, preferência ou benefício real — nunca fingir personalização. Para durável, **não** pressionar recomprar o mesmo item: explorar acessório, manutenção, complemento ou o que é novo. Reconhecer o vínculo **sem culpa** ("você sumiu" e "sentimos sua falta" como argumento central estão fora; um toque leve pode existir, mas o valor vem antes).

**6. Incentivo com gate; cupom não é default.** Antes do desconto, avaliar ciclo, valor, margem, histórico, motivo e segmento — muita gente volta pela novidade/relevância. Cupom recorrente **ensina a esperar desconto**; então condicional e segmentado, com valor/validade/mínimo/exclusões reais. Uma compra por desconto sem retenção tem valor limitado — o que importa é a **nova frequência**, não a conversão isolada.

**7. Papéis, timing e comprimento adaptativos.** Cada mensagem tem um papel (repor, descobrir, atualizar, recomendar, valor, preferência, incentivo, reengajar, sunset). O timing nasce do **estágio** (no prazo → lembrete; atrasado → novidade/benefício; dormente → confirmação de interesse antes de voltar à frequência normal) — nada de "volte" antes de existir atraso real. O comprimento é adaptativo: 1 mensagem, 2–3, ou uma série maior em operação madura — conforme valor, ciclo, consentimento e engajamento.

**8. Proteger a base: supressão, saída, sunset, entregabilidade.** **Purchase Exit**: comprou durante o fluxo → sai e migra para o lifecycle certo (nada de continuar "volte a comprar"). **Engagement Exit**: deu sinal relevante (clique/preferência) → sai do sunset e volta ao segmento apropriado. Suprime unsubscribed, complaint, bounce, inelegível, compra recente e fluxo conflitante. Oferecer **preference center** (frequência, categorias, pausa) pode ser melhor que unsubscribe total; contato muito antigo pode pedir **re-permissão** ("ainda quer receber?"). E **sunset**: contato persistentemente inativo é reduzido/suprimido do marketing ativo — não para "apagar cliente", mas para proteger reputação, entregabilidade e custo. Insistir em base sem engajamento **queima o domínio** (autenticação/complaint herdados do `html-newsletter`). Higiene distingue unsubscribe ≠ bounce ≠ complaint ≠ inválido ≠ desengajado ≠ dormente.

**9. Colisão, cross-channel e medição real.** Winback colide com cart, browse, welcome, pós-compra, promo e replenishment — o evento de maior intenção/atualidade ganha. E-mail/SMS/WhatsApp/push não disparam todos juntos numa base fria. Mede clique, retorno ao site, compra, taxa de reativação, receita, atualização de preferência, unsubscribe/complaint e custo do incentivo — **não** a abertura, e **não** confundindo receita pós-fluxo com receita causada (só um holdout/coorte mostra o incremento).

## Instruções (o cérebro da skill)
1. Identifique o **modo** (criar / segmentar / otimizar / auditar / replenishment / re-engajar / sunset / replanejar) e fixe o **Winback Truth Lock** (status do cliente, última compra/categoria, ciclo esperado, RFM, sinais de engajamento, novidade/recomendação real, regras de incentivo, consentimento/elegibilidade, entregabilidade, supressão/saída, canal).
2. Calcule o **atraso real** contra o ciclo esperado e classifique **winback × re-engagement × replenishment** + estado do cliente.
3. Aplique **elegibilidade, supressão e saídas** (purchase exit, engagement exit) e decida o **comprimento** do fluxo.
4. Atribua **papéis e timing pelo estágio**; escreva com novidade/recomendação **real** (ou estratégia sem novidade), tom sem culpa, personalização com fallback.
5. Passe o incentivo pelo **gate** (margem, dependência de desconto, verdade) e considere **preference center / re-permissão / sunset** quando aplicável.
6. Rode o **Quality Gate** e entregue o e-mail (ou fluxo) + segmento + timing + regras de saída/supressão.

## Regras de qualidade
- **Ciclo esperado** manda no threshold; nada de dias universais; sazonal fora de época não é churn.
- **Winback ≠ re-engagement ≠ replenishment**; risco de churn ≠ churn de fato.
- **Engajamento além de "abriu"**; nunca disparar o próximo e-mail só por não ter aberto.
- **Novidade e recomendação reais**; durável não recompra o mesmo item na marra; sem fingir personalização.
- **Tom sem culpa**: "você sumiu" fora; "sentimos sua falta" nunca como argumento central; valor antes.
- **Incentivo com gate** (margem, dependência de desconto), real; cupom não é default.
- **Supressão e saídas** (purchase/engagement exit); colisão de fluxos resolvida; cross-channel sem bombardeio.
- **Saúde da base**: preference center / re-permissão / sunset / higiene; entregabilidade herdada do `html-newsletter` (não é exceção).
- **Persuasão ética**: sem urgência/escassez falsa, sem garantia de resultado; frases curtas, mobile.
- **KPI de reativação e retenção** (não a abertura); receita recuperada ≠ incremental. **Voz da marca, não da Performa.**

### Winback Quality Gate (silencioso)
A inatividade existe de verdade (contra o ciclo da categoria)? · É winback, re-engagement ou replenishment? · Estado/RFM usados sem inventar? · Engajamento além de opens? · Novidade/recomendação reais? · Tom sem culpa? · Durável sem forçar recompra? · Incentivo necessário e real (dependência de desconto)? · Personalização com fallback? · Purchase/engagement exit e supressão certas? · Colisão de fluxos? · Cross-channel sem bombardeio? · Preference center / re-permissão / sunset quando cabe? · Entregabilidade protegida? · KPI além de opens? · Incremental considerado? · Fluxo simples de manter? — se falhar, reestruture.

## Formato da saída
O **e-mail pronto** (ou fluxo): para cada mensagem `Segmento | Quando | Assunto | Preheader | Corpo | CTA`, com o **segmento e o momento** (contra o ciclo esperado, não "há X dias" cru) e os placeholders a preencher. O incentivo (se houver) fica condicional e passado pelo gate.

Sob pedido: o fluxo com automação (gatilho, delay, saída, supressão, ramificação), a segmentação por lifecycle/RFM/categoria, a etapa de **sunset/re-permissão**, a auditoria de um fluxo existente, ou só a copy. Nada de relatório por padrão.

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
