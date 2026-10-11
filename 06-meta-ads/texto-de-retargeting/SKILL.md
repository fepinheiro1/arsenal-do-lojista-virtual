---
name: texto-de-retargeting
description: Escreve anúncios de retargeting (remarketing) no Facebook e Instagram para quem já interagiu com a loja — a partir do evento real (visitou, viu produto, adicionou ao carrinho, iniciou checkout), da evidência sobre o que travou a compra e das exclusões certas (quem já comprou). Não denuncia rastreamento ("seu carrinho ainda está aqui"), não chuta objeção como se fosse causa, não inventa incentivo nem urgência, e checa evento, consentimento e catálogo antes de prometer personalização. Aceita produto, objetivo, eventos e públicos disponíveis, objeções com evidência, oferta, catálogo e orçamento. Use para criar, auditar, otimizar, segmentar ou sequenciar retargeting.
---

# Texto de Retargeting

## O que faz
Cria anúncios para **quem já interagiu com a loja** — mas começa pelo que se sabe de verdade: **qual evento aconteceu** (e se ele é confiável), **quem pode ser impactado** (consentimento, público disponível, quem precisa ser excluído) e **o que a loja realmente sabe** sobre o motivo da hesitação. Só então escreve a mensagem: útil, factual e que funciona mesmo para quem não esteve na loja.

Regra de ouro: **retargeting é um lembrete útil, não uma perseguição.** O anúncio não revela que a pessoa foi rastreada, não presume o que ela pensa, não inventa desconto ou prazo — e quem já comprou sai do público. A voz é da marca do lojista.

## Quando usar
- Montar campanhas para visitantes, quem viu produto, adicionou ao carrinho ou iniciou o checkout.
- Anúncios dinâmicos de catálogo para quem viu produtos.
- Auditar um retargeting que roda (mensagem, exclusões, evento, catálogo, cupom).
- Entender se o retargeting está gerando venda nova ou só recebendo crédito por quem compraria de qualquer jeito.

## O que a IA precisa de você
- `[produto ou loja]`, `[objetivo]` e `[página de destino]`.
- `[eventos e públicos disponíveis]` — o que o Pixel / API de conversões / integração já registram (visita, produto visto, carrinho, checkout, compra). Se não sabe, a skill trata como **pendência técnica**.
- `[objeções com evidência]` (opcional) — o que o atendimento, pesquisa, funil ou testes mostram. Sem evidência, a objeção vira **hipótese**.
- `[argumentos reais]` — políticas e condições verdadeiras (troca, frete, parcelamento, prova autorizada).
- `[oferta]` (opcional) — só se real, com validade e regras.
- `[catálogo]` (se usar anúncio dinâmico) e `[orçamento]`.

## Como funciona (por baixo)

**1. A skill escreve estratégia e copy — não configura nada.** Ela **não diz** que criou público, configurou pixel, rodou anúncio ou acessou eventos se não recebeu esses dados. O que depende da conta vira pendência técnica com o que conferir.

**2. Evento real, e evento não é intenção certa.** Visita, produto visto, carrinho, checkout, compra e eventos personalizados são coisas diferentes — e a definição real de cada um precisa ser conferida (um "início de checkout" disparando na página do carrinho estraga tudo). A origem também: Pixel, API de conversões, integração parceira ou dado próprio — nada é presumido configurado; com Pixel e API juntos, conferir a deduplicação. E **evento não prova o motivo**: ver um produto não é interesse profundo; adicionar ao carrinho não revela objeção; iniciar o checkout não significa "faltou um clique".

**3. Consentimento e público.** O uso de dados respeita as escolhas de privacidade, a lei aplicável e as políticas da plataforma — consentimento não se presume. Público personalizado só a partir de fontes e permissões existentes; tamanho mínimo e elegibilidade dependem da conta.

**4. Arquitetura mínima e janelas como hipótese.** Janelas de 1, 7, 14 ou 30 dias são **hipóteses**, não padrão universal: dependem do ciclo de compra e do volume. **Não precisa de um conjunto de anúncios por estágio**; separar só quando há volume e motivo. Verba curta não se pulveriza entre dezenas de públicos e criativos. Públicos sobrepostos se evitam quando atrapalham controle e medição — mas sobreposição não é canibalização automática. E a **expansão automática** de público (Advantage+, conforme a configuração) pode levar o anúncio a quem **nunca visitou a loja** — mais um motivo para a copy não presumir nada.

**5. Excluir quem já comprou — com cuidado.** Campanha de recuperação **sempre considera excluir compradores recentes** (sabendo que há atraso de dados e compra offline: exclusão não é instantânea). Compra parcial e recompra pedem exclusão por produto ou categoria — sem suprimir indiscriminadamente o cliente fiel.

**6. A mensagem não denuncia rastreamento.** Fora: "vimos você olhando", "seu carrinho ainda está aqui", "ainda pensando no seu par?", "você visitou 3 vezes". Também nada de atributo pessoal (saúde, dinheiro, condição). A copy funciona para **qualquer pessoa** que a veja. Por estágio, a direção é hipótese, não sequência obrigatória: **visitou** → contexto da loja; **viu produto** → diferenciais e dúvidas reais; **carrinho** → ajuda e informação para decidir; **checkout** → clareza (pagamento, entrega, troca). Uma sequência, se existir, é **progressão útil** (contexto → esclarecimento → prova → oferta real quando fizer sentido), nunca a mesma peça repetida.

**7. Objeção com evidência — e prova para cada uma.** Frete, tamanho, preço e confiança são **hipóteses** até o atendimento, uma pesquisa, o funil ou um teste sustentarem. E cada objeção se responde com a prova certa: tamanho → **tabela de medidas real**; frete → **política real**; confiança → **prova verificável** (política de troca, formas de pagamento, avaliação autorizada) — não um "compra segura" vago.

**8. Produto, oferta, página e catálogo.** Produto, variante, preço, disponibilidade, imagem e promessa iguais aos da página. Desconto, cupom, validade, frete, parcelamento e estoque só confirmados — e informação dinâmica (preço, estoque, prazo) **sincronizada**: dados mudam depois do evento. **Anúncio dinâmico de catálogo**: os IDs enviados pelo pixel precisam **bater com os IDs do catálogo** (senão a personalização não funciona); conferir preço, estoque, imagem, link e variante. Item esgotado: não insistir no mesmo SKU; alternativa só se compatível e autorizada. Criativo e copy combinam — nada de anúncio de produto específico com imagem genérica que engana.

**9. Incentivo com gate.** Desconto **não é padrão**: avaliar margem, política, histórico, ciclo e efeito incremental. Cupom recorrente **ensina a abandonar** e vaza para fora do público — preferir critérios de elegibilidade reais. Nada de urgência, contador, estoque baixo ou preço "de" inventados. (A mesma lógica da `recuperacao-de-carrinho`, frente 04.)

**10. Confiança, formato e política.** Peças de confiança usam políticas verificadas, demonstração factual, FAQ e avaliação autorizada; depoimento só real e com permissão. Feed, Stories e Reels com execução, zona segura e CTA próprios; variações automáticas de criativo revisadas antes de ativar. Políticas da Meta (atributos pessoais, práticas enganosas, destino) e categorias sensíveis (saúde, finanças, infantil) com controles adicionais.

**11. Um plano de contato, não três canais disparando.** E-mail, WhatsApp e anúncio atingem a mesma pessoa: planejar a **pressão total de contato** por jornada e consentimento — sem mandar a mesma oferta por todos os canais automaticamente.

**12. Medir sem se iludir.** Público de retargeting é pequeno, então a frequência sobe rápido: antes de concluir "criativo cansado", olhar frequência, alcance, CTR, CPM, conversão, oferta e página — pode ser **público saturado**. Métricas com janela de atribuição explícita; **ROAS não é lucro** (margem, incentivo, devolução). E retargeting é onde **atribuído mais se confunde com incremental**: muita gente compraria de qualquer jeito — teste de incrementalidade/holdout quando viável. Experimentos com hipótese, variável principal, público, orçamento, duração e critério definidos antes; sem dados suficientes, a recomendação é rotulada como hipótese — nada de previsão exata de CPA ou ROAS.

## Instruções (o cérebro da skill)
1. Identifique o **modo** (criar / auditar / otimizar / segmentar / sequenciar / catálogo / variações / replanejar) e fixe o **Retargeting Truth Lock**: evento, origem, elegibilidade, consentimento, público, janela, exclusões, produto, oferta, prova, destino, catálogo e políticas.
2. Verifique as **dependências técnicas** (evento confiável, deduplicação, IDs do catálogo, consentimento) — o que não está confirmado vira pendência, não premissa.
3. Defina a **arquitetura mínima** (públicos, janelas como hipótese, exclusões de compradores) compatível com o orçamento.
4. Para cada contexto: **hipótese → evidência → mensagem → criativo → CTA**, com objeção tratada só quando há evidência e respondida com a prova certa.
5. Passe pelo **gate de incentivo**, pela coordenação com e-mail/WhatsApp e pela checagem de política.
6. Rode o **Quality Gate** e entregue os textos prontos, separados das pendências.

## Regras de qualidade
- **Nada de rastreamento exposto** nem atributo pessoal; copy compreensível para quem não visitou.
- **Evento ≠ intenção**; objeção sem evidência é hipótese; cada objeção com a prova certa.
- **Compradores excluídos** (considerando atraso); recompra e cliente fiel tratados por produto/categoria.
- **Arquitetura mínima**; janelas como hipótese; sem um conjunto por estágio por padrão.
- **Produto, oferta, prova e página verdadeiros**; dados dinâmicos sincronizados; catálogo com IDs batendo.
- **Incentivo com gate**; sem cupom recorrente por padrão; sem urgência inventada.
- **Coordenação com e-mail/WhatsApp**; sem a mesma oferta em todos os canais.
- **Nunca afirmar acesso à conta** nem configuração feita.
- **Medição honesta**: saturação × cansaço, ROAS ≠ lucro, atribuído ≠ incremental.
- **Persuasão ética** (a mesma do Arsenal): retomada é convite, nunca culpa ("você desistiu", "você abandonou"); sem "imperdível", "última chance", escassez falsa, garantia de resultado.
- **Voz da marca, não da Performa.**

### Retargeting Quality Gate (silencioso)
O evento é confiável e está bem definido? · Consentimento e público respeitados? · A copy revela rastreamento ou presume o que a pessoa pensa? · Atributo pessoal? · A objeção tem evidência — e a prova certa? · Preço, estoque e variante corretos e sincronizados? · Compradores excluídos? · Página coerente? · Catálogo com IDs batendo? · Incentivo passou pelo gate? · Urgência ou escassez inventada? · Coordenado com e-mail/WhatsApp? · Algum claim sem prova? · Afirma configuração ou acesso que não teve? — se falhar, corrija.

## Formato da saída
**Versão simples:** para cada contexto (evento), `Evento → Hipótese → Evidência → Mensagem → Criativo → CTA → Exclusões`, com os **textos prontos** (texto principal, título, descrição quando aplicável e CTA). Depois, num bloco separado, as **dependências técnicas e pendências** — nunca `[preencher]` dentro do anúncio.

Sob pedido: auditoria de um retargeting existente, segmentação por janelas, sequência de mensagens, configuração de anúncio dinâmico de catálogo, variações de teste com hipótese, ou replanejamento com dados.

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
