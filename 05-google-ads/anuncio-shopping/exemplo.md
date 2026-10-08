# Anúncio de Shopping (feed do Merchant Center) — exemplos reais

## Exemplo A — Otimizar um item (com a marca em dúvida)
Entrada:
```
ID: PL-NFX1-PRT-42 · item_group_id: PL-NFX1
Produto: Tênis de corrida NimbusFlow X1
Atributos: marca "PisoLeve" (atenção: é o nome da loja), tipo tênis de corrida, gênero masculino,
  cor preto, numeração 42 (BR), cabedal em malha respirável, 268 g, condição novo
Garantia: 3 meses contra defeito · GTIN: não informado
País/idioma/moeda: Brasil, português, BRL · Relatório do Merchant Center: não tenho
```
Saída:
```
Alerta (atenção) — MARCA: "PisoLeve" é o nome da loja. Se a PisoLeve fabrica a linha NimbusFlow
(marca própria), está certo. Se é revenda, a marca do feed é a do fabricante, e o título muda.
Os títulos abaixo valem para o caso "marca própria".

Título recomendado (61)
Tênis de Corrida Masculino PisoLeve NimbusFlow X1 Preto Nº 42
Por quê: marca própria ainda pouco buscada → o tipo de produto identifica melhor e vem primeiro;
gênero, cor e numeração da variante logo depois.

Alternativas (cada uma é uma hipótese a testar)
A) PisoLeve NimbusFlow X1 Tênis de Corrida Masculino Preto Nº 42 (61)
   Hipótese: vale se já houver gente buscando pelo nome do modelo.
B) Tênis de Corrida Masculino Malha Respirável PisoLeve NimbusFlow X1 Preto Nº 42 (78)
   Hipótese: o material (confirmado) ajuda quem busca por malha respirável.

Descrição recomendada (208)
Tênis de corrida masculino NimbusFlow X1, da PisoLeve, na cor preto e numeração 42. O cabedal
é em malha respirável e o peso é de 268 g, conforme a ficha técnica do modelo. Garantia de 3
meses contra defeito.

Atributos usados (confirmados): tipo, gênero, cor, numeração (BR), material do cabedal, peso,
condição, garantia.

O que saiu da descrição antiga, e por quê: "leve e estável do primeiro ao último quilômetro",
"solta o calor e mantém o pé seco", "para asfalto e esteira", "para quem treina de verdade" —
nada disso foi informado. A descrição ficou mais curta, mas tudo nela pode ser provado.

Pendências (fora do texto publicável)
- Confirmar a marca (marca própria ou fabricante).
- GTIN: se o tênis tem código de barras do fabricante, informar. Se é marca própria sem código,
  seguir a regra vigente do Merchant Center para item sem identificador — nunca gerar um EAN.
- 268 g é o peso de qual numeração? O peso muda com o tamanho; confirmar na ficha.
- Cada numeração e cor é um item próprio (mesmo item_group_id, ID, imagem e link próprios).

Alertas: bloqueio — nenhum · atenção — marca, GTIN · oportunidade — avaliações reais, se houver.
```

## Exemplo B — Diagnóstico de um lote de 3 itens
Entrada:
```
PL-NFX1-VRM-41 | "Tênis de Corrida NimbusFlow X1 Vermelho Nº 41" | imagem mostra o tênis AZUL
PL-TRK-PRT-40  | "PROMOÇÃO Tênis Trilha TrailRock Preto 40 FRETE GRÁTIS"
               | preço no feed R$ 399 · preço na página R$ 349 (informado pelo lojista)
PL-URB-AZL-39  | sem GTIN; o lojista pergunta se pode "gerar um EAN só para aprovar"
               | descrição diz "o tênis mais vendido do Brasil"
Relatório do Merchant Center: não tenho
```
Saída:
```
Evidência: nenhum item foi checado no Merchant Center (não recebi o relatório). Os problemas
abaixo são suspeitos (pelo catálogo) ou informados pelo lojista.

id             | problema                        | severidade | ação
PL-NFX1-VRM-41 | imagem ≠ variante (azul × verm.)| bloqueio   | trocar a imagem pela foto do vermelho
               |                                 |            | (frente 02). O texto está certo; não mexer.
PL-TRK-PRT-40  | preço do feed ≠ preço da página | bloqueio   | corrigir na origem/integração para o
               |                                 |            | preço vigente. NÃO resolver no título.
PL-TRK-PRT-40  | título promocional              | atenção    | "PROMOÇÃO" e "FRETE GRÁTIS" saem:
               |                                 |            | Tênis de Trilha TrailRock Preto Nº 40 (37)
PL-URB-AZL-39  | sem identificador               | atenção    | NÃO gerar EAN. Se o fabricante tem código,
               |                                 |            | buscar na embalagem/fornecedor; se não tem,
               |                                 |            | seguir a regra vigente para item sem GTIN.
PL-URB-AZL-39  | claim não verificado            | atenção    | remover "o mais vendido do Brasil" (sem prova)

Exportação: PL-NFX1-VRM-41 e PL-TRK-PRT-40 ficam FORA da publicação até resolver o bloqueio.
PL-URB-AZL-39 pode seguir com a descrição corrigida, mas o GTIN continua pendente.
Prioridade: os dois bloqueios primeiro — produto inelegível não vende, por melhor que seja o título.
```

> Referência: o diagnóstico vem antes da reescrita; cada problema vai para a solução certa
> (imagem, origem do preço, identificador, política) em vez de virar "título melhor"; nada é
> inventado (marca, GTIN, peso, claim); as alternativas de título têm hipótese; a contagem é
> exata; e as pendências ficam fora do texto que vai para o feed.
