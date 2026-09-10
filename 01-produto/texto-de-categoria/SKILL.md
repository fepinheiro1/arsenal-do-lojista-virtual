---
name: texto-de-categoria
description: Analisa e otimiza o conteúdo de páginas de categoria, coleção e listagem (PLP) para e-commerce — adaptando profundidade, orientação de escolha, subcategorias, filtros e links internos à intenção e ao sortimento real, sem criar filler de SEO. Aceita a categoria, uma URL, o catálogo ou o texto atual. Use ao criar, melhorar ou auditar uma página de categoria.
---

# Texto de Categoria

## O que faz
Entende que tipo de página de catálogo é aquela, o que o comprador precisa para avançar, e qual conteúdo **realmente merece existir** — e só então escreve. Não é "escreva 100 palavras com a keyword da categoria": a profundidade nasce da utilidade, não de uma contagem de palavras. Às vezes a resposta certa é uma intro curta, às vezes uma orientação de escolha, às vezes não colocar texto nenhum e priorizar as subcategorias.

Regra de ouro: **entenda a página e a intenção; o SEO é consequência de uma página útil.** Simples na superfície, especialista por baixo.

## Quando usar
- Criar o conteúdo de uma página de categoria, coleção ou listagem.
- Melhorar uma página com texto genérico ou "parede de texto" antes dos produtos.
- Auditar categorias (duplicação, canibalização, facetas, sazonal vencido).
- Classificar e tratar muitas categorias de uma vez (modo em lote).

## O que a IA precisa de você
No mínimo, a **categoria** (nome + o que ela reúne), ou uma **URL** (com web; se não, descreva a página), ou o **catálogo/sortimento**, ou o **texto atual** para melhorar.

Opcional e valioso: as subcategorias e filtros reais, a intenção (a pessoa quer navegar? comparar? um tema sazonal?) e dados de popularidade *reais* (mais vendidos). Sem isso, a skill infere a intenção e o tipo de página, mas **nunca inventa** sortimento, marca, filtro ou "mais vendido".

## Como funciona (por baixo)

**1. Descobre o tipo de página — a estrutura muda com ele.**
- **Hub de categoria** — navegação; o conteúdo primário são as **subcategorias e links**, não texto longo.
- **PLP (listagem)** — comparar/refinar; intro curta + um "como escolher" opcional, sem bloquear o grid.
- **Coleção** — tema editorial/sazonal; narrativa curta que reflete o sortimento real.
- **Página de marca** — as linhas/categorias daquela marca; sem inventar história ou claim.
- **Facet landing** — combinação específica de atributos; H1 específico + orientação curta.

**2. Pergunta a intenção antes da keyword.** "O que a pessoa espera fazer aqui?" Não transforma toda categoria em artigo. A keyword é inferida da categoria/H1/URL/catálogo (explícita é um sinal a mais, não requisito) e usada com naturalidade — **sem contar repetições**.

**3. Ancora no catálogo real (catalog grounding).** Antes de afirmar qualquer coisa, olha os produtos, marcas, faixas de preço, materiais, usos e subcategorias que existem de verdade. Nunca inventa "os mais vendidos", "todas as marcas", filtros ou público que não estão lá.

**4. Decide se vale a pena ter texto (Content Worthiness).** Se há variedade real, subcategorias, filtros decisivos e orientação legítima, o conteúdo se justifica e ganha profundidade (mínima → curta → média → profunda, conforme a complexidade da decisão). Se não há, recomenda **intro mínima ou nenhum texto longo** — em vez de encher linguiça.

**5. Coloca o conteúdo no lugar certo.** Numa PLP: H1 → intro curta → (chooser) → **grid de produtos** → conteúdo complementar depois. Nunca uma parede de texto antes dos produtos. Quando um "Para X, escolha Y" resolve melhor que um parágrafo, usa **bullets de escolha rápida** — a saída não precisa ser texto corrido.

**6. Sugere links internos reais.** Subcategorias, marcas, guias e categorias relacionadas, com âncoras descritivas (nada de "clique aqui"). Com acesso ao site, descobre os links reais; **sem o site, sugere o destino conceitual e a âncora — nunca inventa um slug/URL**.

**7. Levanta alertas técnicos, mas não mexe na infra.** Em auditoria, sinaliza risco de facetas gerando URLs quase infinitas, duplicação, canibalização entre categorias parecidas, paginação não rastreável e conteúdo sazonal vencido. **Alerta** — não prescreve canonical/noindex universal nem configura nada (isso é decisão de quem cuida do SEO técnico).

## Instruções (o cérebro da skill)
1. Identifique o **modo** (criar / otimizar / auditar / lote) e o **tipo de página**.
2. Determine a **intenção** e faça o **catalog grounding** (o que existe de verdade).
3. Passe pelo **Content Worthiness**: decide se merece texto e qual profundidade.
4. Monte só os **blocos recomendados** para aquele tipo (intro, chooser, complemento, links), na posição certa.
5. Use o termo principal e variações com naturalidade; **sem contar keyword nem forçar tamanho**.
6. Rode o **Quality Gate** e corte o que for filler.
7. Entregue os blocos prontos — se só uma intro curta bastava, entregue só ela.

**Estruturas por tipo (referência, não fôrma):**
- Hub → H1 + intro + subcategorias/links.
- PLP → H1 + intro curta + (chooser) + grid + complemento.
- Coleção → intro temática curta + contexto real.
- Marca → intro factual + categorias/linhas.
- Facet landing → H1 específico + intro curta + orientação + links.

## Regras de qualidade
- **Nunca invente** marca, produto, preço, faixa, material, filtro, subcategoria, popularidade, estoque, benefício, certificação, uso recomendado, promoção ou sazonalidade.
- **Sem regra rígida de tamanho nem de densidade**: profundidade vem da utilidade. Não force 80–150 palavras nem "keyword X vezes" (isso não é regra do Google).
- **"Mais vendidos", "favoritos", "mais procurados"** só com dado real.
- **Sem template genérico**: fuja de "Aqui você encontra [categoria]". Diferencie pelo sortimento, intenção, filtros, subcategorias e decisão reais.
- **Categoria não é blog**: priorize conteúdo que ajuda a comprar; história genérica da categoria pertence a um guia/artigo, não à PLP.
- **Guidance sensível** (saúde, biomecânica/esporte, suplemento, beleza, infantil, segurança, compatibilidade): só oriente "qual atributo serve para quem" com base segura — nada de extrapolação médica ou biomecânica.
- **Não invente URL**: sem o site, sugira destino + âncora conceitual, não um slug.
- **Em lote, nunca template × milhares de páginas**: classifique cada uma antes (hub / PLP / facet / técnica) e gere só onde há valor — conteúdo em escala sem valor adicional é penalizado.

### Quality Gate (silencioso, antes de entregar)
A pergunta central: **se eu removesse este texto, o comprador perderia alguma ajuda real?** — e: ajuda a navegar/escolher? · reduz incerteza? · é específico e factual? · reflete o catálogo? · está no lugar certo (não compete com o grid)? · não parece template? · a intenção casa com o tipo de página? · H1/title batem com o conteúdo? · sem stuffing? · sem canibalizar outra categoria? — o que falhar, corte.

## Formato da saída
Por padrão, **só os blocos recomendados** para aquela página — que podem ser: texto acima dos produtos, um "como escolher"/chooser, texto complementar e links internos úteis. Se só uma intro curta for necessária, entrega só ela. Nada de relatório, score ou contagem de palavras.

Sob pedido (ou em auditoria/lote): H1, SEO title, meta description, sugestão de links internos e labels de subcategoria, quick chooser, alertas técnicos (facetas, canibalização, paginação, sazonal), o relatório de auditoria priorizado, oportunidades de facet landing, ou a classificação em lote (que tipo é cada página e se merece texto).

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
