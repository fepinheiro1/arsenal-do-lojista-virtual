---
name: prompt-cena-de-uso
description: Monta o prompt/instrução de uma cena de uso — uma pessoa usando o produto e demonstrando a função — preservando o SKU real e tratando a demonstração como prova comercial: só mostra ação que o produto realmente executa, do jeito que pode ser usado, com resultado que se sustenta. Cuida da anatomia das mãos, ergonomia, segurança e claims implícitos. Aceita foto de referência, produto, função/benefício, pessoa e canal. Use quando o benefício só fica claro com alguém usando.
---

# Prompt de Cena de Uso

## O que faz
Cria a instrução para a foto de alguém **usando** o produto — a imagem que responde "como isso funciona na minha vida?". É a mais delicada das três de imagem de produto, porque uma demonstração é quase uma prova: mostrar uma ação, um jeito de segurar ou um resultado é afirmar que aquilo é verdade. A skill preserva o produto (como o packshot), respeita o contexto (como o lifestyle) e ainda trava a **função e a ação**: só encena o que o produto realmente faz.

Regra de ouro: **mostre só uma ação que o produto realmente executa, de um jeito que ele realmente pode ser usado, com um resultado que realmente se sustenta.** Você preenche em português; o prompt final sai em inglês.

## Quando usar
- O benefício só fica claro quando alguém está usando (não só olhando).
- Você quer imagens de anúncio, PDP ou social que expliquem a operação.
- (Se tirar a pessoa/ação e a imagem ainda cumpre o objetivo, é **lifestyle**, não cena de uso.)

## O que a IA precisa de você
O ideal é **foto/vídeo real** do produto (e das superfícies que a ação toca). Além disso:
- `[produto]` — o que é, cor, material, variante reais.
- `[função confirmada]` — o que ele faz e como é operado (controles, passos).
- `[benefício observável]` — o que a cena pode mostrar acontecendo (sem prometer magnitude/tempo não comprovados).
- `[quem usa]` — perfil genérico coerente com o uso (sem citar pessoa real).
- `[canal]` — PDP, Google adicional/lifestyle, feed, story, anúncio.

## Como funciona (por baixo)

**1. Trava três verdades.** *Product Truth* (herdada: cor, material, rótulo, quantidade, variante — imutáveis), *Function Truth* (o que faz, como opera, quais controles existem, quais resultados são comprovados, quais limitações) e *Action Truth* (quem interage, como segura/veste, posição, controle acionado, sequência, força, resultado permitido, riscos). Nada fora do lock vira demonstração factual.

**2. Classifica o que dá para demonstrar.** *Diretamente demonstrável* (fechar tampa, encaixar peça, dobrar, transportar) → pode mostrar. *Contextualmente demonstrável* (compacto numa mesa, uso com uma mão, organização) → pode sugerir. *Não demonstrável com segurança* (durabilidade de anos, efeito médico, autonomia longa, resistência extrema) → **não encena**. O benefício só vira imagem quando é observável: "mantém quente" não autoriza mostrar "café fumegante horas depois".

**3. A imagem é um claim.** Suor sumindo, dor passando, cabelo perfeito, mochila na chuva, bateria "durando o dia", força aumentada — toda transformação visual é uma afirmação comercial. Só entra com base. Antes/depois é categoria de alto risco (cosmético, fitness, limpeza, saúde) e não é gerado por padrão.

**4. Escolhe o quadro decisivo da ação.** Uma cena = uma ação principal (no máximo uma secundária natural) — nada de abrir, usar, limpar e carregar ao mesmo tempo. O *Key Action Frame* explica a função sem legenda (mão apertando o controle certo, peça encaixada, item sendo vestido). Quando a operação é o valor, um **close funcional** nas mãos/controle costuma ser melhor que a pessoa inteira — e ainda reduz erro de anatomia.

**5. Mãos e ergonomia por estrutura, não por frase mágica.** "Correct anatomy" no prompt não garante mãos certas. A skill reduz a complexidade: enquadramento claro, uma ação por mão, menos dedos visíveis, sem cruzamentos, sem mão sumindo dentro do mecanismo — e define o *Hand-Product Interaction Lock* (onde segurar, orientação, quantas mãos, pegada e força plausíveis). Peso e esforço têm que parecer reais (nada de mala enorme erguida com dois dedos), e a escala do produto em relação à pessoa se mantém.

**6. Não inventa o que não existe.** Sem criar botão, touchscreen, LED, app, tela, métrica ou dashboard só para "explicar" o benefício. Se o app é real mas você não deu a interface, o celular fica desfocado ou sem conteúdo legível. Acessório e consumível (cápsula, filtro, refil) só aparecem como incluídos se acompanham de verdade; senão, ficam claramente externos ou fora de cena. Efeito invisível (som, aroma, purificação) não vira onda/aura como se fosse prova — melhor o contexto de uso.

**7. Segurança e casting a serviço da função.** Uso seguro por categoria: EPI em ferramenta, posição de mãos no calor da cozinha, nada de eletrônico na água quando a resistência não é conhecida, produto infantil com faixa etária e supervisão coerentes. A pessoa é **funcional** à demonstração (ajuda a mostrar escala, ergonomia, público e ação), com expressão que **vem da ação** (concentração, conforto, neutralidade) — não um sorriso publicitário padrão. Uniforme/jaleco que sugere endosso de especialista só com base real.

## Instruções (o cérebro da skill) — Prompt Compiler
1. Verifique a **cobertura de referência**: as fotos cobrem as superfícies/controles que a ação toca? Se não, reduza a cena ou peça referência.
2. Fixe **Product + Function + Action Truth** e **classifique** o benefício (direto / contextual / não demonstrável).
3. Escolha o **modo**: *editar/demonstrar* (tem referência — preferido) · *conceito* (só descrição, com aviso) · *storyboard* (2–4 frames com continuidade) · auditar / normalizar / lote.
4. Defina o **Key Action Frame**, o enquadramento (micro/médio/amplo) e o **Hand-Product Interaction Lock**.
5. Aplique os presets de **categoria** (segurança) e **canal** (crop, safe zone, pessoa, resolução).
6. Passe pelo **Claim + Safety + Continuity Gate** e compile o prompt em inglês, preservando a cor real; `--ar` só se a ferramenta for conhecida.

## Regras de qualidade
- **Produto, função e ação verdadeiros**: nunca redesenhe o produto, nunca demonstre função que ele não tem, nunca encene resultado não comprovado (tempo, magnitude, efeito médico, performance, durabilidade).
- **Benefício pela classe certa**: direto → mostra; contextual → sugere; não demonstrável → fica de fora.
- **Mãos por estrutura**: enquadramento simples, uma ação por mão, pegada e força plausíveis; escala pessoa × produto real.
- **Sem inventar** interface, app, display, métrica, acessório incluído ou consumível/compatibilidade.
- **Segurança por categoria**: EPI, calor, água, criança, ferramenta — nada de ensinar uso perigoso.
- **Sem before/after nem comparação** com concorrente ou "produto genérico" sem base.
- **Casting funcional, expressão da ação**; sem inferir atributo sensível do público; sem fantasiar especialista.
- **Apparel/wearable**: caimento e posição no corpo não se inventam de uma foto plana — exija referência ou marque conceito.
- Em série (storyboard), mantenha variante, pessoa, roupa, ambiente, luz e quantidade constantes.
- A cena é da loja do lojista, não da Performa.

### Visual Claim + Safety + Continuity Gate (silencioso)
SKU fiel e variante certa? · A função existe? · A ação está correta? · O resultado é demonstrável? · Anatomia e pegada plausíveis? · Peso/força plausíveis? · Escala certa? · Acessórios confirmados? · Alguma interface inventada? · Segurança (água/calor/risco) ok? · Algum claim médico/performance? · Crop/canal ok? · A série mantém continuidade? — se falhar, reduza o escopo, reformule ou peça referência.

## Formato da saída
1. **O prompt recomendado** em inglês, num bloco de código.
2. **O modo** numa palavra: *demonstrar com foto real* (preferido) ou *conceito* (sem foto — fidelidade baixa).
3. **Enquadramento, proporção e resolução** do canal.
4. **Um alerta curto** só se houver risco de claim, segurança ou fidelidade.

Sob pedido: uma **série (storyboard)** de 2–4 frames (preparar → operar → resultado factual), variações de enquadramento com propósito, ou a versão para outro canal. Nada de relatório técnico.

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
