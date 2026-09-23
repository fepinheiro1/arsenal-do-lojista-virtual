# Pós-Compra e Avaliação — exemplos reais

## Exemplo A — Produto com curva de uso (ajuda antes, sem gating)
Entrada:
```
Estado: entregue (plataforma confirma a entrega)
Loja: Cozinha Bruta — utensílios de ferro e madeira
Produto: frigideira de ferro fundido 26cm
Janela de uso: precisa curar e usar algumas vezes para ter opinião real
Destino da avaliação: página do produto (aba de avaliações) — deep link disponível
Apoio real: WhatsApp de atendimento + guia de primeira cura
Incentivo: não informado
```
Saída:
```
Readiness: PRIMEIRA IMPRESSÃO na entrega, PRONTO depois de alguns usos → o pedido de avaliação
espera a pessoa usar. Como há curva de uso (a cura), a AJUDA vem primeiro.

E-mail — PEDIR AVALIAÇÃO (após tempo de uso, a partir da entrega confirmada)
Assunto (2 opções, neutras):
  A) E a primeira fritada, como foi?
  B) Como está sendo cozinhar com ela?
Preheader: Conta pra gente como está sendo — do jeito que for.
Corpo: Sua frigideira de ferro fundido já teve tempo de pegar o ponto. Ferro fundido melhora com
o uso, e a sua experiência real ajuda quem ainda está entre uma e outra. Se puder contar como
está sendo — o que funcionou e o que não — a gente agradece.
E se a cura, o cabo ou qualquer coisa não saiu como você esperava, chama no WhatsApp que a gente
resolve; tem também o guia de primeira cura, se ajudar.
CTA: Contar minha experiência  → [deep link da aba de avaliações do produto]

(Repare: o link de avaliação aparece para todo mundo — inclusive para quem teve problema. O
suporte é oferecido EM PARALELO, não como um desvio que esconde a avaliação. Isso é o contrário
de "review gating".)

Momento de envio: a partir da ENTREGA confirmada + tempo de uso (aqui, alguns dias de cozinha) —
não "X dias após a compra".
Lembrete (se não avaliar): no máximo um, mudando o contexto (ex.: "alguma dúvida na cura?"),
e para de vez quando a avaliação chega. Sem "você ainda não avaliou".
Placeholders: deep link da avaliação, número do WhatsApp.
```

## Exemplo B — Marketplace + janela longa (incentivo barrado pela política)
Entrada:
```
Estado: entregue
Loja: Sono Raso — colchões
Produto: colchão de espuma D33 queen
Janela de uso: opinião real só depois de várias noites (produto de longo prazo)
Destino: página do produto DENTRO de um marketplace
Incentivo: a loja queria dar cupom por avaliar
```
Saída:
```
Dois travamentos antes de escrever:
1) READINESS LONGO PRAZO: pedir avaliação de colchão logo após a entrega não gera opinião útil.
   O pedido espera algumas noites de sono; um contato inicial pode ser só de ONBOARDING (como
   posicionar, período de adaptação), sem pedir nota ainda.
2) POLÍTICA DE INCENTIVO: o destino é um marketplace que restringe avaliação incentivada. Então
   o cupom NÃO entra atrelado ao review — seria contra as regras da plataforma e some com a nota.

E-mail — PEDIR AVALIAÇÃO (após período de adaptação)
Assunto: Depois de algumas noites, como está o sono?
Preheader: Sua opinião ajuda quem está escolhendo colchão.
Corpo: Colchão a gente só conhece de verdade depois de algumas noites — e agora sua experiência
tem valor real para quem está decidindo. Se puder contar como tem sido o sono e o conforto,
ajuda muito. Foto do quarto é opcional, só se você quiser.
CTA: Avaliar meu colchão  → [link real da página do produto no marketplace]

Incentivo: NÃO incluído neste e-mail (o marketplace de destino não permite avaliação
incentivada). Se a loja quiser recompensar o cliente, faça isso desacoplado da avaliação — um
mimo de pós-venda, sem exigir review em troca.
```

> Referência: o gatilho é a ENTREGA + a janela de uso da categoria (não "dias após a compra"); a
> ajuda vem antes quando há curva de uso; pede-se a avaliação e nunca a nota; o link aparece para
> todos (sem esconder do insatisfeito); e o incentivo só entra se for real E permitido no destino.
