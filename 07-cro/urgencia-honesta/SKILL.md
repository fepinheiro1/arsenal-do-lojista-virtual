---
name: urgencia-honesta
description: Comunica urgência e escassez só quando existe um fato atual e verificável — estoque da variante escolhida, promoção com fim real (data, hora e fuso), lote ou pré-venda reais, corte de expedição — e retira a mensagem automaticamente quando o fato expira, some ou fica sem dado confiável. Separa prazo de escassez, expedição de entrega, carrinho de reserva; não usa contador que reinicia, "última chance" em promoção que volta nem preço "de" sem histórico. Escreve as mensagens e as regras de exibição e remoção; não tem acesso ao estoque nem publica nada. Use para criar, auditar, adaptar, revisar política ou especificar a integração de mensagens de urgência.
---

# Urgência Honesta

## O que faz
Transforma um **fato real e atual** — o estoque da variante que a pessoa escolheu, o fim de uma promoção, o tamanho de um lote, o horário de corte da expedição — numa mensagem clara que ajuda a decidir. E escreve junto as **regras** que mantêm a mensagem verdadeira: de onde vem o dado, de quanto em quanto tempo ele é atualizado, quando a mensagem sai do ar e o que aparece no lugar quando o dado falha.

Regra de ouro: **se não há evidência atual e verificável, não há urgência publicável.** Quando o dado está ausente, atrasado ou em conflito, a urgência **sai** e fica uma mensagem neutra (fail-closed). Urgência honesta informa; urgência falsa fabrica pressão — esta skill só faz a primeira, e não tem acesso ao estoque nem às promoções da loja: todo fato operacional depende de integração ou de confirmação.

## Quando usar
- Estoque realmente baixo de uma variante, promoção com fim definido, lote ou edição limitada, pré-venda, corte de expedição para uma data comercial.
- Auditar selos, contadores e frases de urgência que já estão no ar.
- Adaptar uma urgência real para página, carrinho, e-mail, WhatsApp e anúncio sem que os canais se contradigam.
- Especificar para quem desenvolve: fonte do dado, atualização, remoção automática, cache, fuso.

## O que a IA precisa de você
- `[produto ou campanha]` e onde a mensagem vai aparecer.
- `[o fato]` — o dado e **de onde ele vem**: estoque por variante (e se o sistema atualiza sozinho), promoção (início, fim, **fuso**, regras, produtos elegíveis), lote (tamanho, se haverá outro), pré-venda (janela, data prevista), corte de expedição (horário, dias úteis, condição de pagamento).
- `[o que acontece depois]` — repõe? volta a qual preço (e com que histórico)? esgota de vez?
- `[marca e tom]`.

Sem fato confirmado, a skill avisa e propõe a alternativa (benefício, diferencial, ajuda para decidir).

## Como funciona (por baixo)

**1. Fato antes de mensagem.** Cada afirmação é registrada com valor, origem, horário da leitura, responsável e validade. Estados: **verificado**, **desatualizado**, **expirado**, **desconhecido** ou **em conflito** — **só o verificado vira mensagem**. A geração nunca transforma dado incerto em certeza: texto autorizado, dado dinâmico e hipótese ficam separados.

**2. Prazo não é escassez.** Urgência é **tempo** (a oferta acaba); escassez é **quantidade** (o produto acaba). Uma não prova a outra: promoção acabando não significa estoque acabando.

**3. Estoque verdadeiro.**
- **Por variante**: mostrar só o saldo da cor/tamanho **selecionado** — nunca "últimas unidades" da coleção inteira porque uma cor ou um número está acabando.
- **Disponível ≠ físico**: considerar reservas, pedidos pendentes, devoluções, estoque de segurança e vários depósitos antes de mostrar um número.
- **Atualidade**: cada integração tem um tempo de validade do dado; se a atualização falhar, **o número sai**.
- **"Baixo" é relativo**: depende de demanda, reposição e política — "menos de 5" não é regra universal.
- **Reposição** confirmada ≠ estimativa; não inventar data nem declarar edição definitiva sem base. **Lote**: tamanho real, identificação e se pode haver outro lote (primeira tiragem não é exclusividade eterna). **Pré-venda**: dito claramente, com a janela e sem sugerir entrega imediata.
- **Carrinho não é reserva**: só falar em reserva se a plataforma bloqueia as unidades, por um prazo definido. E o estoque pode mudar entre a página e o pagamento — a mensagem nunca garante a unidade.

**4. Tempo verdadeiro.** Promoção guardada com início, fim, **fuso horário**, regras e produtos elegíveis — nada de data escrita à mão que fica velha. **Contador só derivado de um prazo final salvo no servidor**: nunca reinicia por sessão, recarga ou visitante novo. Fuso e horário de verão testados. "Volta ao preço de antes" só com regra e **histórico real** de preço — preço "de" inventado é publicidade enganosa. Cupom com mínimo, exclusões, uso único, quem pode usar, validade e se acumula com outras promoções. Promoção que volta igualzinha todo mês **não é "última chance"**.

**5. Entrega verdadeira.** "**Expedido** até" ≠ "**entregue** até". O prazo depende de CEP, modalidade, transportadora, dia útil, feriado, horário de corte e **pagamento aprovado** — o marco é a aprovação, não o clique em comprar (Pix pendente não conta). Datas comerciais conferidas no calendário brasileiro, sem importar data estrangeira por padrão.

**6. Mensagem que informa.** "Oferta válida até 23h59 de 28/11 (horário de Brasília)" vale mais que ameaça de arrependimento. Cada canal (selo na página, carrinho, checkout, e-mail, WhatsApp, anúncio) adapta o tamanho, **não o fato**. Sem fato, a alternativa é benefício, diferencial ou ajuda para decidir. **Proibido**: fila falsa, contador que reinicia, recusa humilhante, obstáculo para sair, escassez fabricada, "X pessoas vendo agora" sem dado. E sem insistir: o mesmo alerta não aparece em toda etapa nem se repete à exaustão nos canais diretos.

**7. Operação que não deixa a mentira escapar.** Fonte da verdade: o sistema de e-commerce/ERP diz a disponibilidade; o motor de promoções diz preço e validade — sem duplicar regra em texto manual. Sincronização por eventos quando houver, consulta periódica com limite e reconciliação; eventos fora de ordem tratados. **Fail-closed**: dado crítico ausente, atrasado ou em conflito → urgência sai, mensagem neutra fica. Trocar a variante atualiza o selo sem recarregar a página, quando possível. Ao expirar, zerar o estoque ou perder elegibilidade, **selo, contador e botão promocional saem sozinhos**. **Cache e CDN** invalidados — página estática não pode continuar mostrando oferta vencida. E todos os canais compartilham **o mesmo fato e a mesma versão**.

**8. Acessível.** Contador **não anuncia cada segundo** para leitor de tela: prazo final legível, atualização discreta. Contraste, zoom, tela pequena, linguagem simples e informação que não depende só da cor.

**9. Lei, política e privacidade.** No Brasil, o Código de Defesa do Consumidor exige oferta transparente e proíbe publicidade enganosa — quando houver dúvida (preço "de/por", condição de oferta), pedir revisão jurídica. Meta, Google e marketplaces têm regras próprias para urgência e preço. Não divulgar contagem de visitantes ou compras atribuída a pessoas sem base e sem proteção de dados.

**10. Medir sem se enganar.** Testar **urgência real × comunicação neutra** — nunca inventar uma condição só para montar o grupo de teste. Métrica principal: conversão e **margem** incrementais, não clique no selo ou adição ao carrinho. Proteção: cancelamentos, reclamações, devoluções, atendimento, satisfação e confiança. Grupo de controle quando viável: coincidência no tempo não prova efeito. Segmentar por elegibilidade e contexto, nunca explorando vulnerabilidade ou atributo pessoal.

## Instruções (o cérebro da skill)
1. Identifique o **modo** (criar / auditar / adaptar / variações / checar política / especificar integração / remover / lote).
2. **Registre o fato** com origem, horário e validade, e classifique o estado. Se não for **verificado**, não há urgência — vá para a alternativa.
3. Separe **prazo, escassez e entrega**; aplique as regras de cada um (variante, disponível, fuso, histórico de preço, pagamento aprovado).
4. Escreva a **mensagem por canal** a partir do mesmo fato, com a **condição de remoção** e a **mensagem neutra de reserva** (fallback).
5. Defina a **operação**: fonte, atualização, fail-closed, cache, consistência entre canais, acessibilidade.
6. Rode os **Quality Gates** factual e operacional e entregue.

## Regras de qualidade
- **Só fato verificado** vira urgência; desatualizado, expirado, desconhecido ou em conflito → mensagem neutra.
- **Prazo ≠ escassez ≠ entrega**; expedido ≠ entregue; carrinho ≠ reserva.
- **Estoque da variante selecionada**, disponível de verdade, atualizado; nada de soma da coleção.
- **Contador do servidor**, com fuso; nunca reinicia.
- **Preço "de" só com histórico**; "última chance" só se for mesmo a última.
- **Remoção automática** ao expirar ou zerar; cache invalidado; canais com o mesmo fato.
- **Sem padrão manipulador** e sem insistência.
- **Acessível**: contador que não grita para leitor de tela; não depende só de cor.
- **CDC e políticas de canal** considerados; revisão jurídica quando houver dúvida.
- **Medição com controle**, margem como métrica, sem condição inventada.
- **Nada inventado**: número, data, hora, lote, reposição, preço anterior. Pendência fica fora do texto pronto.
- **Voz da marca, não da Performa**, em tom calmo e confiante.
- **Informado ≠ verificado**: nota, número de pedidos, tamanho de lote que vieram do lojista são "informados"; "verificado" só o que veio do sistema ou de fonte conferida.
- **Limite de "estoque baixo" é da loja**: sem o número definido pelo lojista, a skill pergunta ou usa um exemplo declarado.
- **Toda conta por código; alerta sem número novo**: com código disponível, nenhuma conta ou contagem de cabeça — nem nos alertas. Alerta e observação só repetem números já calculados (nos testes, a IA acertava a conta principal e errava os números "de passagem").

### Urgency Quality Gates (silenciosos)
**Factual:** valor sem fonte? · data ou hora expirada? · estoque somado usado como se fosse da variante? · exclusividade ou "sem reposição" sem prova? · preço anterior sem histórico? · "última chance" em promoção recorrente? · expedição tratada como entrega? · carrinho tratado como reserva?
**Operacional:** atualização definida? · fuso correto? · cache invalidado? · canais coerentes? · remoção automática? · fail-closed quando o dado falha? · acessível? — se falhar, a urgência não é publicada.

## Formato da saída
**Modo simples (padrão)** — para cada mensagem: **fato** (estado, fonte, horário) · **mensagem curta** · **onde usar** · **quando sai do ar** · **mensagem neutra no lugar** · pendências. Se não houver fato verificado: a alternativa sem urgência.

**Modo técnico (sob pedido):** regra (fonte, tempo de validade do dado, evento, fallback), registro de auditoria, casos de teste (troca de variante, estoque de 0 para 1, expiração, fuso, cupom inelegível, queda da integração, cache atrasado, carrinho sem reserva) e critérios de implantação.

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
