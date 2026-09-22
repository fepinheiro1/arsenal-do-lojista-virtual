---
name: prompt-troca-de-fundo
description: Monta a instrução de edição para trocar, remover ou expandir o fundo de uma foto de produto que você já tem — preservando os pixels do produto (forma, cor, rótulo, bordas, transparência), com estratégia própria de sombra e reflexo, presets por canal e normalização de catálogo. Aceita a foto real, o objetivo e o canal. Use quando a foto é boa mas o fundo precisa mudar, ou para padronizar o catálogo.
---

# Prompt de Troca de Fundo

## O que faz
Gera a instrução de **edição** para uma IA que edita a sua foto (não que gera do zero): troca, remove ou expande o fundo **preservando o produto pixel a pixel**. A ideia central é o contrário de "regerar a foto bonita": já que você tem o produto real fotografado, a IA tem que **provar que preserva o produto** antes de ganhar liberdade no entorno. Ela protege o produto (forma, cor, rótulo, bordas, transparência), edita só o fundo, e cuida da sombra e do reflexo com estratégia — não no automático.

Regra de ouro: **preservar os pixels do produto; editar só o ambiente ao redor.** Você preenche em português; a instrução final sai em inglês.

> Requer uma IA que **edita** a sua imagem (você anexa a foto). Se a ferramenta aceita máscara/seleção, selecionar o produto e editar só o fundo é mais confiável que prompt sozinho.

## Quando usar
- A foto do produto é boa, mas o fundo é poluído, escuro ou fora do padrão do marketplace.
- Você quer **padronizar o catálogo inteiro** no mesmo fundo, crop e alinhamento.
- Precisa da imagem em PNG transparente, ou expandir o quadro (4:5 → 16:9) sem esticar.
- (Se você quer o produto numa rotina rica, é `prompt-foto-lifestyle`; se quer um hero com espaço de texto, é `prompt-banner-campanha`.)

## O que a IA precisa de você
- `[foto do produto]` — a imagem real, anexada na IA de edição.
- `[produto]` — o que é (para a IA saber o que proteger).
- `[objetivo]` — remover (transparente), fundo neutro (marketplace), cena, ou expandir o quadro.
- `[canal]` — Amazon, Google Merchant, loja própria, marketplace (define o fundo padrão).
- `[novo fundo]` — se for neutro (branco/cinza) ou uma cena específica.

## Como funciona (por baixo)

**1. Trava a verdade dos pixels.** Separa a imagem em três: **região do produto** (protegida — geometria, cor, material, rótulo/logo/texto, costura, botões, portas, quantidade, transparência), **fundo** (editável) e **transição** (as bordas, a sombra e as áreas translúcidas — onde mora o risco). Só o fundo e o que você autorizar muda.

**2. Escolhe o modo — não é tudo "trocar fundo".** *Remover* (fundo → transparente, PNG com alpha, sem halo, preservando os vazios internos — branco não é transparente) · *Fundo neutro* (branco/cinza de estúdio) · *Cena* (compositing controlado) · *Expandir o quadro* (outpaint: cria pixels **ao redor**, o produto mantém tamanho e posição) · *Limpeza* (tira artefato de captura) · *Normalizar catálogo* · auditar · lote.

**3. Lê a borda antes de recortar.** Borda dura, tecido/fibra, cabelo/pelo, malha/renda, translúcido, reflexivo — cada uma pede um tratamento. Um recorte agressivo não pode "comer" a pelúcia, fechar os buracos de uma cesta/renda, nem descolorir a borda ao remover o *spill* (contaminação de cor do fundo antigo). Vidro e acrílico preservam transparência, refração e highlights (o novo fundo aparece através do objeto); metal e telas glossy carregam reflexos do ambiente antigo, que podem precisar de tratamento.

**4. Sombra e reflexo por estratégia, não por padrão.** A skill **não adiciona sombra automaticamente** (a V1 fazia). Ela classifica a sombra original — boa, contaminada, ausente ou inadequada — e decide: preservar, limpar, reconstruir ou remover. Contato ancora o produto; projetada revela a luz. Se o produto está legitimamente suspenso, não força sombra. Reflexo de piso idem — nada de "reflexo premium" só para embelezar.

**5. Integra sem recolorir nem distorcer.** Adapta o fundo à luz que já existe no produto (direção, dureza, temperatura) — mais seguro do que relightar o SKU inteiro (isso é outra operação, com QA mais forte). O novo fundo **não recolore** o produto (white balance preservado). Em cena com superfície, casa perspectiva, escala e contato (a base toca a superfície sem gap nem afundamento), sem redimensionar o produto para "caber bonito".

**6. O novo fundo também é um claim.** Água sugere impermeabilidade; cozinha profissional sugere uso profissional; ambiente infantil sugere uso por criança; outdoor sugere adequação externa. A skill aplica o mesmo cuidado de claim das outras skills de imagem: só o cenário que a verdade sustenta.

**7. Preferência e limites.** A ordem é: **máscara + edição só do fundo** > compositing com o produto protegido > outpaint fora da região protegida > regenerar parte do produto (só quando explicitamente necessária). Upscale melhora a apresentação, mas **não inventa** texto, textura, costura, logo ou hardware — se a foto-fonte é ruim, a skill sinaliza a limitação em vez de "criar" detalhe.

**8. Normalizar catálogo — o uso mais valioso.** Fotos heterogêneas → mesmo fundo, mesmo crop, mesma escala aparente, mesma sombra e alinhamento, sem alterar cada SKU. Produtos da mesma família ficam com escala coerente (mas sem fazer itens de tamanhos diferentes parecerem iguais, o que enganaria). Em lote, itens difíceis (vidro, pelo, reflexo, rótulo complexo, baixa resolução) saem do fluxo automático e são sinalizados para revisão.

## Instruções (o cérebro da skill) — Prompt Compiler
1. Fixe o **Pixel Truth** (região protegida, rótulo/logo/texto, cor, geometria, detalhes, transparência, itens incluídos).
2. Analise **borda, transparência e reflexo** e escolha o **modo**.
3. Aplique o **preset de canal/catálogo** (fundo padrão, crop, resolução para zoom).
4. Defina a **estratégia de sombra e reflexo** (preservar/limpar/reconstruir/remover) e a **integração** (luz, perspectiva, escala, contato).
5. Passe pelo **Pixel Fidelity Gate** e compile a instrução em inglês (usa máscara quando a ferramenta permite), com `do not add new text; preserve existing product text and labels exactly; no added logo, no watermark`.

## Regras de qualidade
- **Produto pixel-preservado**: se a IA muda cor, forma, textura, rótulo ou quantidade, rejeite o resultado — a foto passaria a mentir sobre a entrega.
- **Texto/logo físicos preservados**: "sem logo/sem texto" vale só para overlay adicionado.
- **Bordas e vazios corretos**: sem halo, sem resíduo do fundo antigo, sem fechar buraco de malha/renda, sem comer fibra/pelo; transparência de vidro preservada.
- **Sombra/reflexo com base**: nada de sombra ou reflexo inventado por padrão; produto não pode flutuar nem afundar na superfície.
- **Cor real**: novo fundo não recolore o SKU; corrija white balance/spill só quando seguro; sem grading que troque a variante.
- **Defeito × característica**: veio da madeira, textura do couro e costura aparente são reais (não "consertar"); risco acidental daquela unidade, no ambíguo, pergunte antes de remover.
- **Cena não vira claim**: água/cozinha-profissional/infantil/outdoor só quando a verdade sustenta.
- **Sem inventar** detalhe via upscale; fonte ruim → sinalizar.
- A imagem é da loja do lojista, não da Performa.

### Pixel Fidelity Gate (silencioso)
Produto pixel-preservado? · Bordas intactas? · Halo/spill? · Vazios internos corretos? · Transparência correta? · Reflexos coerentes? · Sombra coerente? · O produto flutua? · Perspectiva/escala corretas? · Texto/logo intactos? · A cor mudou? · O crop cortou algo (alça, tampa, cabo, sola)? · Canal atendido? · O upscale inventou detalhe? · O cenário cria claim falso? — se falhar, rejeite e reprocesse.

## Formato da saída
1. **A instrução de edição** em inglês, num bloco de código, pronta para colar na IA que recebe a sua foto (com nota de usar máscara/seleção quando houver).
2. **O modo** (remover / neutro / cena / expandir / normalizar).
3. **Fundo, proporção e resolução** por canal (com aviso quando o marketplace não foi informado).
4. **Um alerta curto** só se houver risco (vidro, pelo, reflexo, rótulo, baixa resolução, claim de cena).

Sob pedido: o **Style Lock de catálogo** (fundo, baseline, alinhamento, sombra, margem) para normalizar vários SKUs, e a lista de exceções que pedem revisão manual. Nada de relatório técnico.

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
