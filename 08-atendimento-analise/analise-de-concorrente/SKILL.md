---
name: analise-de-concorrente
description: Analisa concorrentes de e-commerce para apoiar uma decisão concreta (preço, sortimento, posicionamento, mídia, experiência ou entrada em categoria) com evidência rastreável — fonte, data, mercado e produto equivalente — separando fato de leitura, normalizando preço (mesma variante, por unidade, à vista × parcelado, com ou sem frete) e marcando o que não foi observado em vez de supor. Não inventa venda, tráfego, faturamento, orçamento de anúncio nem causa, não copia nem difama, e transforma as diferenças em hipóteses testáveis na própria loja. Use para descobrir, comparar, auditar, monitorar ou montar o plano de ação a partir de concorrentes.
---

# Análise de Concorrente

## O que faz
Começa pela **decisão** que o lojista precisa tomar e analisa os concorrentes certos para ela — com cada fato **rastreável** (fonte, data, região, produto) e cada interpretação **rotulada como interpretação**. Compara só o que é comparável (mesmo produto e variante, mesma unidade, mesmas condições), mostra onde estão as diferenças e as lacunas, e devolve poucas ações proporcionais à evidência — de preferência como **hipóteses para testar na própria loja**.

Regra de ouro: **a análise só afirma o que pode mostrar de onde veio.** Sem venda, tráfego, faturamento, orçamento de anúncio ou ROAS inventados; o que não foi observado fica como "não observado", não como "não existe". E a análise é interna, para decidir — nunca para copiar ou difamar.

## Quando usar
- Antes de decidir preço, sortimento, posicionamento, mídia ou entrada numa categoria.
- Mapear quem são os concorrentes de verdade numa categoria ou região.
- Comparar preço e condições de produtos equivalentes.
- Auditar uma análise feita antes, ou montar uma rotina de monitoramento.

## O que a IA precisa de você
- `[decisão]` — o que você quer decidir com a análise.
- `[sua loja]` — o que vende, para quem, onde entrega; e, se a decisão for de preço, seus custos e margem.
- `[concorrentes]` — nomes e links que você já conhece (a skill pode sugerir outros, se puder pesquisar).
- `[o que você observou]` — preços, frete, produtos, textos, anúncios, avaliações — **com a data** em que viu e, para frete, o CEP usado.
- `[mercado]` — país, região, moeda, canal (loja própria, marketplace).

A skill diz em que **modo** está: com pesquisa na web (quando tem acesso) ou só com o material que você trouxe — e as limitações de cada um.

## Como funciona (por baixo)

**1. A decisão define a análise.** Preço, sortimento, posicionamento, mídia, experiência ou entrada em mercado pedem análises diferentes, e a recomendação é **proporcional à evidência**. Escopo registrado: país, região, moeda, canal, categoria, público e período — mercados diferentes não se comparam sem normalizar.

**2. Quem é concorrente — e se é quem parece.** Direto, indireto, marketplace, marca fabricante e substituto funcional são coisas diferentes e ficam sinalizados. A descoberta parte de buscas por categoria, problema, marca e região (não só dos nomes conhecidos), registradas com data. Antes de incluir uma empresa: domínio, operação ativa, categoria e região conferidos — cuidado com homônimos e sites falsos. Amostra de **3 a 7** concorrentes conforme a decisão (o líder, um equivalente, uma alternativa) — **amostra não é o mercado inteiro**.

**3. Evidência rastreável.** Fontes primárias (página do produto, políticas, anúncios públicos, canais oficiais) para afirmar algo sobre a empresa; secundárias (avaliações independentes, estudos) para contexto — relato individual não é padrão. Cada fato relevante com **link, data e hora, região** e, quando preciso, o trecho visto. Estados: **verificado**, **inferido**, **desconhecido**, **desatualizado** ou **em conflito** — hipótese nunca vira dado, e fontes que divergem ficam em conflito, com prioridade para a fonte primária mais recente. Preço, estoque, frete, campanha e anúncio mudam rápido: toda observação tem validade. **Acesso ético**: respeitar termos e limites técnicos; não contornar login, paywall ou CAPTCHA; não coletar dado pessoal.

**4. Preço comparável.**
- **Mesmo produto**: mesma marca, modelo, GTIN e variante quando possível; senão, equivalência funcional com os critérios ditos.
- **Mesma variante**: tamanho, cor, capacidade, voltagem, kit e quantidade iguais antes de comparar.
- **Mesma unidade**: preço por unidade, kg, litro ou dose quando faz sentido, com a conta mostrada.
- **Mesmo tipo de preço**: cheio, promocional, à vista/Pix, parcelado e preço de assinante não se misturam.
- **Custo total para o comprador**: produto + frete + taxas, para um CEP e um cenário definidos — **sem frete conhecido, sem total inventado**.
- **Disponibilidade e condições**: estoque observável e prazo informado (botão "comprar" não prova estoque); parcelamento, retirada, troca, devolução e garantia com evidência.
- **Histórico**: uma captura é um ponto; **tendência** pede várias observações datadas.
- **Marketplace**: preço e condições do vendedor ≠ do marketplace ≠ do fabricante; conferir o vendedor e a variante.

**5. Sortimento e posicionamento.** Amplitude e profundidade **da amostra observada** — sem afirmar o catálogo inteiro sem varredura. Lacuna só com evidência suficiente: **não encontrar um produto numa busca não prova que a loja não tem**. Posicionamento **declarado** (promessa, tom, diferenciais, com citação curta e fonte) separado do **percebido** (público e faixa de valor inferidos — rotulado como interpretação). Avaliações, selos e números que o concorrente divulga são **dele**, não auditados.

**6. Experiência.** Página de produto com a mesma rubrica para todos (informação de decisão, fotos, medidas, prova, clareza da oferta). Celular só se houve visualização real — senão, **não avaliado**. Checkout só nas etapas públicas ou no material fornecido — **sem concluir compra nem usar dado de pagamento real**. Velocidade com ferramenta apropriada (PageSpeed, dados de campo do Chrome), diferenciando campo e laboratório. Políticas e confiança conferidas (selo visual ≠ certificação). Jornada (descoberta → produto → carrinho → checkout → pós-compra) com evidência, sem simular pedido.

**7. Marketing observável — e seus limites.** SEO visível (títulos, categorias, conteúdo, links internos, snippets) — a posição na busca varia por local e dispositivo; volume, tráfego e backlinks de ferramentas são **estimativas**, não o analytics do concorrente. Intenção de busca e quais páginas atendem melhor. **Anúncios** nas bibliotecas oficiais (Biblioteca de Anúncios da Meta, Central de Transparência de Anúncios do Google) — **anúncio visível não revela orçamento, ROAS nem vendas**. Criativos e ofertas catalogados com data e link, sem copiar criação distintiva. Redes sociais: frequência, temas e interações públicas — sem inferir conversão ou receita. **Avaliações e reclamações como sinal**: por tema, volume e recência, com viés de seleção reconhecido; poucos relatos não viram regra — verificar se é recorrente e se houve resposta.

**8. Da diferença à ação.** O **mapa de oportunidades** cruza a necessidade do cliente, a lacuna observada e a **capacidade real da sua loja**. Recomendar **princípios transferíveis**, nunca reproduzir texto, identidade visual, layout ou imagens de outra empresa. Prioridade por **impacto potencial × confiança da evidência × viabilidade**, com critérios ditos — sem ganho inventado. Mudança de preço ou frete passa pela **sua** margem e operação (sem dados, cenários — `precificacao`). Riscos de execução: estoque, plataforma, logística, equipe, jurídico, orçamento. Cada oportunidade vira **hipótese testável** (intervenção, métrica principal, proteção, janela) — porque **comparar sites não prova causa**: "ele vende mais porque tem frete grátis" é palpite; o teste na sua loja é que responde. Métrica conforme o objetivo (conversão, margem, receita por sessão, devolução, custo de aquisição) — não só preço.

**9. Monitoramento.** Rechecar preço, sortimento, campanhas e políticas com frequência proporcional à volatilidade. Comparar observações com data, mesma variante e mesmo CEP; **avisar só de mudança confirmada**.

## Instruções (o cérebro da skill)
1. Identifique o **modo** (descobrir / comparar / preço / sortimento / posicionamento / SEO / anúncios / experiência / auditar / monitorar / plano de ação) e se há acesso à web — declare as limitações.
2. Fixe a **decisão** e o **escopo**; escolha a amostra e verifique a identidade dos concorrentes.
3. Colete e registre a evidência com o **Competitive Evidence Lock**: fonte, data, mercado, produto/variante, tipo de evidência e confiança.
4. **Normalize** antes de comparar (produto, variante, unidade, tipo de preço, frete).
5. Separe **fato, leitura e desconhecido**; monte o mapa de oportunidades com a capacidade real da loja.
6. Priorize, transforme em **hipóteses testáveis**, rode o **Quality Gate** e entregue.

## Regras de qualidade
- **Decisão primeiro**; recomendação proporcional à evidência.
- **Fonte e data** em todo fato; inferência rotulada; conflito preservado.
- **Nada inventado**: venda, tráfego, faturamento, orçamento de mídia, ROAS, estoque real, causa.
- **"Não observado" ≠ "não existe"**; amostra ≠ mercado inteiro.
- **Comparação só entre equivalentes**, normalizada (variante, unidade, tipo de preço, frete).
- **Acesso ético**; sem compra simulada, sem dado pessoal, sem contornar barreiras.
- **Anúncio, rede social e ferramenta de SEO** com os limites ditos.
- **Avaliação e reclamação como sinal**, sem generalizar de poucos casos.
- **Princípio transferível, nunca cópia**; nunca difamação; nada ilegal.
- **Margem e operação da própria loja** antes de mexer em preço ou frete.
- **Hipótese testável** na própria loja; comparação entre sites não prova causa.
- **Saída simples para o lojista**; evidência detalhada sob demanda.
- **Print que a IA não vê não vira dado**: sem ver, pede os números digitados, com data.
- **Toda conta por código; alerta sem número novo**: com código disponível, nenhuma conta ou contagem de cabeça — nem nos alertas. Alerta e observação só repetem números já calculados (nos testes, a IA acertava a conta principal e errava os números "de passagem").

### Competitive Quality Gate (silencioso — bloqueia)
Todo fato tem fonte e data? · Alguma hipótese escrita como fato? · Algum número de venda, tráfego ou orçamento inventado? · Os produtos comparados são equivalentes e normalizados? · Preço desatualizado tratado como atual? · Total com frete inventado? · Ausência tratada como prova? · Causa inventada ("vende mais porque...")? · Recomendação de cópia ou difamação? · Acesso fora dos termos? · Margem própria considerada? · Ações proporcionais à evidência? — se falhar, corrija.

## Formato da saída
**Modo simples (padrão):** resumo curto ligado à decisão · **matriz** com fatos (fonte e data), diferenças, oportunidades e **lacunas de evidência** · **3 ações** priorizadas (como hipóteses, com o que medir).

**Modo avançado (sob pedido):** registro completo de evidências, critérios e notas de priorização, hipóteses com métrica e proteção, responsáveis, riscos de execução e plano de monitoramento.

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
