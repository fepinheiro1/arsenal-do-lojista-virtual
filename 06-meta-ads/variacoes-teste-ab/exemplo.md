# Variações para Teste A/B — exemplos reais

## Exemplo A — Desenhar o teste (controle com problemas, verba curta)
Entrada:
```
Anúncio atual (no ar há 3 semanas):
  Texto principal: Cansada de secar o cabelo e ele armar de novo em 10 minutos?
    A escova secadora alisa e seca ao mesmo tempo, com cerdas que domam o frizz.
    Salão em casa, todo dia. Toca em Comprar agora.
  Título: Escova secadora que aliza e seca · CTA: Comprar agora · sem oferta
Problema: CTR estável, mas o custo por compra subiu de R$ 32 para R$ 45
Produto: escova secadora 2 em 1 (seca e alisa) · Prova real: 4,7 de 5 em 1.200 avaliações
O atendimento diz: a dúvida mais comum é "funciona em cabelo grosso?"
Orçamento: R$ 40/dia · Objetivo: vendas
```
Saída:
```
CONTROLE (A), como está no ar — e o que precisa de correção documentada antes do teste:
- "aliza" no título: erro de escrita.
- "cerdas que domam o frizz" e "salão em casa": sem base informada. Manter só se o fabricante
  sustentar; se não, sai.
- "Cansada de...": presume gênero e uma situação de quem lê. Mesmo não sendo atributo sensível pela
  política, restringe e presume.
Corrigir isso cria um NOVO controle (A'). As 3 semanas anteriores deixam de ser comparáveis.
A' — Texto principal: O cabelo armou de novo depois de secar? A escova secadora seca e alisa ao
  mesmo tempo. Toca em Comprar agora.
  Título: Escova secadora: seca e alisa · CTA: Comprar agora

Variável em teste: a PROVA no início do texto — não o gancho por hábito.
Por quê: o CTR está estável (o anúncio chama atenção) e o custo por compra subiu. O gargalo parece
estar na decisão, não na atenção. E o atendimento mostra uma dúvida concreta.

B — Texto principal: Nota 4,7 de 5 em 1.200 avaliações. A escova secadora seca e alisa ao mesmo
  tempo. Toca em Comprar agora.
  (Título, CTA, criativo, página e público idênticos a A'.)
O que mudou: a 1ª linha (situação → prova social).
Hipótese: se o anúncio abrir pela nota das avaliações, esperamos custo por compra menor, porque a
  prova reduz a dúvida de quem já se interessou. Origem: a nota é real; o efeito é hipótese.

Não entram: "1.200 avaliações de quem cansou de brigar com o frizz" (ninguém sabe quem avaliou),
"antes do café ficar pronto" (tempo não comprovado), CTA "Ver oferta" (não existe oferta).
Próxima candidata, se esta não resolver: responder "funciona em cabelo grosso?" — só se o
fabricante confirmar.

Métrica principal: custo por compra. Proteção: taxa de conversão da página, reclamações.
Igual entre A' e B: criativo, título, CTA, página, público, posicionamentos, janela de atribuição.
Como rodar: ferramenta de Teste A/B do Meta (A' × B), sem mexer no meio.
Verba: R$ 40/dia rende poucas compras por semana → teste EXPLORATÓRIO. Só dois braços, rodando ao
  menos 2 semanas inteiras e com volume mínimo de compras por versão definido antes.
Regra de parada: decidir só no fim do prazo combinado, nunca porque uma versão liderou no 2º dia.
```

## Exemplo B — Ler um resultado ("B ganhou com 57% mais compras!")
Entrada:
```
7 dias, dois anúncios no MESMO conjunto (não foi usada a ferramenta de Teste A/B)
A: 9.800 impressões · R$ 280 · 7 compras
B: 10.100 impressões · R$ 285 · 11 compras
Na mesma semana houve uma ação de frete grátis no site.
```
Saída:
```
Versão | Impressões | Gasto  | Compras | Custo por compra
A      | 9.800      | R$ 280 | 7       | R$ 40,00
B      | 10.100     | R$ 285 | 11      | R$ 25,90

Leitura: INCONCLUSIVO.
- São 4 compras de diferença. Num teste estatístico simples de proporções (compras por impressão),
  uma diferença desse tamanho tem cerca de 38% de chance de aparecer só por acaso (p ≈ 0,38). Isso
  está longe de uma evidência confiável.
- Dois anúncios no mesmo conjunto não dividem o público de forma aleatória: a entrega pode ter
  favorecido um deles.
- A ação de frete grátis no meio do teste pode ter mudado o comportamento de todo mundo.

O que fazer: tratar B como um SINAL, não como vencedor. Repetir com a ferramenta de Teste A/B do
Meta, fora de promoção, com prazo e regra de parada definidos antes. E não generalizar o resultado
para os outros produtos da loja.
```

> Referência: o teste parte do problema (custo por compra), escolhe a variável pelo gargalo e não
> por hábito, mantém o controle como estava e documenta a correção, cria variantes diferentes de
> verdade com os mesmos fatos, cabe na verba (A × B, exploratório), define regra de parada antes e,
> na leitura, mostra a incerteza e aceita o inconclusivo — sem inventar significância.
