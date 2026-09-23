# Reativação de Clientes — exemplos reais

## Exemplo A — Durável/discricionário: winback pela novidade (não pelo "não abriu")
Entrada:
```
Loja: Trilha Livre — roupas e equipamento para trilha e camping
Estado do cliente: comprou 2x, última compra há 150 dias; produto durável (não repõe sozinho)
Ciclo esperado: não é consumível — 150 dias não é "acabou", é fim do ciclo de interesse
Sinais de engajamento: abriu alguns e-mails, sem clique; visitou o site uma vez no mês passado
O que há de novo (real): linha de corta-vento impermeável; categoria nova de mochilas cargueiras;
  envio no mesmo dia para pedidos até 14h
Incentivo: não informado
```
Saída:
```
Classificação: WINBACK (durável — não force recompra do mesmo item; reacenda por novidade e
complemento). A visita recente ao site é um sinal de engajamento melhor que o open — use-a como
gatilho, não "quem não abriu".

E-mail 1 — DESCOBRIR (o que mudou)
Assunto (2 opções): A) Tem equipamento novo pra sua próxima trilha  ·  B) A temporada abriu — e a loja mudou
Preheader: Corta-vento impermeável, cargueiras novas e envio mais rápido.
Corpo: Desde a sua última trilha com a gente, mudou bastante coisa boa por aqui.
- Corta-vento impermeável — encara a chuva no caminho sem peso.
- Mochilas cargueiras — categoria nova, para as travessias mais longas.
- Envio no mesmo dia — pedidos até 14h saem no mesmo dia.
Boa hora para dar uma olhada no que é novo.
CTA: Ver as novidades  → [link real]

E-mail 2 — RECOMENDAR (só para quem NÃO clicou/visitou — não "quem não abriu")
Gatilho: sem clique nem visita após o e-mail 1 (não a abertura). Papel: outro ângulo do novo.
Assunto: A cargueira nova já está em estoque
Corpo: A linha de mochilas cargueiras que faltava chegou. Se a sua próxima aventura é das longas,
vale conhecer — e o envio no mesmo dia ajuda a chegar tudo a tempo.
CTA: Conhecer as cargueiras  → [link real]

REGRAS
Segmento: 2ª compra, 150 dias, durável. SAÍDA: comprou ou clicou/visitou → sai do winback e volta
ao lifecycle normal. Incentivo: não incluído (não há cupom real); se houver, entra condicional, não
como isca. Se nem o e-mail 2 gerar sinal, este contato caminha para o fluxo de sunset (exemplo B).
```

## Exemplo B — Consumível no ciclo vs. dormente: replenishment ≠ winback, e o sunset
Entrada:
```
Loja: Grão Nosso — café em grãos (assinatura avulsa, recompra manual)
Dois clientes na mesma exportação de "inativos há 90 dias":
  Cliente 1: comprava pacote de 1kg a cada ~35 dias; última compra há 40 dias
  Cliente 2: comprou uma vez, há 400 dias; nunca mais abriu, clicou ou visitou
Novidade real: novo torra média do sítio parceiro
Incentivo: cupom de 10% disponível, margem permite no cliente certo
```
Saída:
```
Os dois estão na MESMA lista de "90 dias", mas são problemas diferentes:

Cliente 1 = REPLENISHMENT (não winback). Ele consome ~1kg/35 dias; 40 dias é "está acabando",
não "sumiu". Mensagem é lembrete gentil, sem culpa e sem desconto (ele não precisa).
Assunto: Seu café deve estar no fim
Corpo: Pelo seu ritmo, o pacote de 1kg deve estar acabando por aí. Repor leva um minuto — e, se
quiser variar, chegou uma torra média nova do sítio parceiro.
CTA: Repor meu café  → [deep link do último produto, se a plataforma suporta]
(Sem "seu café acabou" afirmado — a gente estima pelo ritmo, não sabe o consumo real. Incentivo:
NÃO, o lembrete basta; cupom aqui só ensinaria a esperar desconto.)

Cliente 2 = DORMENTE → RE-PERMISSÃO / SUNSET (não é winback comum). 400 dias, zero engajamento:
insistir queima a entregabilidade da base. Uma única mensagem de confirmação de interesse.
Assunto: Ainda quer receber o Grão Nosso?
Corpo: Faz tempo que a gente não se fala. Se ainda quiser novidades e a torra nova, é só confirmar
abaixo. Se preferir, dá para ajustar a frequência — ou pausar, sem problema.
CTA primário: Quero continuar recebendo   ·   Secundário: Ajustar frequência / pausar
REGRA: se não houver clique/confirmação, este contato sai do marketing ativo (sunset) — não é
"apagar cliente", é proteger reputação e a caixa de entrada de quem engaja. Aqui o cupom de 10%
pode entrar como último empurrão, porque o valor de recuperar já compensa o risco de churn real.
```

> Referência: o mesmo "inativo há 90 dias" vira intervenções diferentes conforme o CICLO e o
> ENGAJAMENTO — replenishment gentil para quem está no ritmo, novidade para o durável, re-permissão/
> sunset para o dormente. Nada de culpa, nada de "não abriu" como gatilho, e o cupom só onde o gate
> aprova.
