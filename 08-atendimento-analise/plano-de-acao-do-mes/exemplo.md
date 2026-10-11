# Plano de Ação do Mês — exemplos reais

> As contas foram feitas por código. Nenhum resultado é promessa.

## Exemplo A — Loja pequena, números aproximados
Entrada:
```
Loja de cosméticos naturais. "Muita gente coloca no carrinho e some." Descrições fracas.
Instagram sem constância.
Números (estimativa da lojista, de cabeça): ~6.000 visitas/mês, conversão ~1,1%, ticket R$ 95.
Abandono de carrinho: "alto", mas não sabe a %. Tráfego quase todo do Instagram.
Meta: recuperar carrinhos e melhorar a conversão.
Equipe: a lojista + uma assistente 20 h/semana. Verba: R$ 300 para ferramentas.
```
Saída:
```
Leitura (certeza baixa, números estimados): 6.000 × 1,1% ≈ 66 pedidos × R$ 95 ≈ R$ 6.270 por mês
em pedidos (calculado sobre estimativas; não é lucro). "Abandono alto" ainda não é um dado.
Hipóteses para a conversão baixa — sem veredito:
  (a) tráfego do Instagram chega com pouca intenção de compra (mix de tráfego);
  (b) atrito no checkout (frete, prazo, pagamento);
  (c) página de produto que não responde dúvidas.
O que separa uma da outra: o funil por etapa (visualização → carrinho → checkout → compra) e a
origem de cada venda — e hoje isso não é medido.

Plano (cabe em ~20 h/semana da assistente + parte do tempo da lojista)
Ação                                   | Dono       | Semana | Entrega / concluído quando       | Medir / vigiar               | Skill de apoio
1. Conferir a medição: eventos de      | lojista    | 1      | os 4 eventos aparecem e batem    | % de abandono REAL /          | (tarefa manual)
   carrinho, checkout e compra         |            |        | com os pedidos da plataforma     | pedidos plataforma × GA4      |
2. Ligar a recuperação de carrinho     | assistente | 1–2    | fluxo ativo, com saída na compra | carrinhos que voltaram (não é | recuperacao-de-carrinho
   (e-mail, com consentimento)         |            |        | e sem cupom por padrão           | receita a mais) / reclamações |
3. Reescrever os 5 produtos mais       | assistente | 2–3    | 5 páginas com fatos do rótulo,   | carrinho ÷ visualização das 5 | descricao-que-converte,
   vistos, com as dúvidas reais        |            |        | sem promessa de efeito           | (leitura qualitativa: tráfego | faq-do-produto
                                       |            |        |                                  | pequeno não dá teste)         |
4. Ler o funil e decidir o próximo mês | lojista    | 4      | qual hipótese (a, b ou c) os     | —                             | —
                                       |            |        | dados reforçaram                 |                               |

Ficou de fora, de propósito:
- Calendário de Instagram: não há capacidade junto com as ações 2 e 3, e mais tráfego antes de
  entender o funil não resolve. Volta no próximo mês, se a hipótese (a) for descartada.
- "Colocar avaliações nos produtos": só se a loja já tiver avaliações reais; senão, a coleta entra
  pelo pós-compra (pos-compra-avaliacao) no próximo mês.
Dependência: a ação 1 vem antes de qualquer conclusão sobre abandono.
Simulação, só para ver o peso da conversão: se a conversão fosse 1,3% com as mesmas visitas e o
mesmo ticket, seriam 78 pedidos e R$ 7.410 (R$ 1.140 a mais, antes dos custos). É conta, não meta.
Revisão semanal (sexta, 15 min): feito / travado / o que os dados mostraram / próxima decisão.
```

## Exemplo B — Black Friday, com dados que não batem e um checkout falhando
Entrada:
```
Meta de novembro: R$ 260.000 em pedidos
Outubro, pela plataforma: 780 pedidos, R$ 187.200 (ticket R$ 240); GA4: 640 compras; 52.000 sessões
Atendimento: desde 3 dias atrás, clientes relatam "erro ao gerar o Pix"
O produto âncora da campanha está sem estoque até dia 20; a reposição está confirmada pelo fornecedor
Campanha planejada: 30% de desconto em tudo · Equipe: 4 pessoas · Verba de mídia: R$ 30.000
```
Saída:
```
Antes do plano, três alertas:
1. Fontes divergentes: 780 pedidos (plataforma) × 640 compras (GA4). Não escolho um número: o mais
   provável é o GA4 perdendo compras (Pix pago fora do site, bloqueador, consentimento). Para a
   conta, uso a plataforma (fonte da venda) e registro a diferença.
2. Erro ao gerar o Pix = falha crítica. Vem ANTES de qualquer investimento em mídia
   (→ otimizacao-de-checkout).
3. 30% em tudo: sem a margem de contribuição por produto, não sei se a campanha dá lucro ou
   prejuízo. Conferir antes (→ precificacao).

Conta da meta (plataforma; ticket de outubro):
- R$ 260.000 ÷ R$ 240 ≈ 1.083 pedidos — 38,9% a mais que outubro.
- Com a conversão de outubro (780 ÷ 52.000 = 1,5%): seriam ~72.200 sessões; ou, com as mesmas
  52.000 sessões, conversão de ~2,08%.
- Comparar com outubro engana: o comparável é novembro do ano passado (Black Friday). Pedir esse dado.
São contas para ver o tamanho da meta, não previsão.

Caminho crítico
Semana 1: corrigir o Pix (dev + gateway) e conferir a medição → conferir a margem de cada produto
  com 30% e definir o desconto por produto (precificacao) → campanha só depois.
Semana 2: catálogo e feed atualizados (anuncio-shopping); criativos sem o produto âncora
  (prompt-banner-campanha, angulos-de-anuncio).
Semana 3: o âncora entra na campanha só a partir do dia 20, com o estoque confirmado no sistema
  (urgencia-honesta: nada de "últimas unidades" sem dado).
Semana 4 (Black Friday): monitoramento diário.

Critérios de parada (combinados antes): taxa de erro no checkout acima do normal → pausar a mídia;
contribuição negativa num produto → tirar o produto da campanha; reclamações de entrega acima do
normal → rever o prazo anunciado.
Proteção: aprovação de pagamento, margem, devoluções, reclamações.
```

> Referência: cada número tem estado e fonte; as contas da árvore de receita estão certas e não
> viram promessa; hipóteses vêm com o dado que as separa; a medição e a falha crítica vêm primeiro;
> nada de anunciar produto sem estoque nem de desconto sem margem; o plano cabe na equipe, tem dono,
> entrega e medida em cada ação, diz o que ficou de fora e encaminha só para skills que existem.
