---
name: sequencia-boas-vindas
description: Desenha a jornada de boas-vindas de um novo contato como uma automação que reage ao comportamento — parte da origem e da promessa do cadastro, cumpre essa promessa no primeiro e-mail, e sai do fluxo de "primeira compra" quando a pessoa compra. Adapta número de e-mails, papéis, timing e ramificações à intenção, sem fórmula fixa. Aceita origem, promessa, consentimento, status do cliente, marca, oferta e plataforma. Use para criar, otimizar ou auditar o fluxo.
---

# Sequência de Boas-Vindas

## O que faz
Monta a jornada que recebe o novo contato — mas a pergunta deixa de ser "quais 4 e-mails mandar?" e passa a ser *"qual jornada faz sentido para esta pessoa, dado por que ela entrou, o que prometemos e o que ela já fez desde então?"*. O primeiro e-mail cumpre na hora o que foi prometido no cadastro; os seguintes constroem confiança e ajudam a decidir; e o fluxo **reage ao comportamento** — quem compra sai da sequência de primeira compra, quem já era cliente não entra nela.

Regra de ouro: **um welcome bom reage ao comportamento — ele não continua vendendo "primeira compra" para quem já comprou.** A voz é da marca do lojista.

## Quando usar
- Criar (ou refazer) o fluxo de boas-vindas de quem assina a lista, pega um cupom, faz um quiz ou entra por um lead magnet.
- Auditar uma automação existente (promessa, papéis, timing, saídas, colisões).
- Simplificar um fluxo complicado demais, ou ramificá-lo por segmento/comportamento.

## O que a IA precisa de você
- `[origem e promessa do cadastro]` — de onde veio (newsletter, pop-up, cupom, quiz, waitlist...) e **o que foi prometido** em troca (cupom, guia, acesso, novidades). É o que o e-mail 1 tem de entregar.
- `[status do contato]` — é lead novo ou já é cliente? (muda a jornada).
- `[marca e diferencial reais]`, `[produtos/categorias âncora]`, `[oferta]` (cupom só com valor real).
- `[plataforma]` (opcional) — define o que dá para automatizar (branching, suppression, dados). Sem ela, a skill entrega a jornada e marca o que depende da ferramenta.

## Como funciona (por baixo)

**1. Parte da origem e da promessa — e as cumpre.** A origem do cadastro muda a expectativa (um cupom sinaliza intenção comercial; um lead magnet, interesse específico; uma waitlist, o lançamento). A pergunta crítica: *o que foi prometido em troca do cadastro?* — e o **e-mail 1 entrega isso de forma clara e imediata** (o cupom aparece; o guia vem junto), sem esconder para forçar leitura.

**2. Respeita o consentimento.** O fluxo de boas-vindas não é desculpa para mandar marketing a uma base sem contexto legítimo — só entra quem consentiu, e a expectativa criada no cadastro é honrada.

**3. O objetivo (e o tamanho) vêm da intenção.** Primeira compra é comum, mas o objetivo pode ser entregar a promessa, orientar, gerar a primeira sessão, construir confiança, descobrir preferência ou preparar um lançamento. A jornada **não é uma sequência linear obrigatória**: pode ser 1 e-mail, 2–3, 4–6 ou com ramificações — a quantidade nasce da intenção e da complexidade da compra.

**4. Cada e-mail tem um papel — não uma posição fixa.** Cumprir a promessa, orientar, apresentar a marca, ajudar a descobrir, educar, provar, tratar objeção, incentivar, lembrar, coletar preferência, dar suporte. Nada de "e-mail 2 = história da empresa" por regra. A marca é apresentada **pelo valor para quem chega** (curadoria, origem, serviço, expertise), com fatos reais — sem inventar "começamos na garagem", fundador ou anos de história.

**5. Reage ao comportamento (com parcimônia).** Duas ramificações centrais: **quem já é cliente** não recebe a jornada de primeira compra (vai para orientação/newsletter); e a **saída por compra** — se a pessoa compra durante o fluxo, ela **sai** da sequência de incentivo (ou migra para o pós-compra), e os e-mails de "use seu cupom" são suprimidos. Sinais de comportamento (clique, sessão, visita a produto) valem mais que "abriu" — o *open* é impreciso (a privacidade do Apple Mail infla) e não deve reger uma ramificação crítica. E há um **teto de complexidade**: use a menor ramificação que resolve; branching demais vira automação impossível de manter.

**6. Ajuda a decidir; incentivo é ferramenta, não muleta.** Em vez do catálogo inteiro, oferece poucas rotas claras (por necessidade, categoria, perfil) e, quando a compra exige entendimento, um e-mail que **educa** (como escolher, medidas, compatibilidade) — que muitas vezes converte melhor que mais desconto. Trata objeções reais (tamanho, frete, troca, confiança) só com políticas e dados reais, e usa prova social **verdadeira**. Cupom, quando existe, tem valor/código/mínimo/validade reais (sem inventar, sem contagem regressiva falsa); lembrete de cupom só se ele existe, está válido e a pessoa não comprou. **Valor antes de pressão**: se os e-mails 2–4 só dizem "use seu cupom", a jornada está fraca.

**7. Timing por propósito, e sem colidir.** Sem "dia 2–3 / 4–6 / 7–9" fixo: o e-mail 1 sai imediato quando há promessa a cumprir, e cada intervalo depois tem uma razão (dar tempo de consumir, visitar, decidir — sem bombardear) e depende do ciclo de compra (cosmético simples ≠ móvel de alto ticket). Assunto e preheader **coerentes com o papel** de cada e-mail (a jornada parece uma jornada, sem "Parte 1/2/3"). E o fluxo considera **colisões** com outras automações (carrinho, campanha, pós-compra) e **supressões** (comprou, descadastrou, deu bounce) para a pessoa não receber três e-mails no mesmo dia. Entregabilidade herda os alertas do `html-newsletter` (autenticação, descadastro, consentimento).

## Instruções (o cérebro da skill)
1. Identifique o **modo** (criar / otimizar / auditar / ramificar / simplificar / adaptar origem-plataforma / só escrever a copy de um fluxo definido / replanejar com dados) e fixe o **Welcome Truth Lock** (origem, promessa, consentimento, status do cliente, marca, produto, cupom, plataforma, regras de saída/supressão).
2. Defina o **objetivo da jornada** e o **número de e-mails** pela intenção.
3. Atribua um **papel** a cada e-mail; desenhe as **ramificações** (cliente existente, saída por compra) na menor complexidade que resolve.
4. Defina o **timing por propósito** e escreva **assunto/preheader/corpo/CTA** coerentes com cada papel.
5. Rode o **Quality Gate** e entregue no **nível** pedido (simples, automação ou estratégico), com as regras de gatilho, delay, saída e supressão.

## Regras de qualidade
- **Cumpre a promessa no e-mail 1** (o cupom/guia aparece; nada escondido).
- **Reage ao comportamento**: cliente existente não entra na jornada de 1ª compra; quem compra sai do incentivo.
- **Cada e-mail tem um papel**; nem todo e-mail pede compra (o KPI de cada um segue o seu papel).
- **Verdade**: sem inventar cupom, prazo, política, diferencial, "mais vendido" ou história da marca; o que falta vira `[preencher]`.
- **Valor antes de pressão**; incentivo é opcional; sem urgência/escassez falsa nem contagem regressiva sem base.
- **Timing com razão**; sem horário mágico; ramificação crítica não depende de "abriu".
- **Supressão e colisão** consideradas; personalização com fallback.
- **Persuasão ética** (a mesma do Arsenal): sem "melhor do mundo", "imperdível", "última chance"; sem abrir pela culpa da pessoa.
- **Voz da marca, não da Performa**; entregabilidade herdada do `html-newsletter`.

### Welcome Journey Quality Gate (silencioso)
Promessa cumprida no primeiro contato? · Consentimento adequado? · Cliente existente tratado? · Existe saída por compra? · Cada e-mail tem papel? · Timing justificado? · Cupom e validade reais? · Sem pressão repetitiva? · O conteúdo ajuda a escolher? · Prova social real? · Personalização com fallback? · A ramificação usa sinal confiável? · Os fluxos podem colidir? · Supressão adequada? · KPI por papel? · Alertas de entregabilidade herdados? · A jornada é simples o bastante para manter? · Parece template genérico? — se falhar, reestruture.

## Formato da saída
Adaptado ao que você precisa:
- **Simples** (padrão): a jornada numerada — para cada e-mail: `Papel | Quando | Assunto | Preheader | Corpo | CTA` — mais uma linha de como agendar (gatilho, intervalos, e a **saída por compra**).
- **Automação** (sob pedido): acrescenta `Gatilho | Delay | Ramificação | Saída | Supressão`.
- **Estratégica** (sob pedido): acrescenta `Objetivo | KPI por papel | Hipótese | Teste`.

Nada de complexidade despejada por padrão. Sob pedido: só a copy de um fluxo já definido, a auditoria de um fluxo existente, ou a versão ramificada por segmento.

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
