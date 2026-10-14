# Texto de Retargeting — exemplos ilustrativos

> Casos de demonstração: o anúncio só afirma o que veio na entrada — o que depende de confirmação fica fora do texto.

## Exemplo A — Verba curta, objeção com e sem evidência
Entrada:
```
Produto: tênis casual de couro · Objetivo: vender · Página: a do produto
Eventos: Pixel registra produto visto, carrinho e compra (conferido pelo lojista)
O que se sabe: "dúvida de numeração" aparece muito no atendimento; "frete caro" é palpite
Argumentos reais: troca de numeração em até 30 dias; frete grátis acima de R$ 199; até 6x sem
  juros; 4,7 de 5 em 800 avaliações (pode citar)
Orçamento: R$ 30/dia · Também manda e-mail de carrinho abandonado
O lojista sugeriu: "Seu par está guardado no carrinho" e "Ainda pensando no seu par?"
```
Saída:
```
Ajustes antes de escrever:
- "Seu par está guardado no carrinho" e "Ainda pensando no seu par?" revelam rastreamento e
  presumem o que a pessoa pensa. Além disso, o anúncio pode chegar a quem nunca visitou a loja.
  Os dois saem.
- Frete é palpite: entra como hipótese de teste, não como "o que te segurou".

Estrutura: UMA campanha com R$ 30/dia, um público (viu o produto OU adicionou ao carrinho, últimos
14 dias — janela como hipótese, ajustar ao ciclo de compra) e duas mensagens em teste.
Excluir: quem comprou nos últimos 30 dias (a exclusão tem atraso; aceitar algum vazamento).

MENSAGEM 1 — Numeração (evidência: atendimento)
Hipótese: a dúvida de tamanho trava parte das compras.
Texto principal: Tênis casual de couro, com troca de numeração em até 30 dias — dá para escolher
  o número com tranquilidade. 4,7 de 5 em 800 avaliações.
Título: Troca de numeração em até 30 dias
Descrição: Couro, 4,7 de 5 em 800 avaliações.
CTA: Ver produto
Prova: a política de troca e as avaliações. Se a página tiver tabela de medidas, vale citar
  ("tabela de medidas na página") — a entrada não diz que tem, então ficou fora.

MENSAGEM 2 — Condições de compra (hipótese: frete/pagamento)
Hipótese: deixar claras as condições ajuda quem estava decidindo. Ainda NÃO se sabe se o frete
  é o motivo — este teste ajuda a descobrir.
Texto principal: Tênis casual de couro: frete grátis acima de R$ 199 e até 6x sem juros. Troca de
  numeração em até 30 dias.
Título: Frete grátis acima de R$ 199
Descrição: Até 6x sem juros.
CTA: Comprar agora

Fora, de propósito: "compra segura" (vago — as condições concretas dizem mais) e qualquer cupom
(não há incentivo informado; e cupom recorrente ensina a abandonar o carrinho).

Coordenação: o e-mail de carrinho já fala de retomada. O anúncio não repete a mesma mensagem nem
oferta — fica com tamanho e condições.
Medição: com público pequeno, acompanhar a frequência. Parte de quem comprar depois do anúncio
compraria de qualquer jeito; quando o volume permitir, um holdout mostra o efeito real.
```

## Exemplo B — Auditoria de anúncio dinâmico de catálogo
Entrada:
```
Retargeting dinâmico de catálogo rodando há 2 meses. O lojista conta:
- o evento "início de checkout" dispara também na página do carrinho
- o pixel envia o ID interno do produto; o catálogo usa o SKU como ID
- o tênis que mais aparece nos anúncios esgotou há 1 semana
- o texto fixo do anúncio diz "15% OFF com o cupom VOLTA15" — o cupom expirou no mês passado
- o banner de cookies não está integrado ao pixel
- "o ROAS está ótimo, 9x"
```
Saída:
```
Problema                                   | Severidade | O que fazer
Cupom VOLTA15 expirado no texto fixo       | bloqueio   | tirar do anúncio hoje: oferta falsa
IDs do pixel ≠ IDs do catálogo             | bloqueio   | alinhar os IDs; sem isso a personalização
                                           |            | mostra o produto errado ou nenhum
Produto esgotado ainda anunciado           | bloqueio   | conferir se o catálogo atualiza o estoque;
                                           |            | não insistir no SKU esgotado
"Início de checkout" disparando no carrinho| atenção    | corrigir a definição do evento; até lá, os
                                           |            | públicos de checkout e carrinho estão misturados
Banner de cookies sem integração           | atenção    | revisar com quem cuida da parte legal e técnica:
                                           |            | consentimento não se presume
ROAS de 9x                                 | atenção    | retargeting é onde o crédito mais se confunde
                                           |            | com venda nova; avaliar com holdout e margem

Texto fixo sugerido para o anúncio dinâmico (vale para qualquer produto do catálogo, sem revelar
rastreamento):
Texto principal: Troca de numeração em até 30 dias e frete grátis acima de R$ 199.
Título: o nome do produto (usar o campo dinâmico do catálogo que o Gerenciador oferece — não
  digitar uma sintaxe inventada)
CTA: Comprar agora

Ordem: primeiro os três bloqueios, depois o evento e o consentimento. Só então reavaliar o
desempenho — com os dados corrigidos.
```

> Referência: a mensagem não revela rastreamento nem presume o que a pessoa pensa; objeção com
> evidência é tratada, palpite vira teste; compradores são excluídos; não há cupom nem urgência
> inventados; e os problemas técnicos (evento, IDs do catálogo, estoque, consentimento) aparecem
> como dependência, não como algo que a IA configurou.
