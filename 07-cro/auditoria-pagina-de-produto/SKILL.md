---
name: auditoria-pagina-de-produto
description: Audita uma página de produto com base em evidência — separando o que foi observado, o que é hipótese e o que não pôde ser verificado com o material recebido (texto, prints, URL, dados) — e devolve correções priorizadas por gravidade, alcance, confiança e esforço. Olha o celular primeiro, cobre identificação, mídia, preço/frete/estoque, variantes, botão e retorno do carrinho, conteúdo, prova, confiança, acessibilidade, velocidade e dados do funil; separa correção óbvia de teste e não promete aumento de venda nem inventa claim, estatística ou política. Use para auditar, fazer uma triagem rápida, comparar páginas ou reauditar depois das correções.
---

# Auditoria de Página de Produto

## O que faz
Examina a página de produto como uma auditoria de verdade: **registra o que viu, onde viu e com que grau de certeza** — e não dá "OK" para o que não teve como ver. Começa pelo contexto (produto, público, dispositivo, de onde vem o tráfego) e pelo celular; passa pelos componentes que pesam na decisão; usa os dados do funil quando existem; e entrega poucas correções que importam, separando **o defeito óbvio que se corrige já** da **mudança que merece teste**.

Regra de ouro: **a auditoria aponta evidência e hipótese — não promete aumento de venda, não inventa estatística, claim ou política, e nunca transforma suposição em defeito comprovado.** Ela também não reescreve a página: encaminha cada parte para a skill certa do Arsenal.

## Quando usar
- Um produto recebe visitas e converte pouco — ou antes de colocar anúncio numa página.
- Triagem rápida de uma página (no máximo 5 recomendações).
- Comparar duas páginas ou duas versões.
- Reauditar depois das correções (resolvido / parcial / pendente).

## O que a IA precisa de você
- `[a página]` — URL, **prints do celular e do computador**, o texto colado ou um relatório. A skill declara o que examinou: só com texto, layout e botão ficam **não verificados**.
- `[produto, público e categoria]` — e o preço, para entender a complexidade da compra.
- `[condições reais]` — preço, parcelamento, frete, prazo, troca. Sem elas, pendência.
- `[prova real]` — avaliações (nota, quantidade), depoimentos autorizados.
- (opcional) **dados**: funil por etapa (visualização, carrinho, checkout, compra), celular × computador, fonte de tráfego; **dúvidas do atendimento**; gravações de sessão consentidas; dados de velocidade de campo.

## Como funciona (por baixo)

**1. Escopo e o que foi de fato examinado.** Produto, mercado, dispositivo, fonte de tráfego e a ação de conversão definem a auditoria. A entrada pode ser URL, prints, texto ou relatório — e a skill **diz o que inspecionou**. Texto colado não mostra layout, botão, zoom nem velocidade: esses itens saem como **não verificado**, nunca como "OK".

**2. Registro de evidência.** Cada achado tem **status** (**observado**, **hipótese** ou **não verificado**), a **evidência** (o que se viu e onde), a gravidade, a hipótese de efeito e o dado que falta. Heurísticas reconhecidas de usabilidade e de UX de e-commerce servem para **diagnosticar**, não provam causa. Benchmark externo é referência de contexto — **nunca meta universal** — e a skill não cita estatística ("o motivo nº 1", "o que mais derruba") sem fonte.

**3. Contexto antes de comparar.** Categoria, faixa de preço, complexidade da compra, público e restrições mudam o que importa: o que é essencial numa página de colchão é diferente de uma de capinha de celular.

**4. Celular primeiro.** A experiência real no celular vem primeiro, sem ignorar o computador e outras telas.

**5. Os componentes da decisão.**
- **Identificação e promessa**: nome, marca, variante e o que é o item, claros (não só código interno). Benefícios e características só **confirmados** — inclusive nas sugestões da própria auditoria.
- **Mídia**: cobertura de ângulos, detalhe, escala, uso e embalagem quando relevantes; zoom que funciona sem prender a navegação; vídeo quando ele demonstra a função e reduz dúvida (não é obrigatório em toda categoria); troca de cor/tamanho atualiza a imagem, sem mostrar a variante errada.
- **Hierarquia e layout**: nome, imagem, preço, disponibilidade e ação **fáceis de encontrar** — não necessariamente todos sem rolar. No celular: quebras, cortes, barras fixas, elementos sobrepostos, espaço útil.
- **Preço, frete e estoque**: preço atual, desconto real, parcelas e condições inteligíveis e **iguais aos do carrinho**; consulta de frete e prazo fácil, sem inventar prazo e sem exigir CEP cedo quando dá para evitar; disponível, indisponível, pré-venda e reposição claros.
- **Variantes e medidas**: tamanho, cor e compatibilidade selecionáveis e sem ambiguidade. Tabela de medidas → `tabela-de-medidas`.
- **Botão e carrinho**: rótulo, contraste, posição e estados — sem cor ou texto universal. **Depois do clique**, a página diz o que aconteceu: sucesso, erro ou "escolha o tamanho" — sem adicionar em dobro por acidente. Botão fixo na rolagem pode ajudar em páginas longas no celular, mas se testa (pode cobrir conteúdo e atrapalhar acessibilidade).
- **Conteúdo**: benefícios, especificações e restrições distintos e escaneáveis; informação crítica da categoria (material, medidas, o que vem na caixa, cuidados, compatibilidade, instruções). Perguntas frequentes **só a partir de dúvidas reais** (atendimento, avaliações) → `faq-do-produto`.
- **Prova e confiança**: avaliações autênticas, com a distribuição de notas e acesso às críticas; "compra verificada" só se for real. Políticas, contato, pagamento e troca acessíveis; **selo só se verdadeiro** — informação real vale mais que selo decorativo. Nada de prova fabricada.
- **Acessibilidade**: contraste, rótulos, foco visível, teclado, nome dos botões, texto alternativo, mensagens de erro, tamanho do alvo de toque, diálogos (referência: WCAG 2.2).
- **Fricção e distração**: pop-ups, banners, cross-sell e mensagens disputando a decisão principal.

**6. Dados, quando existem — e a qualidade deles antes.** Eventos de visualização, seleção, carrinho, início de checkout e compra, conferidos na implementação. **Taxas por etapa com o denominador explícito** (carrinho ÷ visualizações, compra ÷ visualizações). Segmentar celular × computador, canal, produto, cliente novo × recorrente — só com amostra suficiente. Antes de apontar gargalo, auditar **qualidade dos dados**: evento duplicado, consentimento, bloqueadores, atribuição. E combinar com o qualitativo: gravações **consentidas**, pesquisa, atendimento, avaliações, testes com usuários — sem gravar dado pessoal nem fazer teste invasivo.

**7. Velocidade e técnica — medida, não chutada.** Core Web Vitals (LCP, INP, CLS) com **dados de campo** quando houver; **não se infere nota de velocidade por um print**. Imagens (dimensão, formato, compressão; carregamento adiado — mas não na imagem principal), scripts e widgets de terceiros e mudanças de layout: risco apontado, medição real pedida. Dados estruturados de produto (preço, estoque, avaliação) coerentes com a página — sem confundir SEO com conversão.

**8. Preço e confiança sem atalho.** Preço percebido depende de concorrência, valor, frete e contexto — **a auditoria não recomenda desconto** sem análise econômica. Insegurança observada (ex.: atendimento perguntando se a loja é confiável) é diferente de hipótese.

**9. Priorizar, corrigir e testar.** Cada recomendação tem gravidade, alcance (quanto do tráfego é afetado), confiança e esforço — com o critério declarado, sem precisão matemática falsa. **Defeito óbvio se corrige sem experimento** (botão coberto, preço divergente, variante errada); mudança de persuasão ou de arquitetura **se testa** quando há tráfego: `observação → mecanismo esperado → mudança → métrica principal → métricas de proteção`, com unidade de sorteio, exposição e análise definidas, sem um teste interferir no outro. Sem tráfego suficiente, nada de prometer significância; considerar sazonalidade e efeito novidade. Proteção: receita por visitante, devolução, margem, reclamações, acessibilidade. Depois de implantar: conferir regressão, analytics e velocidade, registrar o resultado e ter caminho de volta.

## Instruções (o cérebro da skill)
1. Identifique o **modo** (auditoria completa / triagem rápida / comparação / reauditoria) e declare **o que foi examinado** (texto, prints, URL, dados).
2. Fixe o **contexto** (produto, categoria, preço, público, dispositivo, tráfego, conversão).
3. Percorra os **componentes**, celular primeiro, registrando cada achado com status, evidência e local.
4. Se houver **dados**, confira a qualidade antes e leia as taxas por etapa com denominador explícito.
5. **Priorize** (gravidade × alcance × confiança × esforço) e separe **correção já** de **teste**.
6. Encaminhe o que é de outra skill, rode o **Quality Gate** e entregue.

Em **reauditoria**: marque cada achado anterior como resolvido, parcial ou pendente. Em **comparação**: mesmos critérios, com ressalvas de tráfego e contexto.

## Regras de qualidade
- **Observado × hipótese × não verificado** em cada achado; nada de "OK" sem ter visto.
- **Evidência e local** de cada achado; dado faltante dito.
- **Nada inventado**: claim (nem na sugestão de título), estatística, política, prazo, selo, funcionalidade da página.
- **Celular primeiro**; contexto da categoria antes de comparar.
- **Sem regra universal** (tudo sem rolar, cor do botão, vídeo obrigatório); heurística diagnostica, não prova.
- **Dados com qualidade conferida** e denominador explícito; velocidade medida, não inferida.
- **Sem recomendar desconto** sem análise econômica; selo só verdadeiro.
- **Correção óbvia ≠ teste**; teste com hipótese, proteção e honestidade sobre amostra.
- **Poucas recomendações que importam**, executáveis; confirmar o que já está bom.
- **Encaminhar** título, descrição, bullets, FAQ, medidas e imagens para as skills do Arsenal.
- **Sem promessa de aumento de venda.** Linguagem simples para o lojista.

### Product Page Audit Quality Gate (silencioso)
Declarou o que examinou? · Algum "OK" sem evidência? · Cada achado tem status, evidência e local? · Alguma estatística ou benchmark sem fonte? · A sugestão inventa claim? · Celular avaliado (ou não verificado)? · Dados com qualidade conferida? · Velocidade inferida de print? · Recomendou desconto ou selo sem base? · Correção óbvia separada de teste? · Teste com hipótese e proteção? · Recomendações executáveis e poucas? · Encaminhou às skills certas? · Prometeu resultado? — se falhar, corrija.

## Formato da saída
1. **O que foi examinado** (1 linha) e **resumo** em linguagem simples (a maior alavanca, com o grau de certeza).
2. **Achados**: `Componente | Status (observado / hipótese / não verificado) | Evidência e local | O que fazer`.
3. **Plano**: **corrigir já** (defeitos óbvios) e **testar** (com hipótese), cada item com impacto potencial, esforço e confiança.
4. **Dependências e pendências**: dados, medições e informações que faltam; o que vai para outras skills.

**Triagem rápida**: no máximo 5 recomendações. **Reauditoria**: resolvido / parcial / pendente.

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
