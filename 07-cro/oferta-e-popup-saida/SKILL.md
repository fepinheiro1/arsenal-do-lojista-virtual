---
name: oferta-e-popup-saida
description: Decide primeiro SE vale interromper quem está saindo — pop-up, slide-in, bloco na página, ajuda contextual ou nada — e, quando vale, monta a oferta e o texto com verdade, economia e consentimento: gatilho honesto por dispositivo (no celular não existe "intenção de saída" confiável), quem pode ver, frequência e supressões, oferta real que não ensina a sair para ganhar cupom, fechar fácil e acessível, e medição com grupo sem pop-up. Recomenda não exibir quando isso é melhor (no checkout, quase sempre). Use para criar, auditar, otimizar, testar ou adaptar pop-ups e ofertas na loja.
---

# Oferta e Pop-up de Saída

## O que faz
Antes de escrever qualquer pop-up, decide **se interromper a visitante ajuda** — e de que jeito: **pop-up**, **slide-in discreto**, **bloco na própria página**, **ajuda contextual** (guia, tabela de medidas, atendimento) ou **nada**. Quando vale exibir, monta a oferta e o texto com a verdade das condições, a conta da margem, o gatilho certo para cada dispositivo, as regras de quem vê e quantas vezes, um fechamento fácil e o consentimento separado para marketing. E define como saber se funcionou de verdade.

Regra de ouro: **o pop-up abre uma oportunidade real — ou não aparece.** Sem culpa, sem desespero, sem contador falso, sem recusa humilhante; e "não exibir" é uma recomendação válida quando protege a compra e a experiência. A voz é da marca do lojista.

## Quando usar
- Página com muita saída sem compra, ou vontade de capturar contato de quem ainda está decidindo.
- Revisar um pop-up que já roda (frequência, oferta, consentimento, acessibilidade, resultado).
- Testar se o pop-up gera venda a mais ou só dá desconto para quem já compraria.
- Decidir o que fazer quando alguém pede um pop-up no checkout.

## O que a IA precisa de você
- `[página e objetivo]` — onde aparece (home, categoria, produto, carrinho) e o que se quer: compra, contato, aviso de reposição, ajuda.
- `[o que se sabe sobre a saída]` — dados (saída por página, dispositivo, etapa) ou relatos. Sem dados, a skill trata como hipótese.
- `[oferta real]` (se houver) — cupom, frete, brinde, guia, aviso de reposição — com valor, validade (data e horário), mínimo, exclusões. E a **margem**, se possível.
- `[o que pede em troca]` — nada, e-mail, WhatsApp — e se haverá uso para marketing.
- `[outras automações]` — boas-vindas, carrinho abandonado, retargeting, WhatsApp — para não dar incentivo em dobro.
- `[plataforma e ferramenta de pop-up]` e `[marca e tom]`.

## Como funciona (por baixo)

**1. Decisão antes do texto.** Primeiro o diagnóstico: página, objetivo, tráfego, etapa da jornada, dispositivo, frequência e os sinais disponíveis — **nem toda saída é uma objeção** (a pessoa pode só estar pesquisando, comparando ou voltando depois). Observação medida, inferência plausível e suposição ficam separadas. Daí sai a decisão: **exibir, adiar, trocar por algo menos invasivo ou não exibir** — com justificativa.

**2. Objetivo claro.** Compra, contato qualificado, suporte, descoberta de produto, lista de espera e retenção pedem intervenções diferentes. **E-mail capturado não é receita.**

**3. Gatilho honesto, por dispositivo.** No computador, o cursor saindo da janela é um **sinal imperfeito** de saída (tem falso positivo e limite de navegador). **No celular não existe equivalente confiável** — usam-se sinais de contexto (tempo na página, rolagem, inatividade, evento de carrinho) com moderação, sem dizer que "detecta a intenção". Cada gatilho fica descrito: evento, condição, atraso, quem é elegível, intervalo de descanso e motivo de exibir.

**4. Página certa e sem disputa.** Home, categoria, produto e carrinho pedem tratamentos diferentes; **no checkout, quase sempre o certo é nenhum pop-up** — é o ponto mais quente da compra. E o pop-up não pode brigar com o banner de cookies, o chat, os avisos de frete ou as validações do formulário.

**5. Quem vê, quantas vezes, e quando para.** Visitante novo, recorrente, assinante, quem já comprou, quem já usou a oferta — sem presumir identidade onde não há dado. **Depois de comprar, se inscrever ou usar o cupom, a mesma oferta não aparece de novo.** Fechou ou recusou: respeitar, com intervalo proporcional — não reabrir na mesma sessão. Limite por sessão, por visitante e por campanha. Vários pop-ups (cupom, frete, captura, reposição) com prioridade e sem empilhar. E coordenação com **boas-vindas, carrinho abandonado, retargeting e WhatsApp** — sem dar o mesmo incentivo em dois lugares.

**6. Utilidade antes de desconto — e desconto com conta.** Muitas saídas se resolvem com **informação** (frete e prazo, tabela de medidas, comparação, atendimento, aviso de reposição), não com cupom. Oferta só **verdadeira**: valor, validade com data e fuso, mínimo, exclusões e disponibilidade confirmados. Antes de recomendar desconto: margem de contribuição, custo do incentivo, frete subsidiado, taxas. Dois riscos: o cupom pode ir para **quem já ia comprar** (canibalização) e pode **ensinar o cliente a ameaçar sair para ganhar desconto** — elegibilidade limitada e resgates monitorados. Personalizar pelo contexto da página e pelo interesse declarado, **sem expor vigilância** ("vimos que você olhou...").

**7. Texto curto, saída digna, sem truque.** Título com o valor, apoio com a condição real, botão que diz a ação, recusa neutra ("Continuar navegando"). **Proibido**: contador falso ou que reinicia, escassez fictícia, recusa humilhante ("não, prefiro pagar caro"), caixa pré-marcada, condição escondida. Cronômetro só se refletir a expiração real.

**8. Dados e consentimento.** Pedir só o necessário. **Receber o cupom é diferente de aceitar marketing**: resgate sem cadastro, ou cadastro com finalidade clara — e, se houver marketing, consentimento **separado e não pré-marcado**, explicando finalidade e direitos (LGPD). Pegar um cupom **não autoriza** campanhas sem fim. WhatsApp tem opt-in próprio, nunca embutido num botão ambíguo.

**9. Fechar fácil, acessível e leve.** Fechar é simples e visível, por toque, teclado e **Esc**; o foco vai para o conteúdo ao abrir e volta para onde estava ao fechar; o diálogo tem rótulo e semântica; nada de prender o teclado ou travar a rolagem escondendo o botão de fechar. No celular: cabe na tela pequena, não cobre conteúdo crítico, funciona com teclado virtual, zoom e rotação; respeita quem pediu menos animação. O Google orienta evitar intersticiais intrusivos no celular — a skill segue a orientação vigente, sem afirmar penalidade automática por qualquer pop-up. O pop-up não pode atrasar o conteúdo principal nem mexer o layout. Plataforma e ferramenta reais (sem presumir acesso ao checkout ou a APIs). Plano B para quando o benefício falha: cupom expirado, produto sem estoque, erro de rede.

**10. Saber se funcionou de verdade.** Eventos consistentes: elegível, exibido, fechado, clique, envio, cupom aplicado, pedido, erro. Taxa calculada sobre **quem foi exposto e era elegível**; conversão do formulário ≠ compra ≠ receita por visitante. **Compra depois do pop-up não prova que o pop-up causou a compra** — o primeiro teste é **com pop-up × sem pop-up (grupo de controle)**, com sorteio estável por visitante; só depois se otimiza oferta, gatilho, formato e texto. Amostra e duração adequadas (semanas inteiras). Proteção: rejeição, abandono do checkout, reclamações, taxa de fechamento, estabilidade do layout, **receita líquida do desconto**, descadastros, e a qualidade dos contatos capturados (compram? pedem para sair?).

## Instruções (o cérebro da skill)
1. Identifique o **modo** (criar / auditar / otimizar / testar / adaptar / recomendar não exibir / lote) e faça o **diagnóstico**: página, objetivo, dispositivo, etapa, evidência.
2. **Decida a intervenção** (pop-up, slide-in, bloco, ajuda, nada) e justifique.
3. Se houver intervenção: **elegibilidade, gatilho por dispositivo, frequência, supressões** e coordenação com outras campanhas e automações (**Trigger & Consent Lock**).
4. Defina a **oferta** passando pela verdade e pela conta (**Offer Truth Lock**: valor, validade com fuso, mínimo, exclusões, estoque, margem) — ou a utilidade no lugar dela.
5. Escreva o **texto** e o **consentimento**; confira fechamento, acessibilidade, celular e desempenho.
6. Defina a **medição** (com grupo sem pop-up) e rode o **Quality Gate**.

## Regras de qualidade
- **Não exibir é uma recomendação válida**; checkout quase sempre sem pop-up.
- **Gatilho honesto**: no celular não há "intenção de saída" confiável.
- **Frequência e supressões**: não repete depois de comprar, inscrever ou recusar; sem empilhar campanhas; sem incentivo em dobro com outras automações.
- **Utilidade antes de desconto**; oferta verdadeira e com conta de margem; risco de canibalização e de "ensinar a sair" considerado.
- **Sem padrão manipulador**: contador falso, escassez fictícia, recusa humilhante, pré-seleção, condição escondida.
- **Consentimento separado** para marketing; cupom não é autorização; WhatsApp com opt-in próprio.
- **Fechar fácil e acessível** (toque, teclado, Esc, foco); celular e desempenho conferidos.
- **Sem vigilância exposta** na personalização.
- **Medição com grupo sem pop-up**; e-mail ≠ receita; compra depois ≠ compra causada.
- **Nada inventado**: valor, validade, condição, integração, resultado. Pendência fica no briefing, nunca na arte pronta.
- **Persuasão ética** (a mesma do Arsenal): sem culpa, sem desespero, sem "última chance". **Voz da marca, não da Performa.**
- **Sem colchete no texto pronto**: nome ou data que faltam ficam fora do texto publicável, como pendência.
- **Toda conta por código; alerta sem número novo**: com código disponível, nenhuma conta ou contagem de cabeça — nem nos alertas. Alerta e observação só repetem números já calculados (nos testes, a IA acertava a conta principal e errava os números "de passagem").

### Exit Offer Quality Gate (silencioso)
A intervenção é necessária (ou "não exibir" é melhor)? · Objetivo claro? · Gatilho honesto por dispositivo? · Fora do checkout? · Frequência e supressões definidas? · Conflito com outras campanhas e automações? · Oferta verdadeira, com validade e condições reais? · Margem e canibalização consideradas? · Algum padrão manipulador? · Consentimento separado e não pré-marcado? · Fechar fácil por toque, teclado e Esc? · Celular, acessibilidade e desempenho ok? · Medição com grupo sem pop-up? · Algo inventado? — se falhar, corrija.

## Formato da saída
1. **Decisão** (exibir? qual formato?) e o porquê, com o grau de evidência.
2. Se exibir: **quem vê**, **gatilho** (computador e celular), **frequência e supressões**, **oferta** (condições reais e conta), **texto** (título, apoio, CTA, recusa) + 2 variações de título, **consentimento**, checklist de **fechamento, acessibilidade e celular**.
3. **Medição**: eventos, grupo sem pop-up, métrica principal e de proteção.
4. **Dependências e pendências** (cupom ativo, validade, integração, coordenação com automações).

Modo avançado (sob pedido): regras de gatilho e supressão detalhadas, eventos, casos de teste de QA, desenho do experimento.

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
