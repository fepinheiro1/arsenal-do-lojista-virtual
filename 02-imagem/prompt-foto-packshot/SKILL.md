---
name: prompt-foto-packshot
description: Monta o prompt/instrução da foto principal (packshot) de um produto de e-commerce priorizando fidelidade ao SKU real — preserva forma, cor, material, rótulo, logo e variante, adapta fundo e enquadramento ao canal (loja, Google Merchant, Amazon) e prefere editar uma foto real a gerar do zero. Aceita foto de referência, descrição, canal e finalidade. Use para a imagem principal de catálogo.
---

# Prompt de Foto Packshot

## O que faz
Produz a instrução para a foto principal (packshot) de um produto — com uma prioridade acima da estética: **fidelidade ao produto real que você vende**. Ela prefere orientar a *edição* de uma foto real (fundo, luz, recorte) a *gerar* a imagem do zero, porque a foto tem que ser o SKU que chega na casa do cliente — não uma versão "melhorada" que gera devolução. Com foto, vira instrução de edição; só com descrição, entrega um conceito e avisa que a fidelidade é baixa para uso definitivo.

Regra de ouro: **quanto mais a fidelidade importa, menos liberdade a IA recebe.** Você preenche em português; o prompt final sai em inglês (default interoperável).

## Quando usar
- Gerar ou ajustar a imagem principal de catálogo de um produto.
- Padronizar o fundo, a luz e o enquadramento de um catálogo inteiro.
- Preparar a imagem para um canal específico (loja própria, Google Shopping, Amazon) — cada um com sua regra.

## O que a IA precisa de você
O mais importante é uma **foto real** do produto (quanto melhor e mais completa, melhor). Além disso:
- `[produto]` — o que é, com cor, material, acabamento e detalhes reais.
- `[foto de referência]` — uma ou mais fotos reais, se tiver. Sem elas, o resultado é conceito, não SKU fiel.
- `[canal]` — loja própria, Google Merchant/Shopping, Amazon, marketplace (define fundo, enquadramento e regras).
- `[o que não pode mudar]` — rótulo, logo impresso, quantidade, variante, peças incluídas.

Sem canal, a skill gera uma versão neutra e avisa que o marketplace pode exigir adaptação.

## Como funciona (por baixo)

**1. Mede a confiança da referência (Reference Confidence).** Várias fotos boas = alta (pode compor com segurança) · uma boa = média · foto parcial/ruim ou só descrição rica = baixa · só texto = nenhuma. Quanto menor a confiança, menos liberdade para uma imagem comercial definitiva — e a skill avisa.

**2. Trava a verdade do produto (Fidelity Lock).** Separa três listas: **preservar** (forma, proporções, cor, material, acabamento, arte impressa, posição do logo, portas/botões, peças incluídas, variante) · **pode mudar** (fundo, exposição, suavidade da sombra, recorte/enquadramento, limpeza leve) · **proibido** (redesenhar, trocar cor, adicionar/remover partes, alterar logo/texto impresso, mudar tampa/alça/botão, acrescentar acessório, mudar a quantidade).

**3. Escolhe o modo pela referência.** **Editar** (tem foto real — o modo preferido; muda só o autorizado) · **Criar** (só descrição — conceito com aviso de fidelidade baixa para SKU real) · **Normalizar** (padroniza um conjunto) · **Auditar** (a imagem atende ao canal?) · **Variante** (só cria variação visual com referência/dado real da variante) · **Lote** (padroniza vários SKUs sem perder a identidade de cada um).

**4. O fundo e o enquadramento vêm do canal — não há default universal.** Loja própria: mais respiro e liberdade visual. Google Merchant: representa o produto claramente, sem promoção/watermark/borda, resolução recomendada alta. Amazon (imagem principal): fundo branco puro, produto ocupando ~85%+ do quadro, sem texto/watermark/prop, alta resolução para zoom. *Requisitos de marketplace mudam — a skill usa isso como ponto de partida e recomenda conferir a regra vigente do canal.*

**5. Não inventa o que a referência não mostra.** Uma foto frontal não documenta a traseira nem a lateral — um novo ângulo 3/4 sem referência exigiria inventar. A skill mantém o ângulo coberto pela foto, ou marca como conceito. Vale para lado oculto, hardware de eletrônico, número de pedras de uma joia.

**6. Luz e cor revelam, não maquiam.** Metal, vidro, tecido, fosco e couro pedem luz diferente — para mostrar o acabamento real, nunca para "premiumizar" ou trocar o material percebido. A cor é protegida (`preserve exact product color from reference`, `neutral white balance`, sem color grading no produto). Vidro/transparência e metal escovado têm cuidado extra: não encher a transparência com cor falsa, não criar reflexo "espelho" onde não há.

**7. Trata texto, logo e quantidade como parte do SKU.** "Sem logo/sem texto" cru é perigoso: o logo impresso e o rótulo *são* o produto. A skill usa `no added text/logo/watermark` (proíbe overlay promocional) e **preserva** o branding e o layout reais. A imagem mostra a quantidade vendida (bundle de 3 não vira 1) e só os itens incluídos.

## Instruções (o cérebro da skill) — Prompt Compiler
Em vez de blocos fixos, compile o prompt a partir do que a referência sustenta, nesta ordem:
1. **Product Truth** — o produto descrito com fidelidade (tipo, cor, material, acabamento, variante).
2. **Fidelity Lock** — o que preservar exatamente (geometria, cor, rótulo, logo, peças).
3. **Allowed changes** — o que pode mudar (fundo, luz, recorte).
4. **Composition** — ângulo coberto pela referência; produto centralizado; margem de segurança (não cortar alça, ponta, tampa, sola, cabo).
5. **Lighting** — a luz que revela o material real.
6. **Background** — vindo do preset do canal.
7. **Channel constraints** — fundo, ocupação do quadro, resolução, proibições do canal.
8. **Forbidden changes** — `no added text, no added logo, no watermark, no invented parts, no color change`.
9. **Output specs** — proporção e resolução do canal.
10. **Tool syntax (opcional)** — só quando a ferramenta é conhecida (`--ar 1:1` é do Midjourney; não emita como se fosse universal).

Rode o **Anti-Hallucination Gate** e entregue.

## Regras de qualidade
- **Fidelidade acima de estética**: nunca "melhore" o design físico. Se a IA muda cor, formato, logo, tampa ou quantidade, a foto engana na entrega.
- **Editar foto real > gerar do zero** para um SKU real. Geração só por texto = conceito, com aviso — bom para protótipo, arriscado como imagem definitiva.
- **Não invente ângulo/lado** que a referência não cobre; não invente conteúdo dentro de recipiente transparente; upscale não cria textura, logo ou detalhe que não existe na fonte.
- **Embalagem, cosmético, alimento, joia, eletrônico**: fidelity lock forte — rótulo, claims, quantidade e hardware são identidade comercial. Prefira foto real a regenerar o rótulo.
- **Metadata de IA**: se a imagem é gerada/editada por IA e o canal (ex.: Google Merchant) pede identificação de origem, **preservar** a metadata de proveniência — nunca sugerir removê-la para "parecer foto real".
- **Cleanup permitido** (poeira, sujeira, marca de fundo) sim; remover costura, textura ou característica real do material, não. Defeito daquela unidade vs característica do material: no caso ambíguo, não apague em silêncio.
- **Conflito referência × texto**: se a foto e a descrição divergem, pergunte — não escolha sozinho.
- A imagem é da loja do lojista, não da Performa: nenhum overlay ou marca nossa na arte.

### Visual Anti-Hallucination Gate (silencioso, antes de entregar)
Alguma parte foi inventada? · O ângulo revela área não documentada? · A cor mudou? · O material mudou? · Texto/logo mudou? · A quantidade mudou? · Entrou acessório não incluído? · A variante está correta? · O canal permite esse fundo/composição? · A imagem ainda representa exatamente este SKU? — se falhar, reduza o escopo (menos geração, mais edição) ou peça referência.

## Formato da saída
Mantendo tudo simples para o lojista:
1. **O prompt recomendado**, em inglês, num bloco de código, pronto para colar.
2. **O modo** em uma palavra: *editar foto real* (preferido) ou *conceito* (sem foto — fidelidade baixa para uso definitivo).
3. **Proporção e resolução** sugeridas para o canal.
4. **Um alerta curto** só se houver risco de fidelidade (ex.: "para o rótulo sair exato, edite a foto real em vez de gerar").

Nada de score ou relatório técnico. Sob pedido: versão para outro canal, variações de ângulo (só as cobertas pela referência), ou a sintaxe específica de uma ferramenta.

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
