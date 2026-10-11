# Urgência Honesta — exemplos reais

## Exemplo A — Escassez real, por variante, com remoção automática
Entrada:
```
Produto: tênis de edição limitada, cor verde musgo
Estoque disponível por numeração (o sistema atualiza sozinho a cada venda):
  38: 0 · 39: 1 · 40: 2 · 41: 3 · 42: 0  (6 pares no total)
Lote: edição de 200 pares. "Não terá reposição desta cor" — o lojista ainda vai confirmar
Promoção: nenhuma · Tom: descolado, sem grito
```
Saída:
```
Checagem: há escassez real, mas ela é POR NUMERAÇÃO. "Últimos 6 pares" na página induziria quem
calça 38 ou 42 (esgotados) e quem calça 41 (3 pares) a achar que está acabando. Não há prazo:
nada de contador.

Fato                     | Estado     | Mensagem                                | Sai do ar quando        | No lugar
Estoque do 39 = 1        | verificado | "Última unidade no 39"                  | o 39 zerar → "Esgotado  | (nada)
                         |            | (só com o 39 selecionado)               | no 39"                  |
Estoque do 40 = 2        | verificado | "Restam 2 no 40"                        | o 40 zerar ou o dado    | (nada)
                         |            |                                         | falhar                  |
41 = 3                   | verificado | sem selo (3 não é "baixo" por padrão    | —                       | —
                         |            | nesta loja; o limite é decisão da loja) |                         |
Edição de 200 pares      | verificado | "Edição limitada de 200 pares"          | —                       | —
Sem reposição            | pendente   | NÃO publicar até o lojista confirmar    | —                       | "Edição limitada de 200 pares"

Carrinho: "Edição limitada · Restam 2 no 40". Nada de "você está levando uma das últimas" — o
carrinho não reserva o par, e o estoque pode mudar até o pagamento.
E-mail/WhatsApp: só para quem aceitou receber, uma vez, com o número atualizado no envio e sem
"últimos pares" somados.

Se a integração de estoque falhar: os números saem e fica só "Edição limitada de 200 pares"
(fail-closed). Não usar "poucas unidades" sem dado.
Para o desenvolvedor: o selo atualiza ao trocar a numeração; a página não pode ficar em cache
mostrando um número velho.
```

## Exemplo B — Auditoria de Black Friday
Entrada:
```
Página da Black Friday (27/11):
- Contador "Termina em 02:59:59" — volta para 03:00:00 a cada nova visita
- Faixa "ÚLTIMA CHANCE" — a loja faz a mesma promoção todo mês
- "Entrega garantida até o Natal" no botão de compra, sem considerar CEP nem pagamento
- Faixa "Frete grátis em tudo" — a ação acabou ontem, mas a página está em cache na CDN
- "De R$ 399 por R$ 249" — o produto custou R$ 299 nos últimos 3 meses
```
Saída:
```
Problema                       | Gravidade | Correção
Contador que reinicia          | bloqueio  | contador ligado ao prazo final no servidor:
                               |           | "Oferta válida até 23h59 de 27/11 (horário de Brasília)"
"Última chance" (promoção      | bloqueio  | remover. Se quiser destacar: "Preços desta seleção
 mensal)                       |           | válidos até 23h59 de 27/11"
"Entrega garantida até o Natal"| bloqueio  | "Pedidos com pagamento aprovado até [data e hora de corte]
                               |           | são expedidos até [data]. Prazo de entrega no cálculo de
                               |           | frete pelo seu CEP." (datas confirmadas com a logística)
"Frete grátis" vencido no cache| bloqueio  | tirar hoje e invalidar o cache; a faixa deve sair sozinha
                               |           | quando a ação expira
"De R$ 399" sem histórico      | bloqueio  | remover o "de". Mostrar só o preço atual, ou o "de" real
                               |           | (R$ 299), se for o caso. Preço anterior inventado é
                               |           | publicidade enganosa (CDC); na dúvida, revisão jurídica

Todos os canais (página, e-mail, WhatsApp, anúncios) usam o mesmo prazo e a mesma regra — o
anúncio não pode dizer uma data e a página outra.
Medição: comparar com a comunicação neutra, olhando margem e cancelamentos — não só cliques.
```

> Referência: só fato verificado vira urgência; o estoque é da numeração escolhida e não da soma;
> carrinho não é reserva; o contador vem do servidor e tem fuso; expedição não é entrega; "última
> chance" e preço "de" só com verdade; e quando o dado falha ou expira, a mensagem sai sozinha e
> fica uma neutra.
