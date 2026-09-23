# Sequência de Boas-Vindas — exemplos reais

## Exemplo A — Jornada de primeira compra (com saída por compra)
Entrada:
```
Origem/promessa: pop-up com cupom de primeira compra
Status do contato: lead novo
Marca/diferencial: Raiz Verde — cosméticos veganos, testados dermatologicamente, lotes pequenos
Produtos âncora: kit de limpeza facial, sérum de vitamina C
Oferta: cupom (valor não informado)
Plataforma: não informada
```
Saída:
```
Jornada: 3 e-mails (produto de decisão relativamente rápida; não precisa de 6). Objetivo:
primeira compra. Cada e-mail tem um papel; a jornada SAI se a pessoa comprar.

E-mail 1 — CUMPRIR A PROMESSA (imediato)
Assunto: Seu cupom de boas-vindas
Preheader: E uma palavra rápida sobre o que a gente faz por aqui.
Corpo: Que bom ter você. Como combinado, seu cupom: [preencher código e valor]. A Raiz Verde
faz skincare vegano, testado dermatologicamente, em lotes pequenos — fórmula fresca e cuidada.
Sem pressa: dá uma olhada com calma.
CTA: Conhecer a loja

E-mail 2 — EDUCAR / AJUDAR A ESCOLHER (quando teve tempo de olhar; ~2 dias)
Assunto: Por onde começar no skincare natural
Preheader: Dois passos simples para quem está começando.
Corpo: Não precisa de dez produtos, precisa dos certos.
1. Kit de limpeza facial — limpa sem ressecar, para todos os tipos de pele.
2. Sérum de vitamina C — o passo do viço, para usar de manhã.
Comece por um e sinta como a sua pele responde.
CTA: Ver o kit de início
(Este e-mail educa em vez de repetir "use o cupom" — valor antes de pressão.)

E-mail 3 — LEMBRETE (só se o cupom tiver validade real; ~5 dias; SÓ para quem não comprou)
Assunto: Seu cupom ainda está com você
Preheader: Quando quiser usar, ele está aqui.
Corpo: Passando para lembrar que seu cupom continua disponível [validade: preencher]. Na dúvida
por onde começar, o kit de limpeza é o caminho mais tranquilo. Qualquer coisa, é só responder.
CTA: Usar meu cupom

COMO AGENDAR
Gatilho: nova inscrição pelo pop-up. Intervalos: E1 imediato; E2 ~2 dias; E3 ~5 dias.
SAÍDA POR COMPRA (importante): se a pessoa comprar em qualquer ponto, retire-a desta jornada —
principalmente do E3, para não lembrar de um cupom de primeira compra a quem já comprou. Ela
deve migrar para o fluxo de pós-compra. Se o contato JÁ for cliente, não use esta jornada —
mande uma orientação/novidades.
```

## Exemplo B — Auditar (o fluxo manda cupom para quem já comprou)
Entrada:
```
Audita meu welcome: são 4 e-mails em dias fixos (0, 2, 4, 7). O de dia 7 sempre manda "última
chance do seu cupom". Uns clientes reclamaram que receberam isso DEPOIS de já ter comprado.
```
Saída:
```
O problema não é a copy — é a arquitetura do fluxo. Dois furos:

1. Falta SAÍDA POR COMPRA (o mais grave). O e-mail de dia 7 sai para todo mundo, inclusive quem
   já comprou. Isso irrita (a pessoa recebe "última chance de comprar" depois de comprar) e
   queima confiança. Corrija: coloque a condição "não comprou" na entrada do último e-mail e
   remova o contato da jornada assim que houver compra (migrando para o pós-compra).

2. "Última chance" com dia fixo é urgência artificial. Se o cupom tem validade real, comunique
   a data com calma; se não tem validade, não crie uma. Troque "última chance" por um lembrete
   útil ("seu cupom ainda está com você").

Sugestão menor: dias fixos (0/2/4/7) funcionam, mas o intervalo entre o e-mail educativo e o
lembrete deveria dar tempo real de decisão — avalie pelo seu ciclo de compra, não pelo número.
O resto do fluxo (boas-vindas + educação) pode ser mantido.
```

> Referência: o e-mail 1 cumpre a promessa (cupom, sem inventar o valor), cada e-mail tem um
> papel, o número vem da intenção (3, não 4 por regra), e a jornada REAGE — sai por compra e não
> manda "primeira compra" para quem já é cliente. Nada de urgência falsa.
