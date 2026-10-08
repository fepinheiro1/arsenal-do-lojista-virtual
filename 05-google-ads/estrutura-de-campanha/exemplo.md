# Estrutura de Campanha — exemplos reais

## Exemplo A — Conta nova, verba curta, dados faltando
Entrada:
```
Loja: PisoLeve — calçados esportivos (tênis de corrida, tênis casual, chuteiras)
Objetivo: vender tênis de corrida (o lojista diz que é a categoria de maior margem)
Orçamento: R$ 60/dia · Brasil, português, entrega nacional
Margem: não sei · Medição: não sei se a compra está configurada · Feed: não sei
Termos que trazem prejuízo: "grátis", "usado", "conserto de tênis"
Páginas: /tenis-corrida-masculino, /tenis-corrida-feminino
```
Saída:
```
ANTES DE LIGAR QUALQUER CAMPANHA (bloqueante)
- Medição: configurar a COMPRA como conversão principal, com valor. Sem isso, o Google
  otimiza no escuro e nenhuma meta faz sentido. Carrinho e checkout: só para diagnóstico.
- Margem: com ela, o ROAS de equilíbrio sai como hipótese: 1 ÷ margem. Hoje: [preencher].

ÁRVORE (cenário provisório)
Campanha: BR | PESQUISA | VENDA | CORRIDA
  Motivo: é o objetivo declarado; com R$ 60/dia, uma campanha concentra o aprendizado.
  Grupo: Corrida masculino → intenção comercial (categoria) → /tenis-corrida-masculino
  Grupo: Corrida feminino  → intenção comercial (categoria) → /tenis-corrida-feminino
  (Dois grupos porque são duas páginas. Mesma página = um grupo só.)
  Anúncios: a partir dos fatos reais do produto (ver `titulos-e-descricoes`) — nada de
  "amortecimento" ou "estabilidade" sem ficha técnica.
  Lance (hipótese): Maximizar conversões, sem meta, até haver compras medidas com valor.
  Orçamento (hipótese): os R$ 60 inteiros aqui. É média diária: um dia pode gastar mais,
  outro menos; o controle é no mês.

O que NÃO abrir agora, e por quê
- Campanha de marca: loja nova tem pouca busca pelo nome; abrir só se houver volume e
  concorrente anunciando na sua marca. Não é "barata e obrigatória" por regra.
- Campanha só do NimbusFlow X1: só se houver busca pelo nome do modelo e margem que justifique.
- Shopping: tênis é forte candidato a Shopping — mas o feed não foi confirmado. Se estiver
  ok no Merchant Center, veja o Exemplo B antes de dividir R$ 60 em duas campanhas.

Negativas a revisar
- "usado", "conserto de tênis": ok.
- "grátis" sozinho: NÃO. Bloqueia "tênis de corrida frete grátis", uma busca de compra.
  Troque por negativas de frase específicas: "tênis grátis", "amostra grátis".
- "casual", "chuteira" nesta campanha: ok (outra categoria).

3 próximos passos
1. Configurar a compra como conversão com valor (e conferir se não conta em dobro).
2. Informar a margem e o status do feed.
3. Lançar a campanha de corrida e olhar os termos de pesquisa na primeira semana.
```

## Exemplo B — Loja com feed: Shopping, inventário e meta como hipótese
Entrada:
```
PisoLeve, alguns meses depois. Feed ok no Merchant Center: 180 produtos.
Margem de contribuição: 30% · Compra com valor configurada · ~40 compras/mês
Orçamento: R$ 150/dia · A campanha de Pesquisa de corrida está convertendo
Planilha de custos por produto disponível; 22 itens sem estoque
```
Saída:
```
Conta de referência (hipótese): ROAS de equilíbrio = 1 ÷ 0,30 ≈ 3,3 — só paga a mídia,
antes de lucro. É régua para avaliar, não promessa de resultado.

ÁRVORE
Campanha: BR | PESQUISA | VENDA | CORRIDA  (mantém — está convertendo; não mexer junto)
Campanha: BR | SHOPPING | VENDA | CATALOGO
  Motivo: inventário com feed ok; o anúncio de produto mostra foto e preço.
  Shopping padrão primeiro, pelo controle de inventário com 180 produtos e 40 compras/mês.
  Performance Max fica como teste depois, com hipótese e métrica definidas antes.
  Inventário:
    - 22 itens sem estoque: fora.
    - Rótulo personalizado "faixa de margem" (alta / média / baixa), vindo da planilha de
      custos — a origem do dado fica documentada. Margem baixa: fora ou com verba menor.
    - "Mais vendido" só se vier dos dados de venda, nunca no achismo.
  Grupos de produtos: por categoria × faixa de margem — sem separar grupo sem volume.
Lance (hipótese): Maximizar valor da conversão (o valor está medido). Meta de ROAS só
  depois de volume estável, usando 3,3 como piso de referência.
Orçamento (hipótese): R$ 90 Shopping / R$ 60 Pesquisa. Revisar pelo resultado, não por regra.

Sobreposição: Pesquisa e Shopping podem aparecer na mesma busca — isso não é "canibalização"
automática. Se testar Performance Max depois, confira na conta que controles de marca e de
exclusão ela oferece hoje: são diferentes das negativas da Pesquisa e vêm mudando.
```

## Exemplo C — Auditoria e migração de uma conta bagunçada
Entrada:
```
Conta ativa: 18 campanhas de Pesquisa, uma por produto, R$ 100/dia no total (~R$ 5,50 cada)
Conversões: "compra" E "adicionar ao carrinho" marcadas como principais
Queixa do lojista: "o custo por conversão parece ótimo, mas não sobra dinheiro"
```
Saída:
```
Diagnóstico por etapa (não é tudo culpa da estrutura)
1. Medição — o problema principal. "Adicionar ao carrinho" como conversão principal infla o
   número de conversões: o lance otimiza para carrinho, não para venda. Por isso o custo por
   conversão "parece ótimo" e o caixa não fecha.
2. Estrutura — 18 campanhas de ~R$ 5,50: nenhuma junta dados para aprender.

Plano de migração (por etapas, nunca tudo de uma vez)
Etapa 1: carrinho vira conversão secundária; só a compra fica como principal. Não mexer em
  mais nada nas semanas seguintes — o lance vai se reajustar, e é preciso ver o efeito isolado.
Etapa 2: consolidar por categoria, uma de cada vez: as campanhas de produto de corrida viram
  grupos dentro de "BR | PESQUISA | VENDA | CORRIDA". O que já converte com dado comprovado
  é preservado como grupo próprio.
Etapa 3: repetir para as demais categorias.
Critério para voltar atrás (definido ANTES): por exemplo, custo por compra acima da média das
  4 semanas anteriores por 2 semanas seguidas → reverter a última etapa e investigar.
Nomes: PAÍS | CANAL | OBJETIVO | TEMA | VERSÃO — legível, sem código obscuro.
```

> Referência: medição e margem vêm antes da árvore; cada campanha tem motivo de existir;
> orçamento, lance e ROAS de equilíbrio aparecem como hipótese; a negativa que bloquearia
> busca boa é corrigida; o feed entra com inventário filtrado e dado de origem conhecida; e a
> conta existente é auditada e migrada por etapas, com volta atrás — sem prometer resultado.
