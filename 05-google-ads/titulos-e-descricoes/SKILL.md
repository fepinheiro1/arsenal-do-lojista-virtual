---
name: titulos-e-descricoes
description: Monta o conjunto de títulos (até 30 caracteres) e descrições (até 90) de um anúncio responsivo da Rede de Pesquisa do Google como um portfólio de mensagens combináveis — cada asset com uma função diferente, coerente com a intenção de busca e com a página de destino, contagem exata de caracteres e nenhuma alegação que o lojista não confirmou. Não preenche 15 títulos só para ocupar espaço, não fixa (pin) por padrão e separa o que o anunciante escreve do que o Google gera sozinho. Aceita produto/oferta, palavra-chave e grupo, página de destino e diferenciais reais. Use para criar, otimizar, auditar, testar ou gerar em lote anúncios de Search.
---

# Títulos e Descrições (Rede de Pesquisa)

## O que faz
Escreve o texto de um anúncio responsivo de Pesquisa (RSA) entendendo o que ele é de verdade: **um conjunto de peças que o Google combina sozinho**, em ordens diferentes, para cada busca. Por isso a skill não escreve "um anúncio" — monta um **portfólio de mensagens distintas e combináveis**, cada uma com uma função (relevância para a busca, benefício, diferencial, prova, oferta, marca, chamada à ação), todas verdadeiras e coerentes com a página para onde o clique vai.

Regra de ouro: **não gerar 15 títulos só para preencher 15 espaços.** Gerar as mensagens verdadeiras, distintas e combináveis que o produto sustenta — e dizer quais informações destravariam mais. A voz é da marca do lojista.

## Quando usar
- Criar o anúncio de um grupo de anúncios novo (produto, categoria, marca ou promoção real).
- Otimizar ou auditar um anúncio que já roda (repetição, claims sem base, pinning, coerência com a página).
- Propor uma variação de teste com hipótese, adaptar para outro mercado, ou gerar para vários grupos de uma vez.

## O que a IA precisa de você
- `[produto ou oferta]` — o que está sendo anunciado, com os fatos reais (características, preço, condições).
- `[palavra-chave / grupo de anúncios]` — o termo principal e o tema do grupo (ajuda a ler a intenção de busca).
- `[página de destino]` — a URL final. Sem acesso a ela, a skill marca pendências de conferência em vez de afirmar que conferiu.
- `[diferenciais reais]` — frete, troca, garantia, parcelamento, prova (avaliações, prêmios) — **só o que existe e está na página**.
- `[marca e tom]` — como a loja fala.
- (opcional) se a campanha usa **AI Max / personalização de texto / assets automáticos**, se há algo que **precisa** aparecer sempre (aviso legal, marca), e dados de desempenho dos assets atuais.

## Como funciona (por baixo)

**1. RSA é um sistema de peças, não uma frase.** O Google mistura títulos e descrições em ordens que você não controla. Então **cada asset precisa fazer sentido sozinho e com qualquer outro**: não depende da frase anterior, não contradiz o vizinho. Antes de entregar, a skill testa as combinações mais prováveis (título 1 + 2, 1 + 3, 2 + 3, e as descrições) procurando repetição e conflito de sentido.

**2. Diversidade de função, não de sinônimo.** "Tênis de Corrida", "Tênis para Corrida" e "Compre Tênis de Corrida" não são três títulos — é um título repetido (e o Google restringe repetição). Cada título recebe uma **função**: busca/palavra-chave, produto/categoria, benefício, diferencial, prova, oferta, marca, chamada à ação, confiança, caso de uso. As descrições expandem o benefício, explicam o diferencial, detalham a oferta, respondem a uma objeção, trazem prova ou orientam a ação — sem repetir os títulos em 90 caracteres. Hoje o próprio Google cita algo como **8 a 10 títulos com pelo menos 5 realmente distintos** como boa prática — heurística vigente, não regra eterna. Se o produto só sustenta 9 títulos honestos, entrega 9.

**3. Intenção de busca primeiro.** Quem busca por categoria, por um produto específico, comparando, atrás de preço/promoção, pela marca ou por uma solução quer ouvir coisas diferentes — o mesmo conjunto não serve a todos. A palavra-chave entra **naturalmente em alguns títulos**, não em todos. Se a expressão não cabe em 30 caracteres, a skill não mutila o português: usa uma variante natural ou leva o contexto para a descrição. Se o grupo mistura intenções muito diferentes, o problema é da estrutura — a skill sinaliza e encaminha para `estrutura-de-campanha` / `pesquisa-de-palavras-chave`.

**4. O anúncio só promete o que a página entrega.** Produto, categoria, preço, oferta, frete, estoque, variante e CTA precisam bater com a página de destino. Anunciar categoria que não existe, oferta que não aparece ou produto indisponível é deturpação. Sem acesso à página, a skill **não afirma que conferiu**: lista o que conferir. Se a página contradiz a copy, a recomendação é **não publicar** até corrigir.

**5. Nenhuma alegação que o lojista não confirmou.** Marca, característica, material, compatibilidade, benefício, estoque, ranking, preço, desconto, parcelamento, frete, validade, "mais vendido", "nº 1", nota, prêmio, certificação, "oficial", parceria — tudo isso só entra se foi informado e está sustentado. O que falta vira `[preencher]` ou pendência, nunca invenção. Mencionar marca de terceiros (revenda) não autoriza sugerir afiliação ou produto oficial. Categorias sensíveis (saúde, suplemento, finanças, adulto, jogos, política) recebem alerta: aprovação do anúncio não é presumida — conferir a política do país, da conta e do produto.

**6. Contagem exata e regras editoriais.** Limites vigentes do RSA: **até 15 títulos de 30 caracteres, até 4 descrições de 90, 2 caminhos de 15** (conferir no Google Ads, que muda). A contagem é **exata, com espaços e acentos** — se houver como executar código, contar com código, porque contagem de cabeça erra. Linha que estoura é **reescrita**, nunca cortada. Sem CAIXA ALTA como chamariz (só marca/código legítimos), sem `!!!`, símbolos decorativos, letra trocada por número, emoji. Português correto vale mais que encaixar 30 caracteres.

**7. Pinning é exceção.** Fixar um título numa posição reduz as combinações que o Google pode testar. A skill **não fixa por padrão** — só quando há motivo real (aviso legal obrigatório, regra de marca, teste específico). Mesmo assim, prefere fixar **2 ou 3 versões diferentes** na mesma posição e deixar o resto livre, e confere se o fixo combina com todos os livres. CTA também varia: nem todo título precisa ser "Compre Agora" — "Veja os Modelos", "Compare", "Confira", "Encontre" servem a intenções diferentes.

**8. O que você escreve × o que o Google gera.** Com **AI Max / personalização de texto / assets automáticos** ligados, o Google pode criar ou adaptar textos a partir da página e dos seus assets — o anúncio exibido pode não ser nenhuma combinação que você escreveu. A skill pergunta (ou marca como "conferir no Google Ads") se isso está ativo, separa os assets do anunciante dos gerados e lembra de revisar o que a plataforma pode produzir. Os nomes e a disponibilidade desses recursos mudam — conferir a documentação vigente. **Inserção dinâmica de palavra-chave, de localização e customizadores** (preço, promoção, estoque) só entram com sintaxe validada na conta, texto padrão (fallback) e concordância em português — nunca com sintaxe inventada, e localização só se a loja realmente entrega ali.

**9. Caminhos, complementos e o que o Ad Strength não diz.** Os caminhos de exibição são **sinais de contexto**, não URLs reais — a URL final é outro campo, obrigatório. Sitelinks, frases de destaque, snippets estruturados, preço e promoção são **assets complementares**, separados dos 15/4 — a skill pode sugerir, sem misturar. **Ad Strength** ("Bom", "Excelente") mede variedade e cobertura, não ROAS: buscar uma nota boa sem sacrificar verdade nem clareza.

**10. Medir e testar sem enganar a si mesmo.** Relatórios de desempenho por asset e por combinação ajudam, mas cada asset aparece em contextos diferentes — não dá para dar a vitória a um título isolado com base em número agregado, nem dizer que o Google testou todas as combinações. Teste bom tem **hipótese** (preço × benefício, prova × conveniência), **uma variável principal**, período e métrica definidos antes. E a copy não se otimiza só por CTR quando o objetivo é venda lucrativa: depende de conversão bem medida (CVR, CPA, ROAS, margem quando houver).

## Instruções (o cérebro da skill)
1. Identifique o **modo** (criar / otimizar / auditar / variação de teste / adaptar mercado / lote) e fixe o **RSA Truth Lock**: marca, produto, preço/oferta (confirmados ou ausentes), prova (só verificada), intenção de busca, página de destino (fornecida ou pendente), mercado/idioma, categoria de política (checada ou pendente), AI Max/personalização (ligada, desligada ou desconhecida), necessidade de pin (explícita ou nenhuma).
2. Leia a **intenção** do grupo e a **página de destino**; se o grupo mistura intenções, sinalize e encaminhe.
3. Monte a **arquitetura de mensagens**: liste as funções que os fatos reais sustentam e escreva **um asset por função/ângulo** — títulos, descrições e caminhos.
4. **Conte os caracteres de forma exata** (com código, se possível) e reescreva o que estourar. Passe pelos gates de **pinning, inserção dinâmica/customizadores e automação**.
5. Rode o **teste de combinações** e o **Quality & Policy Gate**. Falha crítica (claim sem base, página que contradiz, categoria sensível sem alerta) → corrija ou recomende não publicar.
6. Entregue os assets, as pendências e — separado da copy — as recomendações de pinning, automação, complementos e teste.

Em **otimizar/auditar**: preserve os assets que comprovadamente funcionam (com dado) em vez de reescrever tudo. Em **lote**: cada grupo tem contexto próprio (intenção, página, oferta) — sem clones entre grupos; exportação para Google Ads Editor/API só com colunas verificadas, nunca inventadas.

## Regras de qualidade
- **Portfólio, não preenchimento**: cada asset com função distinta; menos títulos honestos > 15 com repetição ou invenção.
- **Combinável**: todo asset faz sentido sozinho e com qualquer outro; sem contradição nem repetição semântica.
- **Intenção certa**: palavra-chave natural em parte dos títulos; conjunto diferente para intenção diferente.
- **Verdade**: marca, produto, oferta, preço, frete, estoque e prova reais; o que falta vira `[preencher]`; terceiros sem sugerir parceria.
- **Página de destino** coerente com o anúncio; sem acesso, pendência — nunca "auditei".
- **Limites exatos** (30/90/15, conferir vigentes); reescrever, nunca cortar; editorial limpo (sem caixa alta, `!!!`, emoji).
- **Pinning só com motivo**; inserção dinâmica e customizadores só com sintaxe validada e fallback.
- **Automação identificada**: o que é seu × o que o Google gera.
- **Persuasão ética** (a mesma do Arsenal): sem "melhor do mundo", "imperdível", "última chance", urgência ou escassez falsa, garantia de resultado.
- **Ad Strength não é meta de negócio**; teste com hipótese; sem prometer melhora de desempenho.
- **Voz da marca, não da Performa.** Saída simples para o lojista iniciante.

### RSA Quality & Policy Gate (silencioso)
Limites respeitados com contagem exata? · Gramática ok? · Diversidade real de função (não sinônimos)? · Combinações coerentes, sem repetição? · Bate com a intenção de busca? · Bate com a página de destino (ou pendência listada)? · Algum claim não confirmado? · Preço/estoque/oferta reais? · Marca própria e de terceiros sem parceria inventada? · Categoria sensível com alerta? · Pinning justificado? · Inserção dinâmica/customizador com fallback? · Automação do Google identificada? · Idioma e mercado certos? · Dados faltantes visíveis? · Teste sem promessa de resultado? — falha crítica: corrija ou bloqueie a publicação.

## Formato da saída
Três blocos — **Títulos (até 30)**, **Descrições (até 90)** e **Caminhos (até 15)** — cada linha numerada com a **contagem exata** entre parênteses e, quando ajudar, a função do asset (busca, benefício, diferencial, oferta, prova, marca, ação). Depois, curto: **pendências** (o que conferir na página, o que está `[preencher]`, que informação destravaria mais títulos) e, **separado da copy**, as recomendações de pinning, AI Max/automação e assets complementares — só se fizerem sentido.

Sob pedido: a auditoria de um conjunto existente, uma variação de teste com hipótese e métrica, a versão para outro mercado/idioma, ou a geração em lote por grupo. Nada de relatório por padrão.

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
