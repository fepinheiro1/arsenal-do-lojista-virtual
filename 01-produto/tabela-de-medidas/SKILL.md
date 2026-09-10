---
name: tabela-de-medidas
description: Organiza, valida e explica tabelas de medidas e guias de tamanho para e-commerce, distinguindo medidas do corpo, da peça e do produto, sistemas de tamanho, variantes e caimento — sem inventar equivalências internacionais ou recomendações de tamanho. Aceita dados soltos, uma tabela atual, uma URL ou um catálogo. Use em moda, calçados, anéis, cama e qualquer item com tamanho.
---

# Tabela de Medidas

## O que faz
Monta um guia de tamanhos que ajuda a pessoa a acertar — e impede que uma tabela bonita transmita informação errada. Organiza e converte dados físicos (cm ↔ polegada), explica como medir, e trata sistemas, variantes e caimento. O que ela **não** faz: inventar equivalência de tamanho comercial (BR↔US↔EU), recomendar "suba um tamanho" sem regra, ou transformar largura de peça em medida de corpo. Guia certo reduz devolução por numeração; guia errado aumenta.

Regra de ouro: **organizar e converter dado físico, sim; inventar equivalência comercial ou fit sem base, não.** Simples na superfície, especialista por baixo.

## Quando usar
- Montar o guia de tamanhos de um produto (moda, calçado, anel, cama, qualquer item com tamanho).
- Arrumar uma tabela bagunçada (unidades misturadas, colunas sem rótulo).
- Validar se uma tabela está pronta para publicar ou tem pendências.
- Padronizar os guias de um catálogo inteiro (modo em lote).

## O que a IA precisa de você
No mínimo, as **medidas** que você tem (por tamanho), ou uma **tabela atual**, ou uma **URL** (com web; se não, cole os dados), ou um **catálogo**.

Uma coisa é decisiva e a skill vai querer saber: **as medidas são do corpo, da peça ou do produto?** Se não der para deduzir com segurança, ela pergunta — porque isso muda tudo. Opcional e valioso: sistema de tamanho (BR/US/EU), modelagem (slim/regular/oversized) e a tabela oficial da marca para conversões internacionais.

## Como funciona (por baixo)

**1. Separa cinco coisas que não se misturam.** Medida do **corpo** (busto, cintura, pé) · medida da **peça** (largura plana, comprimento, manga) · **dimensão do produto** (anel, colchão) · **tamanho comercial** (P/M/G, 38, US 8, Queen) · **recomendação de fit** (veste justo, suba um tamanho). Tratar uma como a outra é o erro que gera devolução.

**2. Rotula sempre a tabela.** Toda saída diz, no topo: *"As medidas abaixo são do corpo / da peça / do produto."* Se não dá para identificar pelo que você mandou, pergunta antes de montar.

**3. Largura de peça não é circunferência de corpo.** Uma camiseta com 52 cm de largura plana não vira "busto recomendado 104 cm" — no máximo isso é a circunferência aproximada *da peça*, e o caimento ainda depende de folga, corte e elasticidade. Se suspeita que P=48/M=51/G=54 são larguras planas, confirma: *"Esses números são a largura da peça (axila a axila) ou a circunferência do corpo?"*.

**4. Conversão física sim, comercial não.** cm ↔ polegada, mm ↔ cm, m ↔ cm são matemática segura (1 in = 2,54 cm). BR↔US↔EU, UK↔EU **não são** — variam por marca e por sistema. Só adiciona um sistema internacional com a tabela oficial da marca ou fonte que você fornecer; sem isso, explica que a equivalência varia e pede a fonte.

**5. Mede a confiança do fit — e não força maior/menor.** Só recomenda um tamanho específico quando a regra de modelagem foi informada (confirmada) ou os dados a sustentam (apoiada). Sem isso, a orientação honesta é: *"Se ficar entre dois tamanhos, compare suas medidas com a tabela e considere o caimento que você prefere."* Modelagem tem peso: `M Tall`, `M Plus`, `M Oversized` não são o `M` normal.

**6. Valida a consistência e marca o estranho (não conserta sozinha).** Detecta sequência fora de ordem (P 70 / M 68 / G 80), tamanho duplicado, unidade ausente ou misturada, coluna faltante, salto improvável, range com mínimo > máximo, zero/negativo, sistemas misturados. Um outlier não é erro automático — marca para você confirmar.

**7. Trata cada categoria com seu preset.** Tops (busto/ombro/manga/comprimento) · bottoms (cintura/quadril/entrepernas, com `32×34` preservando cintura×entrepernas) · calçados (comprimento do pé → número **só com tabela oficial**; "meça os dois pés e use o maior") · largura de calçado (só quando existe) · anéis (diâmetro/circunferência; número só com tabela oficial) · cama (a dimensão física é mais confiável que "Queen/King", que muda por país). Ranges (`M: busto 96–104 cm`) são nativos.

**8. Nunca calcula o que o material não permite.** Elastano não diz quanto estica; algodão não diz quanto encolhe; tolerância (±) só aparece se informada. Reviews podem revelar "veste pequeno", mas percepção de poucos compradores não vira regra oficial de modelagem.

## Instruções (o cérebro da skill)
1. Identifique o **modo** (criar / otimizar / normalizar / validar / lote) e a **categoria**.
2. Determine o **tipo de medida** (corpo/peça/produto) — se ambíguo, **pergunte** antes de montar.
3. Normalize unidades (converta cm↔in quando útil), registre o **sistema** de tamanho e **valide** a consistência.
4. Monte a tabela pelo preset da categoria, com rótulo no topo e unidade em toda coluna.
5. Escreva o **"Como medir"** certo para o tipo: corpo (medir a pessoa) ou peça (peça semelhante que veste bem, esticada numa superfície plana, medindo os mesmos pontos) — **nunca misture** as instruções.
6. Adicione **notas de caimento só quando suportadas**; conversões internacionais só com fonte oficial.
7. Rode o **Quality Gate**; falha crítica não vai para publicação em silêncio — vira pendência.
8. Entregue o guia pronto + (se houver) a lista curta de pendências a confirmar.

## Regras de qualidade
- **Nunca invente** medida, sistema de tamanho, equivalência internacional, recomendação de fit, tolerância, elasticidade, encolhimento, largura, dimensão, prioridade de medida ou compatibilidade dimensional.
- **Tamanho comercial não é conta**: não gere BR↔US↔EU por cálculo. Se a fonte só dá aproximação, rotule "conversão aproximada".
- **"40" isolado não tem sistema**: não assuma BR nem EU — pergunte ou registre como veio.
- **Não recomende maior/menor sem evidência** de modelagem. (Corrige a dica automática da V1.)
- **Cama**: nunca assuma Queen/King globalmente — a dimensão física manda; sem dimensão/sistema/mercado, peça o dado.
- **Variantes**: se o tamanho identifica o SKU, preserve o valor por SKU; não consolide tamanhos distintos.
- **Contexto regional**: sistema e equivalência dependem do país — não importe a tabela de outro mercado.
- **Mobile-first**: tabela curta, só as colunas que importam; muitas dimensões → separe em blocos em vez de uma tabela horizontal gigante.

### Quality Gate (silencioso, antes de entregar)
O tipo (corpo/peça/produto) está claro? · Unidade em tudo? · Sistema conhecido quando necessário? · Sequência e ranges plausíveis? · Falta dimensão importante? · A conversão foi só física (não comercial inventada)? · A recomendação de fit tem base? · O tamanho bate com o SKU? · As medidas combinam com a categoria? · O comprador sabe como medir? · A tabela é legível no celular? · Equivalências e fit têm fonte? — falha crítica vira pendência, não publicação.

## Formato da saída
Por padrão, o **guia pronto para a página**:
```
## Guia de tamanhos
As medidas abaixo são [do corpo / da peça / do produto].

| Tamanho | Busto | Cintura | Quadril |
|---|---:|---:|---:|
| P | ... | ... | ... |

### Como medir
- Busto: ...
- Cintura: ...

### Sobre o caimento
[Somente o que os dados sustentam.]
```
Se houver ambiguidade ou buraco, uma lista curta no fim:
```
Antes de publicar, confirme:
- o sistema do tamanho "40" (BR? EU?);
- se o busto é medida do corpo ou da peça;
- o valor do tamanho M.
```
Sob pedido: tabela com cm + polegada, conversão internacional (com fonte oficial), dados de Google Merchant (`size`, `size_system`, `size_type`, `gender` — preservando o tamanho por SKU), validação "aprovada / pendências", um Size Advisor (só com tabela estruturada, mapeando a medida no range oficial e dizendo qual critério usou), ou a tabela normalizada em lote.

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
