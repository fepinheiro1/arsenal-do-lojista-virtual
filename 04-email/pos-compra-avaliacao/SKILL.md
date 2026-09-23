---
name: pos-compra-avaliacao
description: Desenha o pós-compra que pede avaliação no momento em que a pessoa realmente tem uma opinião útil — a partir da entrega real (entregue, retirado, acesso liberado, serviço concluído), da janela de uso do produto e da elegibilidade, sem enviesar a nota nem esconder o link de quem teve problema. Ajuda antes de pedir quando o produto tem curva de uso, trata avaliação de produto/loja/entrega separadamente, e respeita a política de incentivo da plataforma de destino. Aceita o estado do pedido, o produto/variante, a plataforma de avaliação, o suporte e o incentivo (se houver). Use para criar, otimizar ou auditar o pedido de avaliação.
---

# Pós-Compra e Avaliação

## O que faz
Cria o pós-compra que pede avaliação **quando a pessoa já formou uma opinião que serve para o próximo comprador** — não alguns dias após a *compra*, mas depois da **entrega real** e do **tempo de uso** que aquele produto exige. Antes de pedir, verifica se a pessoa precisa de ajuda (montagem, cura, setup, primeiro uso); separa avaliação de produto, de loja e de entrega; e trata o feedback negativo como legítimo, sem escondê-lo.

Regra de ouro: **o objetivo não é maximizar estrelas — é coletar feedback autêntico, útil e confiável.** Nunca pedir nota alta, nunca rotear o insatisfeito para um canal privado que suprime a avaliação, nunca condicionar recompensa a elogio. A voz é da marca do lojista.

## Quando usar
- Montar (ou melhorar) o e-mail/fluxo de pedido de avaliação pós-entrega.
- Decidir **quando** pedir por categoria de produto (roupa ≠ cosmético ≠ móvel ≠ eletrônico ≠ consumível ≠ digital).
- Auditar um pedido existente (timing, readiness, gating, neutralidade, incentivo, privacidade).

## O que a IA precisa de você
- `[estado do pedido]` — entregue, retirado, acesso digital liberado ou serviço concluído (e se a plataforma **confirma** isso). Sem confirmação, linguagem conservadora.
- `[produto / variante]` — o item e o SKU/variante certos, para o deep link e a janela de uso (idealmente via variável da ferramenta).
- `[plataforma de avaliação]` — onde a avaliação vive (página do produto, plataforma de reviews, marketplace, "responda este e-mail") e o link/deep link real. Sem isso, `[preencher]`.
- `[apoio pós-venda]` (opcional) — canais reais (WhatsApp, troca, garantia, guia de uso). Só o que existe.
- `[incentivo]` (opcional) — cupom/condição real, **e a política do destino** (marketplaces costumam restringir avaliação incentivada).

## Como funciona (por baixo)

**1. Verdade da entrega, não da compra.** O gatilho é o **estado real**: entregue, retirado na loja, acesso digital liberado ou serviço concluído — nunca "X dias depois da compra". Se o status de entrega não é confiável, a linguagem é conservadora (não afirma que a pessoa já usou).

**2. Janela de uso e prontidão (Review Readiness).** Antes de pedir, pergunta: *quanto tempo esse produto precisa de uso para gerar uma opinião útil?* Roupa pode ser rápido; cosmético exige alguns usos; colchão/móvel pede semanas; eletrônico tem setup; consumível segue o consumo; digital é quase imediato. A pessoa está em `NÃO PRONTO`, `PRIMEIRA IMPRESSÃO`, `PRONTO` ou `LONGO PRAZO` — não existe "dias universais".

**3. Ajuda antes do pedido (Help-First).** Se o produto tem curva de uso (montagem, cura da panela, configuração, cuidado), a ajuda pode vir **antes** de pedir avaliação — quem foi bem ajudado avalia melhor, e por vontade própria. Isso é onboarding genuíno, não um filtro para peneirar quem está feliz.

**4. Tipo e destino de avaliação são coisas diferentes.** Produto (o item/SKU) ≠ loja (a experiência de compra) ≠ entrega (a transportadora) ≠ serviço ≠ NPS/CSAT. Um problema de transportadora não deve virar nota baixa do produto. E **NPS/CSAT privado não vira review público** sem ação/consentimento explícito. Escolhe **um destino** apropriado (PDP, plataforma, marketplace) — não pede a mesma avaliação em vários lugares por padrão, e usa link/deep link **real**, sem inventar merge tag.

**5. Sem review gating — a regra ética central.** **Proibido** rotear "satisfeito → avaliação pública / insatisfeito → suporte privado (e sem link)". Todo cliente elegível pode avaliar honestamente. O suporte é oferecido **a todos** e em paralelo, sem esconder o link de avaliação de quem teve problema. "Evitar nota baixa" não é objetivo; resolver o problema e coletar feedback autêntico é. E pede-se **a avaliação, nunca a nota** — nada de "dê 5 estrelas", nada de pergunta que induz positividade.

**6. Elegibilidade, saídas e colisão.** Verifica entrega, cancelamento, reembolso, se o produto é elegível e **se a avaliação já foi enviada** (quem avaliou sai dos lembretes). Cliente em devolução/reembolso pode precisar de outro contexto — mas não perde o direito de avaliar. O pós-compra colide com suporte, return/refund, recompra, cross-sell, fidelidade e winback: **a experiência tem prioridade**, e e-mail/SMS/WhatsApp/push não disparam todos juntos.

**7. Incentivo: neutro, verdadeiro e conforme a política.** Se houver incentivo, ele **não pode depender de opinião positiva** (vale para elogio ou crítica), o cupom/valor/validade tem que ser real, e — decisivo — **a plataforma de destino pode proibir avaliação incentivada** (vários marketplaces proíbem). Verifica o destino antes de recomendar incentivo; quando permitido, pode exigir *disclosure*. Recompensa por foto/vídeo segue a mesma regra: nunca condicionada à nota.

**8. UGC e privacidade.** Foto/vídeo é **opcional** — a avaliação básica não pode depender de mídia. Foto num review não é autorização irrestrita para publicidade (reuso pode exigir consentimento/termos). Evita expor nome, rosto, localização, crianças, casa. Moderação legítima remove spam, PII, abuso e off-topic — **nunca** remove só por ser negativa.

**9. Lembrete sem cobrança, e medição além da média.** Pode lembrar quem não avaliou, com **frequência limitada**, mudando o contexto (não repetir o mesmo e-mail) e **parando após a avaliação** — nunca "você ainda não avaliou". O timing nasce da entrega + janela de uso + categoria + comportamento, não de uma cadência fixa. E mede envio/clique/conclusão/qualidade/cobertura de SKUs sem review — **não** a nota média (otimizar rating médio é o incentivo errado); só um holdout mostra o efeito real do pedido.

## Instruções (o cérebro da skill)
1. Identifique o **modo** (criar / otimizar / auditar / timing / ramificar / só copy / UGC / replanejar) e fixe o **Review Truth Lock** (entrega + confiança, produto/variante, janela de uso, readiness, tipo/destino, elegibilidade, return/refund/suporte, incentivo/política, link de avaliação, contexto do cliente/canal).
2. Determine a **prontidão** pela janela de uso da categoria e aplique **elegibilidade, saída (já avaliou / cancelado / reembolso) e supressões**.
3. Passe pelo **Help-First gate**: se há curva de uso, ajuda antes (ou junto) do pedido.
4. Escolha **tipo e destino** de avaliação (um só) com **link real**; escreva com **pergunta neutra**, prompts opcionais úteis e UGC opcional — **sem gating e sem induzir a nota**.
5. Passe o incentivo pelo **gate de política do destino** (permitido? disclosure?) e pela **neutralidade**.
6. Rode o **Quality Gate** e entregue o e-mail (ou fluxo) + timing + lembrete + regras de saída/supressão.

## Regras de qualidade
- **Entrega real** como gatilho (não "dias após a compra"); linguagem conservadora se o status não é confiável.
- **Prontidão pela janela de uso** da categoria; nada de dias universais.
- **Sem review gating**: nunca esconder o link de quem teve problema; suporte a todos, em paralelo.
- **Pedir avaliação, nunca a nota**; assunto e perguntas neutros, sem induzir positividade.
- **Tipo/destino certos**: produto ≠ loja ≠ entrega; NPS/CSAT privado não vira público sem consentimento; um destino, link real, sem merge tag inventada.
- **Elegibilidade e saída por avaliação enviada**; return/refund não tira o direito de avaliar; colisão com outros fluxos resolvida.
- **Incentivo** neutro (vale para crítica), real e **conforme a política do destino**; disclosure quando exigido.
- **UGC opcional**, privacidade preservada, moderação que não apaga o negativo.
- **Lembrete sem culpa**, com limite e saída; persuasão ética (sem "imperdível"/"última chance"); entregabilidade herdada do `html-newsletter`.
- **Voz da marca, não da Performa.**

### Review Quality Gate (silencioso)
Entrega confirmada (ou linguagem conservadora)? · Janela de uso respeitada (readiness)? · Precisa de ajuda antes? · Tipo e destino certos (produto ≠ entrega; NPS privado)? · Um destino, link real e não inventado? · Elegível e ainda não avaliou? · Return/refund considerado sem tirar o direito? · **Algum gating escondendo o link do insatisfeito?** · Pede a avaliação e não a nota? · Assunto/perguntas neutros? · Incentivo neutro, real e permitido no destino? · UGC opcional e privacidade ok? · Moderação não apaga o negativo? · Lembrete com limite e saída, sem culpa? · Cross-channel coordenado? · KPI de feedback autêntico (não a média)? — se falhar, corrija.

## Formato da saída
O **e-mail pronto**: `Assunto (2 opções) · Preheader · Corpo · CTA (leva ao destino real da avaliação)`, com o momento de envio (a partir da **entrega confirmada** + janela de uso da categoria) e os placeholders a preencher. Se houver incentivo, a variação com e sem — sempre neutra e condicionada à política do destino.

Sob pedido: o **fluxo** (gatilho por entrega, elegibilidade, saída por avaliação enviada, lembrete, supressões), a ramificação por tipo/destino, o pedido de UGC, a auditoria de um fluxo existente, ou só a copy. Nada de relatório por padrão.

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
