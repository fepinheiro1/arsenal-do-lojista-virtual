# Recuperação de Carrinho — exemplos reais

## Exemplo A — Carrinho abandonado (lembrete antes de desconto)
Entrada:
```
Evento: carrinho (plataforma confirma o item adicionado)
Loja: Passo Firme — calçados de couro masculinos
Estado do carrinho: 1 par (variante e preço vêm dinâmicos da plataforma)
Plataforma: tem deep link de retomada; NÃO reserva estoque
Objeções reais (do atendimento): dúvida de numeração; receio de couro que aperta
Apoios reais: troca de numeração sem custo em 30 dias; Pix e cartão; WhatsApp
Incentivo: não informado
```
Saída:
```
Fluxo de CARRINHO — 2 mensagens (sem incentivo, porque não há um real; o lembrete + a objeção
resolvem a maioria).

Mensagem 1 — LEMBRAR / RESTAURAR (algumas horas depois)
Assunto: Você deixou um par na Passo Firme
Preheader: Ele está aqui — é só continuar de onde parou.
Corpo: Vi que você separou um par por aqui. É só um clique para voltar de onde parou.
[bloco dinâmico: foto + nome + variante + preço do item, puxados da plataforma]
CTA: Voltar ao meu carrinho  → [deep link de retomada da plataforma]
(Não escrevi "guardamos seu carrinho" porque a sua plataforma não reserva estoque — prometer
isso seria falso. "Continuar de onde parou" é verdade.)

Mensagem 2 — TRANQUILIZAR / OBJEÇÃO (dia seguinte)
Assunto: Ficou na dúvida da numeração?
Preheader: A troca é sem custo — dá para acertar com calma.
Corpo: Comprar sapato sem provar dá um receio, a gente entende. Se a numeração não vier
perfeita, a troca é sem custo em até 30 dias, e o couro cede um pouco com o uso. Na dúvida
entre dois tamanhos, responda este e-mail ou chame no WhatsApp que a gente ajuda a escolher.
CTA: Retomar a compra  → [deep link]

REGRAS DE AUTOMAÇÃO
Gatilho: carrinho abandonado (confirmado). Janelas: M1 em ~2-4h; M2 em ~24h.
SAÍDA POR COMPRA: se a pessoa comprar, remova do fluxo na hora. Suprima também quem
descadastrou ou cujo item ficou indisponível.
Prioridade: se ela avançar para o checkout, o fluxo de checkout substitui este.
Incentivo: não incluído (não há cupom real). Se um dia houver, entra como M3 condicional —
nunca um desconto inventado só para "fechar".
```

## Exemplo B — Falha de pagamento (evento diferente, operacional)
Entrada:
```
Evento: falha de pagamento confirmada (cartão recusado no checkout)
Loja: Passo Firme
Estado: pedido montado, pagamento não aprovado
Plataforma: tem link para refazer o pagamento
```
Saída:
```
Isto NÃO é abandono de carrinho — é uma falha de pagamento. A mensagem é operacional, rápida e
sem nenhuma culpa: a pessoa QUERIA comprar.

Mensagem — RECUPERAR PAGAMENTO (rápida, minutos depois)
Assunto: Seu pagamento não foi concluído
Preheader: Pode ter sido só um detalhe do cartão — dá para tentar de novo.
Corpo: O seu pedido está montado, mas o pagamento não foi aprovado. Acontece — muitas vezes é
um detalhe do cartão ou do limite. Você pode tentar de novo em segundos, ou trocar para Pix.
CTA: Concluir meu pagamento  → [link para refazer o pagamento]
(Se ajudar: qualquer dúvida, é só responder este e-mail ou chamar no WhatsApp.)

REGRAS
Gatilho: falha de pagamento confirmada. Envio: rápido (minutos), porque a intenção é alta e a
janela é curta. Um único lembrete costuma bastar; não vire uma sequência de cobrança.
SAÍDA: assim que o pagamento for concluído, encerra. Não misturar com o fluxo de marketing de
carrinho — é outro evento, outro tom.
```

> Referência: o fluxo começa pelo EVENTO (carrinho ≠ falha de pagamento), não promete reserva
> que a plataforma não faz, usa deep link real, sai na hora quando há compra, e o desconto só
> entra se existir de verdade — a maioria das recuperações se faz removendo fricção, não gritando.
