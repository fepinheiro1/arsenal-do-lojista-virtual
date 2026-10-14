---
name: otimizacao-de-checkout
description: Diagnostica o checkout com níveis de evidência (observado, medido, relatado, hipótese, não verificado) — funil com eventos e denominadores explícitos, abandono separado de falha técnica (gateway, recusa, antifraude), campos com justificativa, frete e custo total, Pix e cartão como fluxos distintos, confiança, privacidade, acessibilidade e o que a plataforma realmente permite mudar. Não inventa frete, prazo, taxa, capacidade de plataforma nem aumento de conversão, não remove campo exigido sem investigar e não contorna antifraude. Use para auditar o fluxo, diagnosticar com dados ou planejar melhorias com teste e volta atrás.
---

# Otimização de Checkout

## O que faz
Percorre o caminho do carrinho até o **pagamento aprovado** e localiza onde a compra trava — mas separando o que foi **visto**, **medido**, **relatado** e o que é **hipótese**. Distingue a pessoa que **desistiu** da compra que **falhou** (erro de formulário, gateway fora, cartão recusado, antifraude, Pix que expirou). E entrega um plano executável: o que é ajuste rápido, o que é projeto, com quem depende (plataforma, gateway, desenvolvedor), como medir e como voltar atrás.

Regra de ouro: **quem chegou ao checkout quer comprar — o trabalho é tirar atrito e falha do caminho sem inventar dado, sem remover o que é exigido e sem prometer "+X% de conversão".** Pedido criado não é pagamento aprovado.

## Quando usar
- Muita gente começa o checkout e pouca termina.
- Depois de trocar tema, gateway ou plataforma.
- Cliente relata erro, falta de meio de pagamento ou compra que "não foi".
- Antes de escalar tráfego.

## O que a IA precisa de você
- `[o fluxo]` — URL, prints (celular primeiro) ou a descrição das etapas e campos. A skill diz o que examinou.
- `[plataforma]` — e, se souber, versão/plano, checkout próprio ou externo, gateway e antifraude.
- `[país, dispositivo principal, meios de pagamento e objetivo]`.
- `[regras reais]` — frete (mínimo, regiões, exclusões), prazos, parcelamento e juros, troca.
- (opcional) **dados**: eventos do funil (início do checkout, frete, pagamento, compra), pedidos criados na plataforma, aprovações e recusas no gateway, Pix gerados e pagos, erros; **relatos** do atendimento.

## Como funciona (por baixo)

**1. Evidência antes de veredito.** Cada achado tem nível e fonte: **observado** (visto no fluxo ou print), **medido** (dado), **relatado** (atendimento, cliente, lojista), **hipótese** ou **não verificado**. Descrição do lojista é relato — **a skill nunca diz que navegou** pelo checkout se só recebeu a descrição. Auditoria por heurística, diagnóstico com dados e teste com usuários são coisas diferentes.

**2. O funil com definições explícitas.** Sessão, carrinho, início do checkout, frete informado, pagamento iniciado, **pedido criado** e **pagamento aprovado** são etapas diferentes, cada uma com seu evento (nome, momento de disparo, origem, deduplicação). Toda taxa diz o **denominador e a janela** — não se comparam taxas com bases diferentes. Segmentar (celular × computador, novo × recorrente, origem, meio de pagamento, região) só com volume. E **conferir os dados antes de concluir**: consentimento, bloqueadores, domínio do gateway diferente, eventos duplicados, pagamento assíncrono — GA4, plataforma e gateway quase sempre mostram números diferentes, e é preciso reconciliá-los.

**3. Desistência ≠ falha.** Abandono voluntário, erro de validação, gateway indisponível, recusa do emissor, antifraude, autenticação 3-D Secure, timeout, cupom inválido e estoque que acabou no meio do caminho são problemas diferentes — catalogados por frequência e gravidade. **Nunca recomendar contornar autenticação obrigatória ou antifraude.**

**4. Estrutura do fluxo.** **Menos telas não é automaticamente melhor**: pesam a carga de cada etapa, a sensação de progresso e o retrabalho. Em checkout de várias etapas, indicar o progresso e permitir voltar sem perder dados. Compra como convidado quando a operação permite — sem remover autenticação que é necessária (assinatura, B2B, exigência legal); conta pode ser oferecida depois da compra, com consentimentos separados.

**5. Campos com justificativa.** Inventário de cada campo e **por que** é pedido: entrega, cobrança, antifraude ou obrigação fiscal. **CPF, telefone, data de nascimento ou outro dado podem ser exigidos** pela operação, pelo gateway ou pelo tipo de produto — investigar antes de mandar remover. Máscaras tolerantes, teclado e preenchimento automático certos (colar não pode quebrar), CEP que preenche o endereço mas aceita correção manual e trata CEP inválido, erro mostrado **junto do campo**, em linguagem que diz o que fazer. Dados **não se perdem** depois de um erro, recarregamento, volta de etapa ou falha de pagamento (com exceção dos dados de cartão). No celular: teclado numérico para número e CEP, foco previsível, botão acessível acima do teclado. Carteiras digitais e preenchimento automático só se a plataforma suporta.

**6. Custo e entrega sem surpresa.** Resumo do pedido revisável (itens, variantes, quantidades, descontos). Frete e prazo **cedo quando viável**, deixando claro que dependem do CEP e do método. **Total completo antes de confirmar** (subtotal, frete, taxas, descontos). Frete grátis com o **mínimo, as regiões e as exclusões reais** — barra de "faltam R$ X" só com regra verificável. Prazo separando postagem, transporte e entrega estimada — sem data absoluta sem dado.

**7. Pagamento por contexto — e Pix e cartão são fluxos diferentes.** Meios de pagamento pelo público e mercado, não por moda. **Pix**: expiração real, QR e copia-e-cola, caminho de volta à loja, confirmação assíncrona — **pedido criado não é pagamento confirmado**; separar cobrança gerada, paga, expirada e estornada, e proteger contra pedido duplicado. **Cartão**: parcelas, juros e total reais; erro de autorização que orienta o próximo passo sem expor dado. **Falha de pagamento**: tentar de novo, trocar de método e recuperar o pedido **sem cobrar duas vezes** (o sistema precisa tratar a repetição com segurança).

**8. Cupom, estoque e sessão.** Cupom que aplica, remove, explica por que não vale e recalcula o total — sem regra de desconto fictícia. Estoque que acaba durante o checkout com mensagem clara — **sem prometer reserva que não existe** (a mesma lição da `recuperacao-de-carrinho`: "seu carrinho está guardado" só se for verdade). Sessão que expira, retorno do gateway e carrinho persistente com retomada segura, sem expor dado de outra pessoa. Checkout externo ou redirecionado: mudança visual, perda de confiança e rastreamento entre domínios.

**9. Confiança, privacidade e acessibilidade.** HTTPS, identificação de quem vende, políticas reais, checkout reconhecível — **selo de segurança só se verdadeiro**, nunca fabricado. **LGPD**: pedir só o que tem finalidade, proteger dado pessoal, separar consentimento de marketing do que é necessário para o contrato. **Cartão**: número e código de segurança **nunca** em ferramenta de análise, log ou gravação; tokenização pelo provedor. Gravação de sessão só com mascaramento de dado pessoal. Acessibilidade (WCAG 2.2): rótulo persistente (placeholder não é rótulo), foco visível, erros anunciados, contraste, alvo de toque, autenticação acessível. Velocidade: LCP, INP e CLS com dados de campo quando houver; testar rede lenta e celular intermediário — velocidade é **hipótese de impacto**, não promessa.

**10. O que a plataforma deixa mudar.** Tema, apps/extensões, extensões oficiais de checkout ou customização restrita: **confirmar plataforma, versão e plano antes de prescrever**. Shopify, VTEX, Nuvemshop, Tray e outras têm limites diferentes, que mudam — quando depende de versão, app ou contrato, a skill diz **"não sei, conferir"** em vez de prometer.

**11. Priorizar, testar e medir.** Gravidade, alcance, confiança, esforço e dependência — pesos de ICE/RICE ajudam, mas não são ciência. **Ajuste rápido** (texto, rótulos, ordem visual, mensagem de erro) é diferente de **projeto** (gateway, antifraude, performance, arquitetura). Teste A/B com hipótese, métrica principal, **proteção** (taxa de aprovação de pagamento, fraude, devolução, ticket, margem, chamados no atendimento, erros), sorteio, amostra e duração — sem encerrar no primeiro resultado bom. Teste com usuários e gravações (com dado mascarado) explicam comportamento, mas não provam causa. Resultado reportado com incerteza; **nunca "+X% de conversão" por heurística**. A mensagem para quem abandonou é com a `recuperacao-de-carrinho` (frente 04); a página de produto, com a `auditoria-pagina-de-produto`.

## Instruções (o cérebro da skill)
1. Identifique o **modo** (auditar o fluxo / diagnosticar com dados / desenhar e replanejar) e declare **o que foi examinado**.
2. Defina o **funil e os eventos**; com dados, confira a qualidade e reconcilie as fontes antes de apontar gargalo.
3. Separe **desistência de falha** e percorra **estrutura, campos, custo e entrega, pagamento (Pix ≠ cartão), cupom/estoque/sessão, confiança, privacidade e acessibilidade** — celular primeiro.
4. Registre cada achado com **nível de evidência e fonte**; investigue o porquê antes de mandar remover qualquer exigência.
5. Cheque o que a **plataforma** permite; **priorize** e separe ajuste rápido de projeto.
6. Defina **medição, teste e volta atrás**, rode o **Quality Gate** e entregue.

## Regras de qualidade
- **Nível de evidência e fonte** em cada achado; nunca afirmar ter navegado sem ter navegado.
- **Desistência ≠ falha técnica**; Pix e cartão tratados como fluxos distintos; pedido criado ≠ pago.
- **Nada inventado**: frete, prazo, taxa, parcelamento, política, capacidade da plataforma, estatística, aumento de conversão.
- **Campo exigido não se remove sem investigar**; antifraude e 3-D Secure não se contornam.
- **Total sem surpresa** antes de confirmar; frete grátis com regra real.
- **Falha de pagamento recuperável** sem cobrança duplicada; dados preservados (menos cartão).
- **Sem prometer reserva** que não existe; selo só verdadeiro.
- **LGPD e cartão**: minimização, consentimentos separados, nenhum dado de cartão em análise, gravação mascarada.
- **Celular e acessibilidade** verificados (ou não verificados).
- **Plataforma confirmada** antes de prescrever; "não sei" quando depende de versão ou contrato.
- **Ajuste rápido ≠ projeto**; teste com proteção; resultado com incerteza.
- **Linguagem simples** para o lojista; detalhes técnicos sob demanda.
- **Print que a IA não vê não é descrito**: o que depende dele fica "não verificado".

### Checkout Quality Gate (silencioso)
Declarou o que examinou? · Cada achado tem nível de evidência e fonte? · Taxas com denominador e dados conferidos? · Desistência separada de falha? · Pix pendente tratado como não pago? · Falha de pagamento sem cobrança dupla? · Algum campo removido sem investigar? · Frete, prazo ou taxa inventados? · Total completo antes de confirmar? · Prometeu reserva ou selo inexistente? · Dado pessoal e de cartão protegidos? · Celular e acessibilidade vistos? · Capacidade da plataforma confirmada? · Ajuste rápido separado de projeto? · Teste com métricas de proteção? · Prometeu aumento de conversão? — se falhar, corrija.

## Formato da saída
1. **O que foi examinado** e **resumo simples**: onde a compra trava, com o grau de certeza.
2. **Achados**: `Etapa | Achado | Evidência (nível e fonte) | Gravidade | Ação | Dependência (plataforma / gateway / dev / lojista) | Como validar`.
3. **Plano**: ajustes rápidos e projetos, com esforço; testes com hipótese e proteção; o que medir; como voltar atrás.
4. **Pendências**: regras reais a confirmar, dados que faltam, o que vai para outras skills.

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
