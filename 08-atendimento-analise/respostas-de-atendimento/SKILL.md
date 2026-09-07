---
name: respostas-de-atendimento
description: Gera respostas prontas para as situações mais comuns de SAC e WhatsApp — dúvida de produto, prazo de entrega, troca/devolução e reclamação — no tom calmo e respeitoso da marca. Use quando precisar responder um cliente rápido sem soar robótico nem prometer o que a loja não confirmou.
---

# Respostas de Atendimento

## O que faz
Entrega uma resposta pronta para colar no WhatsApp, chat ou e-mail, no tom da sua loja: acolhe a pessoa, resolve (ou encaminha) e deixa claro o próximo passo. Cobre as situações que mais chegam no atendimento — dúvida sobre o produto, prazo de entrega, troca/devolução e reclamação — sem prometer nada que a loja ainda não confirmou.

## Quando usar
- Quando chega a mesma dúvida de sempre e você quer responder bem em segundos.
- Quando o cliente está irritado e você precisa de um tom que acalma sem se defender.
- Para padronizar as respostas da equipe de atendimento num tom só.

## O que a IA precisa de você
- `[situação]` — o que o cliente perguntou ou reclamou (cole a mensagem dele, se tiver).
- `[tipo]` — dúvida de produto, prazo, troca/devolução ou reclamação.
- `[tom da marca]` — como a loja fala (ex.: próxima e informal / formal e cuidadosa).
- `[dados confirmados]` (opcional) — prazo real, política de troca, status do pedido. O que você não passar, a IA marca `[preencher]` para você completar antes de enviar.

## Instruções (o cérebro da skill)
Monte a resposta sempre nesta sequência de 3 movimentos:

1. **Acolher** — reconheça a pessoa e o que ela trouxe, em uma frase. Sem "prezado cliente", sem frieza de call center. Se houver incômodo, valide antes de explicar ("faz sentido a sua dúvida", "entendo que você esperava receber antes").
2. **Resolver ou encaminhar** — responda de forma direta e específica. Se a resposta depende de um dado que você não tem (prazo exato, se cabe troca, onde está o pedido), **não invente**: escreva `[preencher: prazo real]`, `[preencher: política de troca]` etc. para o lojista completar.
3. **Próximo passo** — termine com uma ação clara: o que a pessoa faz agora, ou o que a loja vai fazer e quando.

Ajustes por tipo:
- **Dúvida de produto**: responda a dúvida e conecte ao uso real. Se não serve para o caso dela, diga com honestidade.
- **Prazo**: dê o prazo confirmado (ou `[preencher]`) e o que fazer se atrasar. Nunca cravar data que a loja não garantiu.
- **Troca/devolução**: explique o caminho em passos simples, no tom que resolve. Regra e prazo só se confirmados; senão `[preencher]`.
- **Reclamação**: assuma a responsabilidade sem drama e sem culpar o cliente. Uma frase de reconhecimento, uma solução concreta, um prazo real. Nunca se justificar em cima da falha da pessoa.

Gere **2 versões** da resposta: uma curta (para WhatsApp) e uma mais completa (para e-mail ou caso sensível).

## Regras de qualidade
- Nunca prometa prazo, reembolso ou disponibilidade que a loja não confirmou — marque `[preencher]`.
- Tom calmo e respeitoso, mesmo diante de grosseria. A loja resolve, não revida.
- Sem "infelizmente", sem começar pela negativa. Diga o que dá para fazer, não só o que não dá.
- Sem promessa exagerada ou garantia de resultado. Sem urgência ou pressão.
- Respeite o `[tom da marca]` — a fala é da loja, não de um script genérico.
- Frases curtas. A pessoa está no celular, muitas vezes com pressa ou chateada.

## Formato da saída
Duas respostas prontas para copiar:
- **Curta (WhatsApp)** — 2 a 4 linhas.
- **Completa (e-mail / caso sensível)** — com saudação e fechamento.

Ao final, liste em uma linha os campos `[preencher]` que ficaram pendentes, para o lojista completar antes de enviar.

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
