---
name: prompt-foto-lifestyle
description: Monta o prompt/instrução de uma foto lifestyle — o produto no contexto real de quem compra — preservando o SKU real e tratando a cena como um claim comercial: ambiente, escala, clima, pessoas e props precisam ser plausíveis e verdadeiros, sem sugerir usos ou resultados não comprovados. Aceita foto de referência, produto, público/ocasião e canal. Use para imagens de contexto no catálogo, no feed ou no Google lifestyle.
---

# Prompt de Foto Lifestyle

## O que faz
Cria a instrução para a foto do produto no contexto de quem compra — a cozinha, o criado-mudo, a mesa de trabalho — para a pessoa se imaginar usando. Duas verdades andam juntas: a **do produto** (a mesma do packshot: cor, material, rótulo, quantidade não mudam) e a **do contexto** — porque uma cena afirma coisas mesmo sem texto. Um relógio dentro d'água diz "à prova d'água"; folhas verdes ao redor dizem "eco"; um antes/depois diz "resultado". A skill trata a imagem como um claim: só mostra o que é verdadeiro.

Regra de ouro: **o cenário pode inspirar; o contexto não pode mentir.** Você preenche em português; o prompt final sai em inglês.

## Quando usar
- Dar contexto ao produto que já tem packshot (feed, PDP, campanha).
- Gerar a imagem de estilo de vida do Google Shopping (`lifestyle_image_link`).
- Mostrar escala e momento de uso sem produção fotográfica.
- (Se a pessoa vai *usar ativamente* o produto, demonstrando a função, o job é da skill **cena-de-uso**, não desta.)

## O que a IA precisa de você
O ideal é uma **foto real** do produto (para editar/compor, não recriar). Além disso:
- `[produto]` — o que é, cor, material, variante reais.
- `[uso confirmado]` — para que serve de verdade (define o ambiente e evita claim falso).
- `[público / ocasião]` — para quem e em que momento (manhã, deslocamento, fim de semana).
- `[canal]` — loja, Google lifestyle, feed social, campanha (define proporção, crop e presença de pessoa).

Público é opcional e só orienta o **contexto**, nunca altera o produto — e nunca vira estereótipo.

## Como funciona (por baixo)

**1. Trava duas verdades.** *Product Truth* (herdada do packshot: geometria, cor, material, rótulo, logo, quantidade, variante — imutáveis) e *Scene Truth*: uso permitido, escala, local plausível, orientação física, o que é/não é incluído, condições ambientais e público quando confirmado.

**2. Usage Truth — a cena não inventa uso.** Não mostra o produto fazendo o que não foi confirmado: relógio submerso (impermeabilidade), caixa de som na piscina, panela em indução sem compatibilidade, mochila com peso extremo, cosmético com resultado clínico. Antes de fechar a cena, pergunta: *"o que um comprador concluiria olhando isto?"* — se a conclusão não se sustenta, muda a cena.

**3. O ambiente nasce do uso, não do bonito.** Produto → uso confirmado → ocasião → ambiente plausível (travesseiro → quarto; cafeteira → cozinha; mochila urbana → transporte). Ocasião mapeada (rotina, hora, local, atividade) rende cena específica, não um "cozy kitchen" genérico. Sem estereótipo (não "feminino = tudo rosa", "executivo = escritório de luxo", "mãe = cozinha").

**4. Escala honesta.** Quando o tamanho importa, usa uma âncora conhecida e proporcional (mão, mesa, notebook) — nunca um prop enganoso (a bolsa ao lado de uma xícara miniatura para parecer maior), e nunca aumenta/diminui o produto para ficar mais "hero".

**5. Realismo físico.** Sombra de contato coerente, produto apoiado (sem flutuar nem atravessar objetos), perspectiva e horizonte compartilhados entre produto e cenário, e posição compatível com a função (TV apoiada/fixada, luminária com base, aparelho com ventilação livre). Nada de uso inseguro (eletrônico na água, vela perto de inflamável, criança em situação inadequada).

**6. Luz e profundidade são adaptativas — não uma fôrma.** A profundidade de campo depende da narrativa (rasa para atmosfera, média/profunda quando o contexto precisa ser lido) — não `shallow` obrigatório. A luz também (janela, golden hour, difusa, ambiente, noturna, estúdio natural), conforme a ocasião — e sempre preservando a **cor real** da variante (golden hour/neon não podem falsear a cor; controlar o white balance quando a cor é atributo comercial).

**7. Props e pessoas com função e sem claim indevido.** Props (0–3) contextualizam, ajudam a escala ou compõem — não enchem, e não podem parecer *incluídos na caixa* (afaste ou use prop claramente ambiental). Pessoa entra como **apoio** (mão, silhueta, corpo parcial, desfocada), com anatomia correta (mãos!), e coerente com o uso confirmado — a escolha de pessoa não pode sugerir faixa etária, indicação, segurança ou benefício de saúde sem base.

**8. Aspiracional sem inflar, e coerente com a marca.** A cena pode ser bonita, mas plausível para o posicionamento (uma cafeteira doméstica não vira equipamento de cafeteria profissional; nem todo produto merece mármore e hotel cinco estrelas). Com a identidade visual da marca, um pequeno *Style Bible* (luz, paleta, materiais, câmera) guia o cenário — sempre secundário ao produto. Sazonalidade e local só quando relevantes, atuais e sem sugerir promoção inexistente nem cultura de fachada.

## Instruções (o cérebro da skill) — Prompt Compiler
1. Fixe **Product Truth** e **Scene Truth** (uso, escala, local, incluídos, ambiente, público confirmado).
2. Escolha o **modo**: *editar/compor* (tem foto real — preferido: insere o produto real no cenário) · *conceito* (só descrição, com aviso) · normalizar / auditar / variante / lote.
3. Derive o **ambiente** do uso e da ocasião; escolha a **âncora de escala** se o tamanho importa.
4. Ajuste **DOF, luz e composição** à narrativa e ao **canal** (proporção, crop/safe zones, presença de pessoa, resolução).
5. Passe pelo **Claim + Safety + Fidelity Gate** e compile o prompt em inglês, preservando a cor real; sintaxe de ferramenta (`--ar`) só se a ferramenta for conhecida.

## Regras de qualidade
- **Produto imutável, contexto verdadeiro**: nunca altere cor, material, rótulo, quantidade ou variante; nunca mostre uso, resultado ou condição não confirmados.
- **A imagem é um claim**: sem dramatizar performance (gotas para "waterproof", gelo/fogo, partículas mágicas, velocidade), sem green claim visual (folhas/eco sem base), sem antes/depois ou resultado clínico em beleza/wellness.
- **Escala real**, âncora honesta, produto no tamanho certo.
- **Realismo físico e segurança**: contato, perspectiva e placement plausíveis; nada de uso inseguro.
- **Pessoas de apoio** com mãos corretas e sem criar claim de idade/indicação/saúde; criança e pet só quando coerentes e seguros.
- **Cor fiel sob luz ambiente**; atmosfera sim, cor falsa não.
- **Props não incluídos** não podem parecer parte da compra.
- **Sazonal/cultural/local** só quando relevante e atual (sem reusar coleção antiga, sem sugerir promoção).
- A cena é da loja do lojista, não da Performa: sem overlay ou marca nossa.

### Visual Claim + Safety + Fidelity Gate (silencioso)
Produto fiel e variante certa? · Escala plausível? · Ambiente coerente com o uso real? · O uso implícito é verdadeiro? · Os props confundem o que vem na caixa? · A pessoa cria um claim indevido? · A luz alterou a cor? · Segurança ok? · Perspectiva e contato físico ok? · Canal/crop ok? · **A cena parece publicidade enganosa?** — se falhar, reescreva ou reduza o escopo.

## Formato da saída
1. **O prompt recomendado** em inglês, num bloco de código.
2. **O modo** numa palavra: *editar foto real* (preferido) ou *conceito* (sem foto — fidelidade baixa).
3. **Proporção e resolução** do canal (com safe zone, se for servir a vários).
4. **Um alerta curto** só se houver risco de claim ou fidelidade.

Sob pedido: variações com propósito (contexto A × B, com/sem âncora de escala, público/ocasião diferente quando legítimo) — não trocas decorativas sem hipótese. Nada de relatório técnico.

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
