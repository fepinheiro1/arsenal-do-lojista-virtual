---
name: html-newsletter
description: Cria uma campanha de e-mail para e-commerce em três camadas — estratégia, copy e HTML email-safe — verdadeira, legível, acessível, compatível com os clientes de e-mail e preparada para chegar à caixa de entrada. Entrega assunto/preheader, corpo, CTA bulletproof, HTML de tabela com fallback, plain-text opcional, placeholders e alertas de entregabilidade. Aceita objetivo, tipo, segmento, oferta, marca, links e plataforma. Use para newsletter, promoção, lançamento ou comunicado.
---

# HTML de Newsletter

## O que faz
Monta uma campanha de e-mail inteira — não só "um HTML bonito". Trabalha três camadas separadas: a **estratégia** (objetivo, segmento, oferta, mensagem), a **copy** (assunto, preheader, corpo, CTA) e a **renderização** (HTML compatível com os clientes de e-mail). E entrega o e-mail preparado para o mundo real: legível no celular, compreensível com as imagens bloqueadas, acessível, seguro no Outlook, com o descadastro previsto e sem dado inventado.

Regra de ouro: **copy boa não compensa infraestrutura ruim; infraestrutura boa não compensa e-mail irrelevante.** A skill respeita as duas camadas. A voz é da marca do lojista.

## Quando usar
- Anunciar coleção, lançamento, reposição ou um informativo periódico.
- Comunicar uma oferta real (data e condição definidas).
- Melhorar uma campanha existente, adaptá-la a uma plataforma, ou só gerar o HTML de uma copy aprovada.

## O que a IA precisa de você
- `[objetivo]` e `[tipo]` — o que a pessoa deve fazer; e se é promoção, newsletter editorial, lançamento, reposição, comunicado ou educativo (muda a estrutura e a intensidade comercial).
- `[segmento]` — quem recebe (cliente, lead, VIP, quem comprou uma categoria...). "Lista geral" não é um default cego, e a skill não inventa segmentação.
- `[conteúdo/oferta]` — destaques com benefício; preço/cupom/prazo só se forem reais.
- `[marca]` — nome, tom, cor; `[links]` — para onde os CTAs levam.
- `[plataforma]` (opcional) — Klaviyo, Mailchimp, RD Station, Brevo... (define as merge tags e o descadastro). Sem ela, a skill usa placeholders neutros.

## Como funciona (por baixo)

**1. Trava a verdade.** Marca (tom, identidade, claims permitidos), Produto (sem inventar feature, benefício, preço, estoque ou popularidade), Oferta (desconto/cupom/prazo/frete reais) e Link (o CTA leva ao destino certo — URL não informada vira placeholder e pendência, nunca inventada).

**2. Um objetivo principal — com flexibilidade editorial.** Um e-mail tem um trabalho principal, mas uma newsletter pode legitimamente ter links secundários. "Um CTA único" é a regra geral, não uma lei absoluta.

**3. Assunto e preheader sem números mágicos.** O assunto prioriza clareza, valor e identidade, com a informação importante cedo — o comprimento é heurística (o truncamento muda por cliente), não "~45 caracteres". As opções testam **ângulos diferentes** (clareza, benefício, novidade, especificidade, pergunta, oferta), não "uma direta, uma curiosa". O assunto **corresponde ao conteúdo** (sem "Re:/Fwd:" falso, urgência inventada ou personalização fictícia). O preheader é uma segunda linha que **complementa** (não repete), também com tamanho adaptativo — e vai como texto de prévia controlado, para o cliente não puxar texto aleatório do topo.

**4. Hierarquia da informação e mobile-first.** Antes do HTML: motivo do e-mail → valor para quem lê → prova/detalhe → ação → secundários. Não começa pela empresa. No celular (onde a maioria abre): coluna única, texto legível, botões grandes, sem depender de hover, e o topo comunica marca + mensagem sem um hero gigante empurrando tudo para baixo.

**5. HTML email-safe de verdade.** Layout em **tabela** (Outlook ainda precisa), CSS **inline** nas propriedades críticas com fallback, **sem JavaScript**, fontes seguras. O CTA é um **botão bulletproof** (área de toque confortável, funciona mesmo com estilos variando) com rótulo que diz a ação ("Ver a coleção", não "clique aqui"). Não é uma landing page moderna disfarçada de e-mail. A largura ~600px é referência de compatibilidade, não dogma.

**6. Resiliente a imagem bloqueada e a dark mode.** Headline, preço e CTA essenciais **nunca ficam só dentro da imagem** (muita gente vê com imagens off). Imagens levam `alt` útil (decorativa pode ter alt vazio), width/height definidos e peso otimizado. E o design sobrevive ao **dark mode** (logo legível, sem texto que some, sem depender de uma cor exata).

**7. Descadastro, identidade e entregabilidade.** Todo marketing precisa de **descadastro real** — a skill usa um placeholder neutro ou adapta à merge tag da plataforma informada (não crava `{{ link_descadastro }}`). O **remetente é identificado com honestidade** (sem nome enganoso nem falso "responder"). E ela **sinaliza a camada técnica** que não configura mas da qual a entrega depende: autenticação (SPF/DKIM/DMARC), requisitos de remetente em volume (Gmail/Yahoo), endereço postal quando exigido, e base legal (LGPD) — **sem "resolver" o jurídico** e sem sugerir compra de lista/disparo para base sem consentimento. Nada de blacklist ingênua de "palavras de spam" (a entrega depende de reputação, autenticação e engajamento, não da palavra "grátis").

**8. Medição honesta.** Placeholders de rastreamento/UTM consistentes (sem inventar a convenção que a loja já usa); personalização só com **fallback** ("Olá!" quando não há o nome) e sem inventar merge tag; e o lembrete de que **open rate não é verdade absoluta** (a privacidade do Apple Mail infla opens) — priorizar cliques, sessões, conversão e reclamações.

## Instruções (o cérebro da skill)
1. Identifique o **modo** (criar copy+HTML / só copy / só HTML de uma copy aprovada / otimizar / adaptar a plataforma-segmento / auditar / variação de assunto / template reutilizável) e fixe o **Email Truth Lock**.
2. Defina **tipo + segmento + objetivo** e a **hierarquia da informação**.
3. Escreva **assunto (variantes por ângulo) + preheader + corpo + CTA** na voz da marca.
4. Renderize o **HTML email-safe** (tabela, inline, bulletproof, alt, images-off, dark mode, descadastro), com plain-text opcional.
5. Rode o **Quality Gate**, liste os **placeholders** e emita os **alertas de entregabilidade** que fizerem sentido.

## Regras de qualidade
- **Verdade**: sem inventar produto, oferta, número, URL, merge tag, segmento ou endereço; o que falta vira `[preencher]`/pendência.
- **Assunto honesto** (corresponde ao conteúdo); sem "melhor do mundo", "imperdível", "última chance", urgência ou escassez falsa; oferta real é informada, não gritada.
- **Compreensível com imagens off**: nada essencial só na imagem; alt útil.
- **Email-safe**: tabela + CSS inline + sem JS; CTA bulletproof com rótulo de ação; Outlook e dark mode considerados.
- **Descadastro presente** (placeholder neutro ou da plataforma); remetente identificado com honestidade.
- **Deliverability/compliance como alerta**, não como configuração: sinalizar SPF/DKIM/DMARC, requisitos de volume e base legal (LGPD) — sem resolver o jurídico nem sugerir lista comprada.
- **Personalização com fallback**; **open rate não é KPI absoluto**.
- **Benefício antes da característica** quando ajuda; a Performa não assina o e-mail.

### Email Quality Gate (silencioso)
Objetivo claro? · Segmento correto? · Assunto honesto? · Preheader complementa? · Info importante cedo? · Oferta/produto reais? · CTA e link corretos? · Mobile ok? · Funciona com imagens off? · Alt text? · Dark mode razoável? · Outlook-safe? · Descadastro presente? · Remetente identificado? · Placeholders resolvidos/listados? · Personalização com fallback? · UTM coerente? · Open rate fora do pedestal de KPI? · Precisa de alerta de compliance/entregabilidade? · Parece e-mail, não landing page? — se falhar, corrija.

## Formato da saída
1. **Versão texto** — assunto (variantes por ângulo), preheader e corpo em blocos, para revisar.
2. **Versão HTML** — um bloco de código email-safe (tabela, CSS inline, responsivo, bulletproof, alt), pronto para colar.
3. **Plain-text** (quando útil) — a alternativa text/plain legível, com os links essenciais.
4. **Placeholders a trocar** e os **alertas de entregabilidade** aplicáveis (descadastro/plataforma, autenticação, LGPD, dado faltante).

Sob pedido: só a copy, só o HTML de uma copy já aprovada, a adaptação para uma plataforma (merge tags certas), variações de assunto para teste, ou um template reutilizável. Nada de relatório por padrão.

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
