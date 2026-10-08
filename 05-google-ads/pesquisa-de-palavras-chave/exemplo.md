# Pesquisa de Palavras-chave — exemplos reais

## Exemplo A — Sem dados (tudo é hipótese, e está rotulado)
Entrada:
```
Loja: PisoLeve — tênis de corrida masculino e feminino, numeração 37 a 44,
  modelo principal NimbusFlow X1. Só produto novo, só varejo.
Mercado: Brasil, português, entrega nacional
Páginas: /tenis-corrida-masculino, /tenis-corrida-feminino
Não atende: usado, aluguel, atacado, conserto
Planejador / relatório de termos: não tenho · Compra medida com valor: não sei
```
Saída:
```
Fonte de tudo abaixo: IDEIA (hipótese) — nenhum volume ou CPC porque não houve exportação
do Planejador. Confira lá antes de definir lance.

Palavra-chave                       | Intenção          | Grupo        | Corresp. | Prioridade | Confiança | Motivo
tênis de corrida masculino          | compra/comparação | Corrida masc | frase    | alta       | média     | termo central; a página atende
comprar tênis de corrida masculino  | compra            | Corrida masc | frase    | alta       | alta      | intenção clara; frase já cobre variações de sentido
tênis de corrida masculino 42       | compra            | Corrida masc | frase    | média      | alta      | numeração existe no catálogo (37–44)
tênis de corrida feminino           | compra/comparação | Corrida fem  | frase    | alta       | média     | grupo próprio porque a página é outra
nimbusflow x1                       | compra (modelo)   | Corrida masc | exata    | média      | alta      | nome do modelo vendido; vale se houver busca por ele
melhor tênis de corrida masculino   | comparação        | Corrida masc | frase    | baixa      | média     | a página é de catálogo, não comparativa — testar depois

Por que "frase" e não ampla: a medição da compra não está confirmada. Ampla funciona bem com
conversões medidas e lances inteligentes; sem isso, fica como teste para depois.
Por que não repeti a lista em exata, frase e ampla: duplicar não traz controle, só divide dado.

Ficaram de fora (e por quê)
- "tênis de corrida com amortecimento", "para pisada pronada": atributo não confirmado. Entram
  se a ficha técnica e a página disserem isso.
- "como escolher tênis de corrida": busca de pesquisa; a página de catálogo não responde.
  É assunto para conteúdo, não para esta campanha.
- "pisoleve" (marca): loja nova — só vale se houver busca pelo nome. Não é "clique barato" por regra.

Negativas
Termo            | Corresp. neg. | Escopo           | Buscas boas que poderia bloquear       | Status
usado            | ampla         | campanha         | nenhuma (a loja só vende novo)         | SEGURA
aluguel, alugar  | ampla         | campanha         | nenhuma — cada forma entra separada    | SEGURA
atacado          | ampla         | campanha         | nenhuma (só varejo)                    | SEGURA
conserto, consertar | ampla      | campanha         | nenhuma — negativa não pega variação   | SEGURA
grátis           | —             | —                | "tênis de corrida frete grátis"        | NÃO APLICAR
tênis grátis     | frase         | campanha         | nenhuma aparente                       | REVISAR
feminino         | ampla         | SÓ grupo masc.   | na campanha, mataria o grupo feminino  | REVISAR

Nada foi aplicado — é uma lista para você revisar.
Lacuna: buscas por atributo técnico pedem página que comprove o atributo.
```

## Exemplo B — Auditar o relatório de termos de pesquisa
Entrada:
```
Campanha de Pesquisa "corrida", últimos 30 dias, compra medida com valor.
Relatório de termos (dados do lojista):
  tênis de corrida masculino 42        | 120 cliques | R$ 180 | 6 compras
  tênis de corrida frete grátis        |  40 cliques | R$ 70  | 3 compras
  conserto de tênis de corrida         |  15 cliques | R$ 22  | 0 compras
  tênis de corrida nike                |  60 cliques | R$ 110 | 0 compras  (a loja não vende Nike)
  tênis de corrida para corrida de rua |   9 cliques | R$ 14  | 0 compras
  tênis feminino de corrida            |  18 cliques | R$ 27  | 1 compra   (caiu no grupo masculino)
Alguém sugeriu negativar "grátis" em toda a conta.
```
Saída:
```
Fonte: TERMOS DE PESQUISA (30 dias, dado do lojista). O relatório não mostra todas as
buscas (privacidade) — ele refina, não é o retrato completo.

1. "tênis de corrida masculino 42" — melhor termo do período. Manter; pode virar palavra-chave
   própria (frase) para acompanhar de perto.
2. "tênis de corrida frete grátis" — 3 compras. É a prova: negativar "grátis" derrubaria um
   termo que vende. Status de "grátis": NÃO APLICAR.
3. "conserto de tênis de corrida" — a loja não faz conserto. Negativa "conserto" + "consertar"
   na campanha: SEGURA. O motivo é a oferta, não os 0 cliques que viraram compra.
4. "tênis de corrida nike" — a loja não vende Nike. Negativa "nike" na campanha: SEGURA, pelo
   mesmo motivo. E a marca alheia nunca entra no anúncio.
5. "tênis de corrida para corrida de rua" — 9 cliques é amostra pequena e o termo é relevante.
   NÃO negativar; olhar de novo depois da janela de conversão.
6. "tênis feminino de corrida" — vende, mas caiu no grupo errado. Negativa "feminino" SÓ no
   grupo masculino, para essa busca ir ao grupo feminino (que tem a página certa). Na campanha
   inteira, mataria o próprio grupo feminino. Status: REVISAR e aplicar no escopo do grupo.

Nada foi aplicado: as 3 negativas seguras e a de grupo ficam para a sua aprovação.
```

> Referência: tudo que veio da IA está rotulado como hipótese e sem número; atributo não
> confirmado ficou de fora; a correspondência é explicada como funciona hoje (frase por
> significado, ampla condicionada à medição); cada negativa passou pelo teste de bloqueio e
> recebeu o menor escopo; e no relatório o corte foi por incompatibilidade com a oferta — a
> amostra pequena e o termo que vende foram protegidos.
