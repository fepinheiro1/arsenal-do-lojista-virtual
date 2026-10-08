---
name: estrutura-de-campanha
description: Desenha a arquitetura mínima viável de uma conta de Google Ads — quais campanhas (Pesquisa, Shopping, Performance Max), quais grupos, com que orçamento e que lance — a partir do objetivo econômico, do catálogo, da margem, da medição e do mercado. Verifica medição e economia antes de recomendar lance, só separa campanha quando há motivo de controle, trata orçamento e projeção como hipótese e audita a conta existente antes de reconstruir. Aceita catálogo, objetivo, orçamento, país/moeda, URLs e situação da conta. Use para criar, auditar, otimizar, migrar, expandir ou simular a estrutura.
---

# Estrutura de Campanha

## O que faz
Desenha o esqueleto da conta antes de qualquer anúncio: **quais campanhas existem, por quê, com quanto de verba, que tipo de lance e para onde cada grupo leva**. Mas começa antes da árvore: confirma o objetivo econômico (receita? lucro? clientes novos? girar estoque?), se a **medição** permite otimizar e se a **margem** sustenta a meta. Só então monta a **menor estrutura que resolve** — e explica o motivo de cada separação.

Regra de ouro: **estrutura organiza o investimento; ela não garante clique mais barato nem Índice de Qualidade maior.** Resultado depende de leilão, anúncio, página e concorrência. Por isso a skill entrega um plano com premissas visíveis, sem promessa de CPA ou ROAS, e nunca como se a conta já estivesse publicada.

## Quando usar
- Abrir uma conta nova (sobretudo com verba limitada).
- Decidir entre Pesquisa, Shopping e Performance Max para o catálogo.
- Auditar ou reorganizar uma conta que já roda — com plano de migração e volta atrás.
- Expandir depois de ter evidência, ou simular cenários de orçamento e viabilidade.

## O que a IA precisa de você
- `[objetivo]` — receita, lucro, clientes novos, girar estoque, proteger marca.
- `[catálogo]` — categorias, produtos principais, se há **feed no Merchant Center** e como está.
- `[orçamento]` — valor e moeda; `[país / idioma]` e onde a loja entrega de verdade.
- `[margem]` (opcional) — margem de contribuição (depois de custo, frete subsidiado, taxas, devoluções). Sem ela, nada de meta financeira como fato.
- `[medição]` — compra configurada como conversão, com valor? (GA4/Google Ads). Se não sabe, a skill marca como "não verificado".
- `[conta existente]` (se houver) — campanhas atuais, gasto, conversões, termos de pesquisa, histórico.
- `[URLs]` — as páginas de destino de cada tema.

Faltou dado? A skill **não trava num questionário longo**: monta um cenário provisório rotulado como tal e lista o que confirmar.

## Como funciona (por baixo)

**1. Objetivo econômico e medição vêm antes da árvore.** Receita, lucro de contribuição, cliente novo, estoque e marca pedem estruturas diferentes — e **ROAS alto não é lucro alto**. A medição é pré-requisito: a compra é a conversão **primária**, com valor e moeda certos, sem contar em dobro? Visualização, carrinho e início de checkout servem para diagnóstico, não para substituir a venda como objetivo. Se a base não permite otimizar com confiança, a skill **sinaliza o bloqueio** em vez de recomendar lance por valor como se estivesse pronto.

**2. Margem antes de meta.** Com a margem de contribuição informada, dá para calcular **como hipótese** o ROAS de equilíbrio: `1 ÷ margem disponível para mídia` (margem de 25% → ROAS 4 só para cobrir a mídia, antes de qualquer lucro). Sem margem, a skill **não calcula nem inventa** — deixa a fórmula para preencher. E não aplica a conta cegamente a lucro total ou valor de vida do cliente.

**3. Conta existente: auditar antes de reconstruir.** Antes de propor outra estrutura, olha campanhas, conversões, orçamento, termos de pesquisa, sobreposição e histórico. Reconstrução total sem benefício demonstrável destrói aprendizado e comparação histórica. Mudança grande vira **migração faseada**: ordem, janela de observação e critério de volta atrás.

**4. Tipo de campanha pela elegibilidade, não por moda.** Pesquisa, Shopping e Performance Max se escolhem por feed, intenção, controle desejado e qualidade da medição — nem toda loja precisa dos três. Pesquisa e Performance Max podem conviver; uma não "rouba" automaticamente da outra, e separar não elimina sobreposição (o Google tem regras próprias de qual campanha entra no leilão). **Shopping padrão × Performance Max** não tem vencedor universal: compara-se controle de inventário, criativos, relatórios, orçamento e maturidade da conta. **Campanha de marca** pode ser útil, mas não é presumida barata nem incremental — depende de concorrência na marca e do orgânico. **Termos de concorrentes**, só com página relevante e sem uso indevido de marca alheia.

**5. Arquitetura mínima viável — separar só com motivo.** **Campanha** guarda configuração e orçamento; **grupo** organiza tema, anúncio e página. Uma campanha nova só nasce quando há **motivo de controle**: orçamento ou meta diferente, outro país/idioma, inventário à parte, marca, restrição ou estratégia distinta. Um grupo reúne buscas que **podem dividir o mesmo anúncio e a mesma página** — não precisa uma palavra-chave por grupo, e se o anúncio e a página não mudam, o grupo não precisa existir. Campanha por produto só se demanda, margem e orçamento justificam. Separar por dispositivo ou horário, só com motivo e compatível com o lance. **Verba baixa → poucas campanhas** (microsegmentar divide os dados e o aprendizado).

**6. Palavras-chave, negativas e controles de cada tipo.** Correspondência ampla, de frase e exata funcionam por **significado e intenção**, não por igualdade literal — sintaxe não é controle absoluto. O relatório de termos de pesquisa refina a estrutura, com visibilidade limitada por privacidade. **Negativa é faca de dois gumes**: pode bloquear tráfego bom ("grátis" negativado derruba "tênis frete grátis"); conferir antes de listas globais. E cada tipo de campanha tem **controles próprios**: negativas de Pesquisa ≠ exclusões de marca ≠ controles do Performance Max — e esses controles vêm mudando. A skill **não supõe** que um controle existe (ou não existe) em todo tipo: monta a matriz de exclusões por campanha e marca "conferir na conta" quando não tem certeza.

**7. Feed e inventário (Shopping / Performance Max).** Merchant Center sem pendências, itens aprovados, disponibilidade, identificadores e preço iguais aos da página. **Não promover o catálogo inteiro por padrão**: produto sem estoque, de margem baixa ou restrito fica de fora. Grupos de produtos por categoria e por **rótulos personalizados** (margem, sazonalidade, estoque, mais vendido comprovado) — sempre com a origem do dado, nunca classificação inventada. Grupo sem volume não se separa.

**8. Orçamento e lance como hipótese.** Concentrar verba quando o volume é baixo; documentar orçamento por campanha só quando ela tem motivo próprio. **Orçamento diário é média, não teto**: o Google pode gastar mais num dia e compensar no mês (regra vigente de gasto e cobrança — conferir). Lance pelo objetivo e pela qualidade do dado: **Maximizar conversões** ou **Maximizar valor da conversão**, com meta de CPA ou ROAS opcional e só com volume e valor confiáveis — nada de ROAS desejado "porque é e-commerce". Mudanças simultâneas em orçamento, meta, conversão e segmentação atrapalham a estabilização (sem prazo fixo garantido). **Projeção sem dado é invenção**: sem CPC, conversão, ticket e histórico confiáveis, a skill entrega cenário com premissas visíveis — ou diz que não há base.

**9. Mercado, página e política.** Localização conforme onde a loja **entrega de verdade** (a opção de "presença ou interesse" amplia alcance — decidir conscientemente); idioma é o de quem busca, não o da interface; vários países só se separam quando moeda, logística ou catálogo mudam — nada de duplicar por cidade sem motivo. Cada grupo aponta para uma página que cumpre a promessa (produto disponível, preço certo, celular, velocidade) — **sem acesso à página, a skill não afirma que conferiu**. Categorias restritas, alegações, marcas e Merchant Center viram `VALIDAR POLÍTICA`, sem prometer aprovação.

**10. Do plano à conta, e da conta ao diagnóstico.** "Plano pronto" ≠ "conta pronta para publicar": antes do lançamento, checklist de acesso à conta, conversões/GA4, Merchant Center, domínio, páginas, anúncios, pagamento e consentimento. Depois, diagnóstico **por etapa do funil** — elegibilidade/impressão, relevância/CTR, custo, página, conversão, valor — sem culpar a estrutura por todo CPA alto. Teste de estrutura tem hipótese; prefira os experimentos oficiais do Google a comparar períodos (sazonalidade e leilão mudam). Expansão só com evidência — **catálogo grande não é motivo para criar campanha por produto**.

## Instruções (o cérebro da skill)
1. Identifique o **modo** (criar / auditar / otimizar / migrar / expandir / simular / exportar) e fixe o **Campaign Architecture Truth Lock**: objetivo (confirmado ou pendente), país e moeda, orçamento (informado ou hipótese), catálogo/inventário (fonte e data), margem (fonte ou ausente), medição (verificada ou não), páginas (verificadas ou não), tipos de campanha (elegibilidade a validar), controles da plataforma (conferir vigentes), histórico (fonte e período), riscos de política. **Separe sempre fato, premissa e decisão proposta.**
2. Passe pelo **gate de medição e economia**: o que dá para otimizar com a medição atual? Há margem para meta?
3. Escolha os **tipos de campanha** elegíveis e monte a **arquitetura mínima viável** — cada campanha com motivo, cada grupo com intenção e página.
4. Proponha **orçamento e lance como hipótese**, a matriz de **negativas/exclusões por tipo** (sem bloqueio acidental) e, com feed, a organização do inventário.
5. Rode o **gate de política e dependências** e, em conta existente, o **plano de migração** com volta atrás.
6. Rode o **Quality Gate** e entregue a árvore, as justificativas e os próximos passos.

## Regras de qualidade
- **Objetivo econômico explícito**; ROAS ≠ lucro.
- **Medição e margem antes de lance e meta**; sem margem, sem ROAS de equilíbrio como fato; sem medição, sem lance por valor "pronto".
- **Estrutura compatível com a verba**: cada campanha com motivo próprio, cada grupo com intenção e página coerentes; verba baixa não vira dez campanhas.
- **Tipos elegíveis** e controles de cada tipo sem extrapolação; negativas sem bloqueio acidental; sobreposição não é canibalização automática.
- **Feed e estoque** verificados ou marcados pendentes; catálogo inteiro não é default.
- **Nada inventado**: margem, CPC, taxa de conversão, projeção, rótulo de produto, regra de política.
- **Sem promessa de CPA, ROAS, posição ou Índice de Qualidade.** Nada apresentado como já publicado.
- **Conta existente**: auditar antes; migração faseada com volta atrás; preservar o que funciona.
- **Nomenclatura legível** (ex.: `PAÍS | CANAL | OBJETIVO | TEMA | SEGMENTO | VERSÃO`, campos opcionais; manter o padrão atual se ele funciona).
- **Linguagem simples para o lojista**; jargão só no modo avançado.

### Campaign Architecture Quality Gate (silencioso)
Objetivo comercial explícito? · Mercado e moeda certos? · Algum dado financeiro inventado? · Conversão e valor tratados como pré-requisito? · Estrutura cabe no orçamento? · Cada campanha tem motivo próprio? · Cada grupo tem intenção e página coerentes? · Tipos de campanha elegíveis? · Controles por tipo, sem extrapolar? · Negativas/marca sem bloqueio acidental? · Feed e estoque verificados ou pendentes? · Promessa de CPA/ROAS em algum lugar? · Nomes consistentes? · Migração com volta atrás (se conta existente)? · Próximas ações claras e executáveis? · Algo apresentado como publicado? — se falhar, corrija.

## Formato da saída
**Modo simples (padrão):** a árvore `Campanha → Grupo → Intenção → Página → Objetivo`, com o **motivo** de cada campanha existir, o **orçamento sugerido como hipótese**, as negativas a revisar, as **pendências** (medição, margem, feed, páginas) e **3 próximos passos**. Sem jargão.

**Modo avançado (sob pedido):** + tipo de lance e conversão usada, feed e grupos de produtos, matriz de negativas/exclusões por tipo de campanha, dependências técnicas, métricas por nível, riscos, plano de implantação ou migração com volta atrás, cenários de orçamento com premissas visíveis. Também sob pedido: auditoria de uma conta existente ou a árvore em formato estruturado para exportar — sem fingir que algo foi publicado.

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
