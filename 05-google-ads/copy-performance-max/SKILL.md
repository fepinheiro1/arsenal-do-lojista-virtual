---
name: copy-performance-max
description: Escreve os textos de um grupo de recursos do Performance Max (títulos, títulos longos, descrições, nome da empresa) começando pela estratégia — quais produtos o grupo cobre, que oferta e que página — e garantindo que cada texto funcione sozinho, valha para todos os produtos do grupo e bata com o feed e a página. Conta os caracteres de forma exata, não infla atributo além do que ele prova e trata como dependência o que o Google faz sozinho (textos gerados a partir da página, expansão de URL, vídeo automático). Aceita produto/coleção, objetivo, marca, página, benefícios confirmados, oferta e o feed. Use para criar, otimizar, auditar, variar, adaptar ou gerar em lote assets de texto do PMax.
---

# Copy para Performance Max

## O que faz
Escreve os textos que o Performance Max combina sozinho em vários canais do Google — mas começa pela pergunta que o preenchimento de campos ignora: **o que este grupo de recursos promove, e o que é verdade para todos os produtos dele?** Define o escopo do grupo, a oferta e a página; depois escreve textos modulares (cada um funciona sozinho e combinado), confere que nenhum promete o que o feed ou a página não sustentam, e avisa o que o Google pode gerar ou mudar por conta própria.

Regra de ouro: **verdade comercial acima do preenchimento de campos.** Menos textos verdadeiros e distintos valem mais que todos os campos cheios com sinônimos ou com atributo esticado além do que prova. A voz é da marca do lojista.

## Quando usar
- Criar o grupo de recursos de uma campanha Performance Max (com feed de produtos ou sem).
- Revisar ou auditar textos que já rodam (repetição, claims, coerência com o feed e a página).
- Propor variações de teste, adaptar para outra coleção/mercado ou gerar vários grupos de uma vez.

## O que a IA precisa de você
- `[produto ou coleção]` — os produtos que o grupo cobre (e, com feed, quais itens estão no grupo de listagem).
- `[objetivo]` — vender, gerar contato, girar estoque.
- `[marca]` — o nome comercial exato (e uma forma curta aprovada, se passar de 25 caracteres) e o tom.
- `[página de destino]` — a URL. Sem ela, a skill marca pendência — nunca inventa domínio.
- `[benefícios e características confirmados]` — o que a ficha técnica e a página sustentam.
- `[oferta]` (opcional) — frete, preço, parcelamento, cupom, validade — só o que é real e vale para os produtos do grupo.
- (opcional) feed/Merchant Center, temas de pesquisa e sinais de público, configurações de automação (expansão de URL, textos gerados), assets e métricas atuais.

## Como funciona (por baixo)

**1. Estratégia antes da redação.** Primeiro objetivo, produtos, oferta e página — depois os textos. Campanha de varejo **com feed** e campanha **sem feed** funcionam diferente: com feed, o catálogo pesa muito no que aparece. Título genérico que serviria para qualquer loja não entra.

**2. Grupo de recursos não é grupo de anúncios.** Ele reúne textos, imagens e o contexto de um tema — **não controla as buscas** como um grupo de Pesquisa. Por isso o grupo precisa cobrir produtos **coerentes o bastante para dividir os mesmos textos e a mesma página**. Todo claim tem que valer para **todos** os produtos cobertos: se só um modelo tem frete para todo o Brasil, "frete para todo o Brasil" não entra no grupo misto. Grupo heterogêneo → textos com o que é comum a todos, ou dividir o grupo (quando houver volume para isso). Com feed, a skill cruza o grupo com os itens realmente incluídos no grupo de listagem.

**3. Verdade de produto, oferta, página, feed e prova.** Nome, marca, categoria, variante, atributo e disponibilidade como são. **Atributo informado não autoriza efeito não provado**: "entressola de alta absorção" não vira "menos impacto no joelho"; "malha respirável" não vira "pé seco do início ao fim". Preço, frete, desconto, parcelamento, cupom e validade só reais e atuais. O anúncio não promete coleção, preço ou condição que a página não mostra. Com feed, título, preço, estoque e destino precisam bater com o Merchant Center (e aprovação dos itens é dependência). Selo, depoimento, nota, "mais vendido", "oficial", escassez: só com prova. O que falta vira pendência — **nunca texto final com `[preencher]` publicado**.

**4. Textos modulares e diversidade real.** O PMax mostra os textos em combinações e espaços diferentes, então **título curto, título longo e descrição precisam se sustentar sozinhos** — nada de "essa oferta" sem antecedente, nem título longo que dependa de um curto que talvez não apareça junto. A skill testa pares plausíveis procurando repetição, contradição e promessa enganosa. Cada texto recebe um **papel** (produto, categoria, benefício, característica, prova, uso, oferta, confiança, marca, ação): trocar a ordem das palavras não cria variedade, e "leve" em cinco títulos é um título só. **Quantidade adaptativa**: quando os fatos sustentam 11 títulos, entrega 11 e diz o que destravaria mais.

**5. Campos e limites vigentes, contados de verdade.** Os campos do PMax **não são cópia dos do anúncio de Pesquisa**. Hoje o Google indica algo como: até 15 títulos de 30 caracteres, até 5 títulos longos de 90, descrições de até 90 com pelo menos uma curta de até 60, e nome da empresa de até 25 — **conferir a especificação vigente** antes de publicar. Contagem **exata, com espaços, pontuação e acentos** (com código, quando possível); o que estoura é **reescrito**, nunca cortado. Nome da empresa é o informado, sem slogan; se passar do limite, pede a forma curta aprovada.

**6. O que o Google faz sozinho é dependência, não detalhe.** O PMax pode **gerar ou adaptar textos** (inclusive a partir do conteúdo da página) — então a skill pergunta se a automação está ligada, separa os textos do anunciante dos gerados e **audita a página**: uma faixa de promoção vencida ou um texto antigo pode virar anúncio. A **expansão de URL final** pode mandar o tráfego para outras páginas do site: com ela ligada, uma página só não controla o destino — a skill propõe uma lista revisável de exclusões (suporte, políticas, itens esgotados, páginas sem oferta), sem bloquear categorias inteiras por conta própria. Sem vídeo enviado, o Google pode **criar um vídeo** em alguns casos — revisar marca, ritmo e claims; a skill não diz que revisou o que não recebeu. PMax ≠ AI Max para Pesquisa: configurações diferentes, nomes que mudam — conferir a documentação vigente.

**7. Cada controle resolve um problema diferente.** **Exclusões de marca**, **palavras-chave negativas** e **exclusões de URL** não têm o mesmo propósito nem o mesmo alcance — a skill diz qual resolve qual problema e marca a disponibilidade na conta como algo a conferir (esses controles mudam). Diretrizes de marca também variam por campanha.

**8. Sinais orientam, não restringem.** **Temas de pesquisa** são sinais de intenção, não palavras-chave com correspondência — não garantem exibição só nesses termos. **Sinais de público** ajudam a automação, mas não limitam a entrega a esse público. Nada de copy baseada em atributo sensível inferido. Sugerir tema só quando o catálogo e a intenção sustentam.

**9. Imagem, vídeo e ação.** Imagem é com as skills da frente `02-imagem`; aqui, o texto não pode contradizer a variante, a cor, a quantidade ou a embalagem que a imagem mostra. Nenhuma regra universal do tipo "todo PMax exige vídeo" ou "texto nunca é necessário" — depende da configuração vigente. A chamada para ação vem **das opções que a interface oferece** (ou automática), coerente com o objetivo — sem inventar rótulo de botão.

**10. Medir sem se enganar.** **Ad Strength mede completude e variedade, não ROAS.** Ad Strength "Excelente" com ROAS ruim pede **diagnóstico econômico** (margem, preço, feed, página, medição) — não mais copy. Relatórios de asset não dão causalidade individual: ninguém prova que um título "fez a venda". Antes de trocar textos com baixo desempenho, considerar período, volume, sazonalidade, mudança de feed, destino e orçamento. Nada de troca diária de tudo; oferta vencida e problema de política vêm antes de teste de estilo. Teste com hipótese, uma variável principal, período e critério de decisão — mexer em feed, orçamento, criativo e URL ao mesmo tempo apaga a leitura.

## Instruções (o cérebro da skill)
1. Identifique o **modo** (criar / otimizar / auditar / variação / adaptar / lote / exportar) e fixe o **PMax Truth Lock**: objetivo (confirmado ou pendente), escopo do grupo (produtos e variantes reais), feed (título, preço, estoque, destino), marca (nome, tom, restrições), produto (atributos confirmados), oferta (condições e validade), página (destino e promessas), configurações (expansão de URL, textos gerados, controles de marca), política (país, categoria), medição (conversões, valor). **Nenhuma informação pendente vira texto final.**
2. Defina o **escopo do grupo**: os produtos são coerentes? Que claims valem para todos? Recomende dividir se não forem.
3. Monte o **mapa de mensagens** por papel e escreva os campos — títulos, títulos longos, descrições (com a curta) e nome da empresa.
4. **Conte com exatidão** e reescreva o que estourar; rode o teste de combinações e o de **feed/página**.
5. Rode o **gate de política e de automação** (textos gerados, expansão de URL, vídeo automático, controles).
6. Rode o **Quality Gate** e entregue os textos, a CTA e as pendências.

Em **otimizar/auditar**: preserve o que funciona com dado; priorize oferta vencida e risco de política. Em **lote**: cada grupo com a verdade dos próprios produtos — sem clonar textos entre grupos; exportação só em formato verificado, sem afirmar publicação.

## Regras de qualidade
- **Escopo coerente**: todo claim vale para todos os produtos do grupo; grupo heterogêneo → claim comum ou divisão.
- **Atributo não vira efeito**: nada de saúde/resultado/estabilidade/"pé seco" que a ficha não prova.
- **Oferta, preço, frete, estoque reais** e consistentes com feed e página; nada de `[preencher]` publicado.
- **Modular**: cada texto funciona sozinho; combinações sem repetição nem contradição.
- **Diversidade de papel**, não de sinônimo; quantidade adaptativa.
- **Campos e limites vigentes** do PMax (não os do RSA), contagem exata, reescrever em vez de cortar.
- **Nome da empresa fiel**, sem slogan.
- **Automação tratada como dependência**: textos gerados, página auditada, expansão de URL com exclusões revisáveis, vídeo automático a revisar.
- **Sinais e temas** como orientação, não segmentação; sem atributo sensível.
- **Controles certos** para cada problema (marca × negativa × URL), disponibilidade a conferir.
- **CTA das opções da interface.**
- **Persuasão ética** (a mesma do Arsenal): sem "melhor do mundo", "imperdível", "última chance", "GRÁTIS!!!", urgência/escassez falsa, garantia de resultado. Categoria sensível com revisão de política.
- **Ad Strength não é ROAS**; nada de prometer resultado. **Voz da marca, não da Performa.**

### PMax Quality Gate (silencioso)
Campos compatíveis com a especificação vigente? · Contagem validada por código? · Quantidade adequada aos fatos? · Nome da empresa fiel? · Oferta ou prazo inventado? · Característica inventada ou esticada? · Prova social inventada? · Cada texto funciona sozinho? · Combinações sem contradição? · Diversidade real? · Claims válidos para todos os produtos do grupo? · Feed e página não contradizem? · Expansão de URL e textos gerados tratados como dependência? · Política, idioma e mercado revisados? · Pendências claras, sem afirmar publicação nem resultado? — se falhar, corrija.

## Formato da saída
Um resumo de uma linha do **escopo do grupo** e, em blocos, **Títulos (até 30) · Títulos longos (até 90) · Descrições (até 90, com a curta até 60) · Nome da empresa (até 25)** — cada linha numerada com a **contagem exata**. Depois: **1 CTA sugerida** (das opções da interface), as **pendências** (feed, página, automação, o que destravaria mais textos) e avisos objetivos.

Modo avançado (sob pedido): tabela `campo | texto | caracteres | papel | evidência | status`, mapa de combinações, lista de exclusões de URL a revisar, auditoria de um grupo existente, variações de teste com hipótese, ou formato estruturado para revisão/importação — sem afirmar que nada foi publicado.

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
