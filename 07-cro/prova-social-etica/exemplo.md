# Prova Social Ética — exemplos reais

## Exemplo A — Pouca prova no site: inventário, apresentação e coleta sem filtro
Entrada:
```
Produto: mochila antifurto para notebook (cor preta) · Página: produto
Avaliações no site: 9, média 4,9 (8 de 5 estrelas, 1 de 4) — todas da mochila preta
Marketplace: 130 avaliações, média 4,7 — anúncio da mesma mochila, cores preta e cinza juntas
Depoimento: "Uso todo dia no metrô e me sinto tranquila. O compartimento esconde bem o zíper."
  — Renata (autorizou só o primeiro nome; sem foto)
Garantia: 6 meses do fabricante · Pagamento: processado pelo gateway da loja
Vendas: não sei · Canais: e-mail de pós-compra e WhatsApp
Plano que o lojista pensou: "no WhatsApp, quem responder bem eu convido para avaliar"
```
Saída:
```
INVENTÁRIO
Prova                       | Estado                 | O que pode ser mostrado
Avaliações do site (9)      | verificada (plataforma)| 4,9 em 9 avaliações, com a distribuição
Avaliações do marketplace   | informada, não verif.  | só por link, e dizendo que somam preta e
  (130)                     |                        | cinza; conferir os termos do marketplace
                            |                        | antes de importar texto
Depoimento da Renata        | informado, autorizado  | citação literal, assinada "Renata" — sem
                            |                        | cidade (não foi autorizada)
Garantia de 6 meses         | informada              | é política de confiança, não prova social
Número de vendas            | pendente               | não exibir

APRESENTAÇÃO (pela dúvida de quem compra)
- Perto do preço (decisão): "4,9 de 5 · 9 avaliações", com a distribuição ao abrir.
- Bloco de avaliações (consideração), rótulo "Quem usa no dia a dia":
  "Uso todo dia no metrô e me sinto tranquila. O compartimento esconde bem o zíper." — Renata
  Logo abaixo: "Também avaliada no [marketplace]: 4,7 em 130 avaliações (cores preta e cinza) →
  ver lá". É link e não soma com as notas do site.
- Bloco de confiança (separado, sem chamar de prova social): garantia de 6 meses do fabricante;
  pagamento processado pelo gateway [nome]. Sem "100% seguro".

CORREÇÃO NO PLANO DE COLETA
"Quem responder bem, convide a avaliar" é review gating: só quem está satisfeito chegaria à
avaliação pública. No lugar:
1. Pedido de avaliação para TODO comprador, depois de um tempo de uso (o tempo exato fica com a
   pos-compra-avaliacao), com link direto e pergunta neutra ("Como está sendo usar a mochila?").
2. Quem tiver um problema recebe ajuda, e continua podendo avaliar.
3. Foto de cliente: pedir com autorização para o site. Para usar em anúncio, autorização separada.
4. Acompanhar convites enviados, avaliações recebidas e fotos — não só a média.
```

## Exemplo B — Auditoria do que já está no ar
Entrada:
```
Na página do tênis VERMELHO:
- "Mais de 10.000 clientes satisfeitos" (o sistema registra 10.000 PEDIDOS)
- "Média 4,8" = média simples entre o site (4,9, com 9 avaliações) e o marketplace (4,7, com 130)
- Widget "23 pessoas vendo agora": número aleatório gerado no navegador
- As avaliações exibidas são do tênis PRETO
- Ordenação "mais relevantes" deixa as 2 avaliações de 1 estrela no fim da 5ª página
- Uma "foto de cliente" foi gerada por IA
- Dados estruturados com AggregateRating num produto sem nenhuma avaliação própria
```
Saída:
```
Evidência                 | Risco                                   | Correção                      | Prior.
"10.000 clientes          | pedidos ≠ clientes únicos; "satisfeitos"| "Mais de 10.000 pedidos       | alta
 satisfeitos"             | não tem fonte                           | enviados desde [ano]", com data|
Média 4,8                 | média de médias com bases diferentes    | ponderada: (9×4,9 + 130×4,7) ÷| alta
                          |                                         | 139 ≈ 4,7 — e só se puder     |
                          |                                         | somar os canais; se não, separar|
"23 pessoas vendo agora"  | contador falso                          | remover                       | bloqueio
Avaliações do tênis preto | vínculo errado de variante              | mostrar as do vermelho; se    | bloqueio
 na página do vermelho    |                                         | mostrar as do preto, avisar   |
Críticas escondidas na    | impressão enganosa                      | ordenação transparente; filtro| alta
 5ª página                |                                         | por nota                      |
Foto gerada por IA como   | prova falsa                             | remover ou identificar como   | bloqueio
 "de cliente"             |                                         | ilustração (fora do bloco de  |
                          |                                         | avaliações)                   |
AggregateRating sem       | marcação sem conteúdo real              | remover até haver avaliações  | alta
 avaliações próprias      |                                         | visíveis deste produto        |

Ordem: os 3 bloqueios saem hoje. Depois, recalcular a média, corrigir o número e abrir as
críticas. Nenhuma correção depende de "testar" — é integridade, não otimização.
```

> Referência: cada prova tem estado, fonte e autorização; a citação é literal e mostra só o que foi
> autorizado; a avaliação fica no produto e na variante certos; a média é ponderada e a distribuição
> aparece com as críticas; a coleta não filtra por satisfação; confiança operacional não é chamada
> de prova social; e contador, foto de IA e estrela sem avaliação são bloqueados.
