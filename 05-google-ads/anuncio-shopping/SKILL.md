---
name: anuncio-shopping
description: Cuida dos dados do produto no feed do Google Merchant Center (Shopping e o feed que alimenta o Performance Max): primeiro diagnostica se o problema é de texto, de atributo, de sincronização (preço/estoque), de imagem, de identificador ou de política; depois escreve título e descrição factuais, com a contagem exata e sem fórmula universal. Nunca inventa atributo, GTIN, MPN ou marca, preserva o ID e as variantes, e mantém pendências fora do texto publicável. Aceita o SKU, o feed atual, a página do produto, o país e, se houver, o relatório de diagnóstico. Use para criar, otimizar, auditar, diagnosticar, comparar ou processar em lote produtos do feed.
---

# Anúncio de Shopping (feed do Merchant Center)

## O que faz
No Shopping, **o anúncio é o dado do produto**: título, descrição, preço, estoque, imagem, marca, identificadores e variante saem do feed. Por isso a skill começa pelo diagnóstico — o problema é de **texto**, de **atributo faltando**, de **preço/estoque fora de sincronia**, de **imagem**, de **identificador** ou de **política**? — e só depois reescreve título e descrição, com o que está confirmado, na ordem que faz sentido para aquele tipo de produto.

Regra de ouro: **dados corretos antes de texto persuasivo.** O feed descreve fielmente o item ofertado; otimizar não autoriza inventar atributo, mudar a variante ou disfarçar um problema de elegibilidade. Copy boa não resolve produto reprovado.

## Quando usar
- Cadastrar produtos no Merchant Center ou melhorar título e descrição de quem já está lá (o modo padrão quando há dados do catálogo é **otimizar**).
- Entender por que um produto está reprovado, limitado ou aparecendo pouco.
- Auditar ou processar o catálogo em lote sem misturar dados de um SKU com outro.

## O que a IA precisa de você
- `[produto / SKU]` — ID do item, título e descrição atuais, link, imagem.
- `[atributos confirmados]` — marca (do fabricante), tipo, gênero/idade (se pertinentes), cor, tamanho e sistema de tamanho, material, modelo, condição, GTIN/MPN, se é kit ou multipack. **Da fonte oficial** (ERP/catálogo/ficha do fabricante), não de memória.
- `[país, idioma e moeda]` do feed — e o destino (anúncios, listagens gratuitas).
- `[página do produto]` — para conferir preço, estoque e variante.
- (opcional) `[relatório de diagnóstico do Merchant Center]`, regras de feed e fontes suplementares, dados de desempenho.

## Como funciona (por baixo)

**1. Diagnóstico antes da reescrita.** Cada problema ganha uma classe — **atributo faltando**, **valor inválido**, **feed × página divergente**, **política**, **imagem**, **identificador**, **baixa relevância** ou **indefinido** — porque cada um tem uma solução diferente, e só "baixa relevância" se resolve com texto. Cada achado diz se é **confirmado** (veio do relatório do Merchant Center), **suspeito** (inferido do catálogo) ou **não checado**. Sem o relatório, a skill entrega um checklist — e **nunca diz que consultou** o Merchant Center.

**2. Fonte da verdade e conflito.** Ordem de confiança: catálogo/ERP aprovado → página do produto → feed atual → documentação do fabricante. Quando duas fontes discordam (cor no feed ≠ cor na página), a skill **alerta** — não escolhe em silêncio. Cada atributo carrega valor, fonte e status: confirmado, faltando ou em conflito.

**3. Identidade intocável.** O **ID** do item é estável: não se cria ID novo para "testar título" (perde o histórico). **Marca** é a do fabricante — nome da loja só se a loja fabrica aquela linha; produto sem marca não ganha marca inventada. **GTIN nunca é fabricado** (nada de EAN "plausível" ou reaproveitado de outro SKU); MPN, SKU interno, GTIN e ID são coisas diferentes. Produto que realmente não tem identificador segue a regra vigente do Merchant Center para esse caso.

**4. Variante é variante.** Variantes genuínas se agrupam pelo `item_group_id`, mas cada uma mantém **ID próprio, cor, tamanho, imagem e link** — nada de colapsar SKUs diferentes num item só. Cor com o nome fiel (sem trocar por sinônimo para pegar busca). Tamanho com o sistema certo, sem converter BR/US/EU sem a tabela do fabricante. Gênero e faixa etária só quando pertinentes e sustentados (nunca inferidos pela foto). Material e estampa da especificação, não de adjetivo. Condição real (não marcar "novo" na dúvida). Kit e multipack têm significado próprio — não se deduzem pela imagem.

**5. Categoria certa, sem chutar código.** A **categoria do Google** (taxonomia deles) é diferente do **tipo de produto** (a hierarquia da loja). A skill não inventa código de taxonomia; na dúvida, sinaliza.

**6. Preço, estoque, página e imagem.** Preço (e preço promocional, se houver) igual ao da página e às regras da promoção; disponibilidade igual ao estoque **atual**. Divergência se corrige **na origem ou na integração** — nunca escondendo no título (preço no título é proibido de qualquer jeito). O link abre o produto **e a variante** certos, no celular também; a página permite comprar e mostra preço, moeda, entrega e devolução. Sem acesso à página, a skill não afirma que conferiu. Imagem representa exatamente o item e a variante, sem selo promocional nem marca-d'água — problema visual vai para as skills da frente `02-imagem`; texto não corrige imagem.

**7. Título informativo, sem fórmula universal.** Limite técnico de **150 caracteres** (especificação vigente — conferir), contado com código, com espaços. **Não existe ordem única** "Marca + Tipo + Atributos": em moda pesa gênero, cor e tamanho; em eletrônico, marca, modelo e capacidade; em marca própria pouco buscada, o tipo de produto costuma identificar melhor que a marca. O que identifica o produto vem **cedo**, porque a exibição corta — mas o trecho visível **varia por tela e dispositivo** (não existe "70 caracteres garantidos"). Sem preço, promoção, "frete grátis", chamada para ação, urgência, caixa alta, repetição ou claim não verificado; marca, modelo e variante necessários à identificação ficam. Toda mudança guarda **título original → sugerido → motivo**.

**8. Descrição factual.** Até **5.000 caracteres** na especificação geral — o que não significa encher. Texto específico, verificável e útil: o que é, para que serve (se confirmado), atributos, compatibilidade, o que vem na caixa. Benefício só quando comprovável; nada de resistência, desempenho, garantia, certificação ou resultado sem fonte. Sem oferta temporária, link promocional ou palavra-chave empilhada, e sem repetir o título sem acrescentar nada.

**9. Pendência nunca entra no feed.** `[preencher]` dentro de um título ou descrição publicável é proibido. O que falta vai num **campo separado de pendências**, e o item incompleto **sai da exportação** até ser resolvido.

**10. País, destino e política.** Requisitos mudam por país, idioma, tipo de produto e destino. Categorias com restrição ou proibição vão para **revisão de política** — a skill **não reescreve para contornar** restrição. Seguir uma regra editorial não garante aprovação: o Merchant Center aplica outras políticas.

**11. Feed não é asset de PMax, e dado bom não é garantia de mídia.** O mesmo feed alimenta Shopping e Performance Max, mas título e atributos do feed **não são** os textos do grupo de recursos (isso é com a `copy-performance-max`). Atributo completo ajuda a correspondência e a qualidade do anúncio, mas **não garante** impressão, CTR ou ROAS. Fontes suplementares e regras de feed podem completar ou transformar dados — atenção à precedência: uma regra pode sobrescrever a correção que você acabou de fazer.

**12. Lote, prioridade e teste.** Em lote, esquema fixo e **identidade isolada** — nenhum atributo vaza de um SKU para outro. Saída com antes/depois, mudanças, evidência e alertas (sem GTIN, conflito de variante, claim não verificado, preço divergente, imagem divergente, revisão de política, baixa confiança); item crítico fica fora da publicação automática. Validação de limites e campos em **100% dos itens**; revisão humana em amostra por categoria e em **todos** os casos de alto risco. Prioridade por impacto: primeiro quem está inelegível, quem gera receita e quem está incompleto — não volume de busca imaginado. Teste de título com grupos comparáveis, janela e sazonalidade registradas — um antes/depois isolado não prova causa.

## Instruções (o cérebro da skill)
1. Identifique o **modo** (criar / otimizar / auditar / diagnosticar / lote / comparar / exportar) e fixe o **Feed Truth Lock**: ID do produto (obrigatório), ID da variante, atributos só de fonte oficial, identidade imutável, marca/GTIN/MPN nunca inventados, preço/estoque só da fonte atual, claims com evidência, página que precisa bater, país/idioma/destino explícitos ou sinalizados.
2. **Diagnostique**: classifique cada problema e o grau de evidência; o que não é de texto recebe a ação certa (origem, integração, imagem, política).
3. Valide **atributos e variantes** (completude por categoria, conflitos entre fontes).
4. Escreva **título e descrição** com o que é confirmado, na ordem que faz sentido para a categoria; **conte com código**.
5. Rode os gates de **política, variante e página**; separe pendências do texto publicável.
6. Rode o **Quality Gate** e entregue no formato do modo.

## Regras de qualidade
- **Identidade preservada**: ID, SKU e variante corretos em texto, imagem e link.
- **Nada inventado**: atributo, GTIN, MPN, marca, oferta, claim. Conflito entre fontes vira alerta.
- **Preço e estoque** só da fonte atual; divergência corrigida na origem, nunca no título.
- **Título** dentro do limite (contado com código), informativo, sem promoção nem repetição, ordem por categoria; mudança rastreável.
- **Descrição** factual e verificável; benefício só comprovável.
- **Página** coerente ou pendência sinalizada; imagem certa (problema visual → frente 02).
- **Política** considerada, sem contornar restrição; regra editorial ≠ aprovação garantida.
- **Diagnóstico** não consultado nunca declarado como confirmado.
- **`[preencher]` nunca no texto publicável**; item incompleto fora da exportação.
- **Lote** com isolamento entre SKUs e explicação das mudanças.
- **Voz da marca, não da Performa** — e no feed, a voz é informativa, não promocional.

### Feed Quality Gate (silencioso)
ID e SKU preservados? · Variante certa em texto, imagem e link? · Algum atributo inventado? · GTIN/MPN fabricado? · Marca é do fabricante? · Limites validados com código? · Título sem repetição nem promoção? · Descrição informativa e verificável? · Oferta inventada? · Preço/estoque presumidos? · Página consistente (ou pendência)? · Política da categoria considerada? · Diagnóstico não consultado tratado como confirmado? · `[preencher]` dentro do texto publicável? · Lote sem vazamento entre SKUs? · Mudanças explicadas e bloqueios sinalizados? — se falhar, corrija.

## Formato da saída
**Modo simples (padrão):** título recomendado (com contagem), descrição recomendada (com contagem), **2 alternativas de título com a hipótese** de cada uma, os atributos usados (confirmados), as **pendências** num bloco separado e os alertas por severidade (**bloqueio / atenção / oportunidade**).

**Modo auditoria/diagnóstico:** `problema | evidência (confirmado/suspeito/não checado) | severidade | ação recomendada`.

**Modo lote:** `id | original | sugerido | mudanças | evidência | alertas | status de revisão` — itens críticos marcados fora da publicação. Exportação só em formato verificado da plataforma, sem afirmar que algo foi publicado.

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
