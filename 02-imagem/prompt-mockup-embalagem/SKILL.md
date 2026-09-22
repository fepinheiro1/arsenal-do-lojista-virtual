---
name: prompt-mockup-embalagem
description: Monta o prompt/instrução de um mockup de embalagem (caixa, pote, frasco, sachê, tubo) preservando estrutura, artwork e informação factual do rótulo — aplica a arte real como decal em vez de reescrevê-la, nunca inventa texto regulatório (ingredientes, tabela nutricional, registro, peso, código de barras) e deixa a criatividade só na luz/câmera/fundo. Aceita a estrutura, a arte real e o objetivo. Use para visualizar a embalagem antes de imprimir ou como imagem de apresentação.
---

# Prompt de Mockup de Embalagem

## O que faz
Cria a instrução para um mockup realista da sua embalagem — mas com uma fronteira clara: a IA pode inventar a luz do estúdio, **não pode inventar o que está escrito no rótulo**. A skill separa três camadas: a **estrutura** (formato, tampa, dimensões), o **artwork/rótulo** (logo, cores, textos) e o **rendering** (câmera, luz, fundo) — e a liberdade criativa fica quase toda na terceira. Se você tem a arte final, ela é **aplicada** como um decal, não redesenhada; o que você não tem vira área neutra marcada, nunca texto de aparência real.

Regra de ouro: **a luz é livre; o rótulo é verdade.** Você preenche em português; o prompt final sai em inglês.

> Mockup é visualização, não arte de produção: não substitui dieline, prova de impressão, preflight nem validação regulatória.

## Quando usar
- Ver como a embalagem se apresenta antes de imprimir, ou ter uma imagem de apresentação.
- Aplicar a arte final (PDF/PNG) numa estrutura para o packshot do anúncio.
- Comparar acabamentos (fosco × brilhante × foil) sem mudar a arte.
- (Se você já tem a foto da embalagem real e só quer trocar o fundo, é `prompt-troca-de-fundo`.)

## O que a IA precisa de você
- `[estrutura]` — tipo (caixa, pote, frasco, sachê, tubo, lata, pouch), dimensões/referência, tampa/pump/válvula.
- `[artwork]` — a arte real do rótulo (o ideal, para aplicar como decal) ou o que aparece nele.
- `[material e acabamento]` — kraft, PET, vidro âmbar, alumínio; fosco, brilhante, soft-touch, foil, verniz localizado.
- `[objetivo]` — conceito (explorar) ou fiel à produção (arte/estrutura reais).

Sem a arte final: a skill usa **placeholder** (área neutra) e marca `[preencher]` — nunca gera pseudo-texto que pareça informação real.

## Como funciona (por baixo)

**1. Trava as camadas de verdade.** *Structure Truth* (formato, dimensões, tampa, faces — não inventa estrutura; e "300 ml" não define diâmetro/altura), *Artwork Truth* (logo, cores, tipografia, textos — aplicados da arte real, não reescritos), *Regulatory Truth* (ingredientes, tabela nutricional, peso, lote, validade, registro, advertências, selos — nunca inventados), *Material/Finish Truth* e *Variant Truth*. A liberdade fica em **câmera, luz, fundo e apresentação**.

**2. Escolhe o modo.** *Conceito* (explora formato/material/acabamento, marcado como conceito) · *Aplicar artwork* (a arte real vira decal na estrutura — o caminho fiel) · *Renderizar* (estrutura + arte aprovadas) · *Comparar acabamento* (fosco/brilho/foil sem mudar a arte) · *Conjunto de vistas* · auditar · família/variante · lote.

**3. Texto e dado crítico não são gerados.** Ingredientes, tabela nutricional, peso/volume, lote, registro (ANVISA/MAPA), alergênicos e advertências vêm da **arte/dado real** ou ficam como pendência — nunca estimados, completados ou "parecidos". O nome da marca, para um SKU comercial, é melhor pelo **logo/wordmark real** (nome curto gerado ainda sai errado). O verso (que concentra o texto regulatório) fica fora de vista ou em placeholder, se você não deu a arte traseira.

**4. Código de barras, QR e selos são dados, não decoração.** Não gera barras nem QR que **pareçam** válidos: para conceito, placeholder claramente não-funcional; para produção, o asset real aplicado (preservando proporção e contraste). Selos de certificação (orgânico, vegano, FSC, reciclagem) e símbolos técnicos só entram quando você fornece — nada de selo "bonito" inventado.

**5. Estrutura, material e acabamento com fidelidade.** Respeita faces (não move conteúdo entre frente/lateral/verso), orientação (não espelha a arte), emendas e dobras (sem repetir a arte num loop impossível; pouch com selos/gusset; rótulo cilíndrico com wrap sem redesenhar o logo). O material (kraft, vidro, alumínio, filme) muda reflexo e dobra; o acabamento (fosco/brilho/foil/spot UV/emboss) aparece em highlight e relevo, **só na área especificada** — sem máscara, é conceito. Vidro/transparência preserva parede, refração e o que se vê dentro (a cor do vidro âmbar é material, não um filtro global).

**6. Ângulo pelo objetivo, não 3/4 por padrão.** Frontal para ler o rótulo, 3/4 para mostrar a estrutura, lateral para profundidade, top-down para a tampa, macro para o acabamento. Um conjunto multi-vista (frente/3-4/lateral/verso/detalhe) só quando você tem a arte de cada face — sem inventar o verso.

**7. Não promete produção.** A cor no mockup (RGB) não é a cor impressa (CMYK/Pantone) — a skill não afirma que serão idênticas. E um visual pode ser industrialmente inviável (foil sobre dobra, relevo na emenda, janela impossível): quando o conceito usa estrutura/acabamento complexos, ela **alerta para validar com a gráfica** e nunca diz "pronto para impressão".

## Instruções (o cérebro da skill) — Prompt Compiler
1. Fixe **Structure + Artwork + Regulatory + Material/Finish + Variant Truth**; separe o que é dado real do que é placeholder.
2. Escolha o **modo** (conceito / aplicar / renderizar / acabamento / vistas / família / lote).
3. Aplique a **arte real como decal** quando houver; senão, área neutra marcada.
4. Componha **câmera, luz e fundo** (a parte livre), respeitando material, acabamento, faces e emendas.
5. Passe pelo **Fidelity + Regulatory + Manufacturability Gate** e compile o prompt em inglês; `--ar` só se a ferramenta for conhecida.

## Regras de qualidade
- **Nunca invente** o que vai no rótulo: ingredientes, tabela nutricional, peso/volume, lote, registro (ANVISA/MAPA), advertência, alergênico. Sem o dado → área em branco / `[preencher]`.
- **Sem claim nem selo inventado**: "detox", "imunidade", "clinicamente comprovado", "hipoalergênico", "nº 1", prêmio, orgânico, vegano — só com arte/autorização real (o visual também cria claim por ícone).
- **Barcode/QR**: nunca gere um que pareça funcionar; placeholder para conceito, asset real para produção.
- **Artwork aplicado, não reescrito**: preserve logo, tipografia, cores e spacing da arte real; texto gerado pela IA sai torto/errado.
- **Estrutura/material/acabamento fiéis**: sem inventar estrutura, sem espelhar a arte, sem foil/relevo/spot onde não foi especificado; volume não define geometria.
- **Cor não é prova de impressão** (RGB ≠ CMYK/Pantone); não afirme conformidade nem "print-ready".
- **Variante** só com a arte real daquela variante (não troque só uma cor e ache que criou o SKU); multipack com a quantidade real.
- A embalagem é da marca do lojista, não da Performa.

### Packaging Quality Gate (silencioso)
Estrutura e proporção plausíveis? · Face correta? · Artwork preservado, texto/logo sem corrupção? · Cor preservada? · Barcode/QR real ou claramente placeholder? · Algum dado regulatório inventado? · Peso/volume corretos? · Variante certa? · Acabamento na área certa? · Material parece correto? · Transparência plausível? · Emenda/dobra respeitadas? · Verso inventado? · Multipack correto? · O render sugere claim/certificação inexistente? · Algo foi dado como "print-ready" sem validação? — se falhar, reformule ou peça o asset/dado.

## Formato da saída
1. **O prompt recomendado** em inglês, num bloco de código (com nota de aplicar a arte real como decal, quando houver).
2. **O modo** (conceito / aplicar artwork / renderizar) e o que ficou como **placeholder**.
3. **Ângulo, proporção e resolução** conforme o objetivo.
4. **Um alerta curto** só se houver risco (dado regulatório ausente, acabamento/estrutura a validar na gráfica, cor de impressão).

Sob pedido: um **conjunto de vistas** (só das faces com arte), a comparação de acabamentos, ou um **style lock de família** para visualizar a linha. Nada de relatório técnico.

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
