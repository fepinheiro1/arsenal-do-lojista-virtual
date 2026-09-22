---
name: prompt-banner-campanha
description: Monta a composição/prompt de um banner ou hero de campanha para e-commerce — com o texto (headline, preço, CTA) FORA da imagem e uma copy zone funcional reservada — preservando produto, oferta e marca, controlando claims visuais e gerando versões irmãs para cada formato. Aceita conceito, produto/oferta, identidade da marca e canais. Use para hero de site, banner de coleção/data comercial e peças de campanha.
---

# Prompt de Banner de Campanha

## O que faz
Cria a **arte de fundo** de um banner de campanha como um sistema, não como "produto de um lado, espaço vazio do outro". O texto (headline, preço, desconto, CTA) **não entra na imagem** — entra depois como camada no editor/HTML, porque a IA erra letra, um preço embutido vira risco de propaganda enganosa, e o texto separado melhora acessibilidade, tradução, atualização e testes. A arte reserva uma **copy zone funcional** (área calma, com contraste previsível para o texto), preserva o produto/oferta/marca e gera versões coerentes para cada formato.

Regra de ouro: **a criatividade pode mudar a atmosfera; não pode mudar o produto, a oferta ou a verdade da campanha.** Você preenche em português; o prompt final sai em inglês.

## Quando usar
- Hero de topo de site, banner de coleção, lançamento ou data comercial.
- Você tem o conceito e a oferta e precisa da arte com espaço real para o texto.
- Precisa da mesma campanha em vários formatos (desktop, mobile, feed, story).

## O que a IA precisa de você
- `[conceito da campanha]` — a ideia, o objetivo, o período/coleção, a ocasião.
- `[produto ou cena]` — o que aparece (com cor/material reais); idealmente uma foto real para recortar.
- `[oferta]` — só para você ter em mãos; **preço, desconto e condições entram por cima, no editor** — nunca na arte.
- `[cores/identidade da marca]` — a arte usa as suas cores, não as da Performa.
- `[canais/formatos]` — hero desktop, mobile, 4:5, 1:1, 9:16 (define composição e safe zones).
- `[onde o texto vai]` — o lado/zona reservada para a copy.

## Como funciona (por baixo)

**1. Trava as verdades da campanha.** *Campaign Truth* (conceito, objetivo, período, coleção, mensagem, público — não inventa campanha), *Offer Truth* (preço, desconto, cupom, parcelamento, validade — ficam fora da arte, nunca inventados), *Product Truth* (herdada: SKU, variante, cor, material, branding físico, quantidade), *Brand Truth* (paleta, formas, mood, densidade — da marca, não um "premium" genérico) e *Layout Truth* (quais elementos vão por cima: eyebrow, headline, preço, CTA, badge, disclaimer). A criatividade acontece dentro desses limites.

**2. A arte também faz claims.** Chuva sugere impermeabilidade; folhas sugerem "eco"; multidão e pilha de pedidos sugerem popularidade; cronômetro e "prateleira vazia" sugerem escassez; mármore e hotel sugerem posicionamento. **"50% OFF" não autoriza** explosão, urgência, fila ou estoque acabando na imagem. Energia sim; fato inexistente não — sem scarcity, popularity, sustainability ou performance sem base.

**3. Reserva uma copy zone funcional.** Não é "espaço vazio à esquerda": é uma área de **baixa complexidade visual** e **contraste previsível** (se o texto vai ser branco, a zona é escura e estável; se escuro, clara), com margem e tamanho suficientes para a headline, o benefício, o CTA e os disclaimers caberem com legibilidade (mirando o contraste que um banner acessível pede). Nada de padrão, objeto ou brilho atrás do texto.

**4. Compõe com foco e hierarquia.** Define o *focal point* (produto, coleção ou detalhe) sem competir com a copy; a imagem permite a ordem de leitura focal → headline → oferta → CTA → detalhes. Pistas direcionais (olhar, linhas, luz) conduzem ao texto/CTA sem pose forçada. O produto **não** precisa ficar centralizado — a posição nasce da copy zone e do formato.

**5. Trabalha multi-formato de propósito.** Desktop e mobile têm áreas úteis diferentes — um 16:9 cortado não vira um bom 9:16. A skill gera composições **irmãs** (mesma campanha, composição adaptada) e protege **safe zones** (produto, rosto, mãos, copy e CTA longe das bordas e das UIs de header/Stories/Reels). Para `object-fit: cover`, mantém o sujeito numa área segura, não só define a proporção.

**6. Prefere recortar o produto real a regenerá-lo.** O workflow forte de campanha é **packshot real recortado + cenário/fundo gerado** — preserva o SKU e libera a criatividade no mundo à volta. Ao compor, perspectiva, luz, sombra, escala, temperatura e contato precisam casar (nada de produto "colado").

**7. Resolução e peso pelo destino.** Nada de pedir "8K" ou "ultra high resolution" por padrão — o hero pesa no carregamento (LCP). A skill define o tamanho pelo destino (desktop, mobile, feed, story, display) e deixa a otimização para depois. Elementos decorativos (luz, formas, confete) e motion entram se combinam com a marca, não parecem itens incluídos, não cobrem produto/copy e não criam claim — e o motion blur nunca embaralha a leitura do SKU.

## Instruções (o cérebro da skill) — Layout Compiler
1. Detecte o **tipo** (produto único / múltiplos / coleção) e fixe **Campaign + Offer + Product + Brand + Layout Truth**.
2. Escolha o **modo**: *editar/compor* (packshot real + mundo gerado — preferido) · *criar* (conceito do zero) · *adaptar* (campanha aprovada → outro formato) · normalizar / auditar / variante / lote.
3. Defina **focal point**, **copy zone** (lado, contraste, margem) e **safe zones** por formato/canal.
4. Componha cena, fundo, luz e decoração dentro da marca; mantenha o produto fiel e a hierarquia clara.
5. Gere as **versões irmãs** dos formatos pedidos (composição própria, não só crop).
6. Passe pelo **Claim + Brand + Layout + Responsive Gate** e compile o prompt em inglês, com `no added text/letters/words/logo/watermark`; `--ar` só se a ferramenta for conhecida.

## Regras de qualidade
- **Texto fora da arte**: headline, preço, %, cupom, CTA e disclaimer entram por cima — os números reais você preenche, a IA nunca inventa. "No text" = *no added campaign text* (o rótulo/logo físico do produto é preservado).
- **Verdade de campanha e oferta**: não invente conceito, coleção, sortimento, preço ou condição.
- **Claim visual controlado**: sem urgência/escassez/popularidade/eco/performance falsas; energia pode, fato inexistente não.
- **Copy zone real**: área calma, com contraste previsível e espaço para o texto — não um fundo caótico atrás da mensagem.
- **Estilo da marca, não "premium" padrão**; a arte usa as cores do lojista.
- **Multi-produto/coleção**: preserve quantidade, variantes e escala; defina o hero; não sugira bundle que não é vendido junto; não invente produtos.
- **Pessoas** só quando fortalecem o conceito (product-led / person-led / balanced), sem roubar o hero, sem celebridade ou pessoa real inventada, sem estereótipo.
- **Sazonal/local**: atual (sem reusar data de outro ano) e sem clichê obrigatório (Natal não exige neve; "winter sale" no Brasil não herda neve europeia).
- **Resolução pelo destino**, sem "8K" default; decoração e motion não alteram o produto.

### Campaign Quality Gate (silencioso)
SKU fiel? · Sortimento real? · Oferta não inventada? · Claim visual sustentado? · Marca coerente? · Copy zone suficiente e com contraste? · Focal point claro? · O CTA terá espaço? · Crop e mobile funcionam? · A UI não cobre elementos? · Sazonalidade atual? · Bundle/escassez/popularidade não foram sugeridos falsamente? · Peso/LCP considerado? · Os formatos irmãos parecem a mesma campanha? — se falhar, reformule a composição.

## Formato da saída
1. **O prompt recomendado** em inglês (a arte de fundo), num bloco de código, com a copy zone descrita.
2. **O modo** numa palavra: *compor com packshot real* (preferido) ou *criar do zero*.
3. **Formato(s), proporção e resolução** por destino, com as safe zones.
4. **Lembrete** de que o texto/oferta entra por cima no editor (números reais preenchidos por você).

Sob pedido: as **versões irmãs** (desktop, mobile, 4:5, 1:1, 9:16), variações A/B com hipótese (product-led × contextual, close × wide, com/sem pessoa), ou um pequeno *Style Bible* para a campanha inteira. Nada de relatório técnico.

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
