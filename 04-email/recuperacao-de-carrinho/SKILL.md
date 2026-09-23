---
name: recuperacao-de-carrinho
description: Desenha o fluxo de recuperação de compra por evento — navegação, carrinho, checkout ou falha de pagamento — removendo fricção sem mentir sobre intenção, estoque, preço ou urgência. Sai na hora quando a compra acontece, usa incentivo só quando faz sentido, e respeita o que a plataforma realmente suporta. Aceita o evento, o estado do carrinho, produto/preço/estoque, objeções reais e a plataforma. Use para criar, otimizar ou auditar o fluxo.
---

# Recuperação de Carrinho

## O que faz
Cria o fluxo que reencontra quem estava perto de comprar — mas primeiro pergunta **qual evento realmente aconteceu** (só navegou? adicionou ao carrinho? começou o checkout? o pagamento falhou?), qual é o estado atual da compra e **qual é a menor intervenção necessária**. Muitas recuperações não precisam de desconto — precisam remover fricção. E a regra de ouro é sair na hora: compra confirmada, a pessoa deixa o fluxo.

Regra de ouro: **recuperar compra não é pressionar — é remover fricção sem mentir sobre intenção, estoque, preço ou urgência.** A voz é da marca do lojista.

## Quando usar
- Montar (ou melhorar) a automação de carrinho/checkout abandonado.
- Tratar falha de pagamento (evento diferente de abandono).
- Auditar um fluxo existente (evento, verdade do carrinho, saída por compra, colisões).

## O que a IA precisa de você
- `[evento]` — navegação, carrinho, checkout ou falha de pagamento (e se a plataforma **confirma** o evento).
- `[estado do carrinho]` — produtos, variantes, quantidade, preço (idealmente dinâmicos da plataforma).
- `[plataforma]` — o que ela suporta (deep link para retomar, persistência do carrinho, dados de estoque/preço, supressão). Sem isso, a skill usa linguagem conservadora e placeholders.
- `[objeções reais]` (com evidência) e `[apoios reais]` (troca, pagamento, atendimento — só o que é verdade).
- `[incentivo]` (opcional) — cupom/condição real, só se existir.

## Como funciona (por baixo)

**1. Classifica o evento — não é tudo "você esqueceu seu carrinho".** *Navegação* (só viu um produto; intenção menor; não afirmar que estava no carrinho) · *Carrinho* (adicionou, mas o checkout pode nem ter começado) · *Checkout* (avançou; há mais contexto) · *Falha de pagamento* (não é abandono voluntário — mensagem mais operacional, oferecer nova tentativa/alternativa, sem culpa). E só usa linguagem específica quando a plataforma **confirma** o evento; com dado genérico, mensagem conservadora.

**2. Verdade do carrinho é dinâmica.** Produtos, variantes (cor/tamanho/quantidade), preço e subtotal vêm do e-commerce — não se congela no texto um valor que pode ter mudado. O preço pode variar entre o abandono e o envio; a promoção pode expirar; o estoque pode esgotar. Nada de "restam 2" numa copy estática sem integração confiável, nem preço antigo prometido sem política real.

**3. "Guardamos seu carrinho" só se for verdade.** Muita plataforma não reserva estoque, expira a sessão ou reconstrói o carrinho — então essa frase (que a V1 usava) só entra se for tecnicamente verdadeira. O CTA ideal é um **deep link** que retoma o carrinho/checkout específico (funcionando cross-device quando a tecnologia suporta) — sem inventar merge tag, e respeitando a **expiração** (não mandar um link quebrado dias depois).

**4. Sai na hora (Purchase Exit) e não colide.** Regra absoluta: **compra confirmada → sair imediatamente do fluxo** (nada de lembrar de um produto já comprado; compra parcial e cancelamento/reembolso seguem a regra da plataforma, sem assumir). Suprime quem comprou, descadastrou, deu bounce ou está com item indisponível. E resolve **colisão de fluxos**: carrinho tem prioridade sobre navegação; checkout sobre carrinho; falha de pagamento sobre o marketing genérico — para a pessoa não receber três mensagens no mesmo dia (e-mail, SMS, WhatsApp e push não disparam todos juntos por padrão).

**5. Lembrete antes de desconto; incentivo com critério.** O primeiro contato muitas vezes só **facilita o retorno** — muita gente volta sem cupom nenhum. O incentivo passa por um **gate**: margem, histórico, valor do carrinho, segmento e promoção já existente. Cupom **não é obrigatório**, e cupom recorrente ensina o cliente a abandonar de propósito, vaza e canibaliza a venda a preço cheio — por isso, condicional/segmentado. Frete grátis só com regra/região/mínimo reais; urgência só com prazo/estoque/token verdadeiros.

**6. Trata a objeção com evidência, e oferece ajuda.** Não adivinha por que a pessoa abandonou — usa objeções que a loja **realmente observou** (pesquisa, atendimento, etapa do checkout) e responde só com apoios verdadeiros (troca, pagamento seguro, atendimento). Muitas vezes o melhor CTA secundário é **suporte** (responder o e-mail, WhatsApp, guia de tamanho) — só um canal que existe de verdade.

**7. Papéis, timing e medição.** Cada mensagem tem um papel (lembrar, restaurar o carrinho, ajudar, tranquilizar, esclarecer, provar, incentivar, recuperar pagamento, avisar disponibilidade) — não "e-mail 2 = objeção" por regra. O timing vem do **evento** (checkout e falha de pagamento pedem resposta mais rápida que navegação) e da expiração do carrinho, não de uma cadência fixa. E a medição olha receita recuperada, retomada de checkout e reclamações — lembrando que "comprou depois do e-mail" **não é** o mesmo que "o e-mail causou a compra" (só um holdout mostra o incremento real).

## Instruções (o cérebro da skill)
1. Identifique o **modo** (criar / otimizar / auditar / mapear eventos / ramificar / só copy / simplificar / replanejar) e fixe o **Recovery Truth Lock** (evento + confiança, identidade/consentimento, estado do carrinho, produto/variante, preço/promo/estoque, persistência/deep link, status do cliente, evidência de objeção, regras de incentivo, purchase exit, supressão/colisão, canal).
2. **Classifique o evento** e defina a **elegibilidade, a saída e as supressões**.
3. Atribua **papéis** às mensagens e o **timing pelo evento**.
4. Escreva com **verdade dinâmica** (bloco de produto/preço via plataforma + fallback), tratando objeção com evidência e passando o incentivo pelo **gate**.
5. Rode o **Quality Gate** e entregue as regras de gatilho, saída, supressão e prioridade.

## Regras de qualidade
- **Evento certo**: linguagem coerente com o que aconteceu (e confirmado); navegação não vira "seu carrinho".
- **Verdade dinâmica**: produto/variante/preço/estoque reais; sem congelar valor, sem "restam 2" estático, sem prometer preço antigo.
- **"Guardamos seu carrinho" e reserva** só se a plataforma faz isso; deep link real, sem link expirado.
- **Purchase Exit é absoluto**; supressão e colisão de fluxos consideradas.
- **Incentivo com gate** (margem, leakage); cupom não obrigatório; frete grátis/urgência só se reais.
- **Objeção com evidência**, não adivinhação; apoios e suporte só se existem.
- **Persuasão ética** (a mesma do Arsenal): lembrete é gentileza, nunca culpa; sem "imperdível", "última chance", contagem regressiva fabricada.
- **Personalização com fallback**; multi-item vira resumo, não e-mail gigante; entregabilidade herdada do `html-newsletter`.
- **Voz da marca, não da Performa.**

### Recovery Quality Gate (silencioso)
O evento está certo e confirmado? · A linguagem bate com ele? · Carrinho/variante/preço/estoque dinâmicos? · Prometeu reserva que não existe? · Deep link real e não expirado? · Purchase Exit presente? · Supressão e prioridade de fluxo ok? · Timing pelo evento? · O desconto é necessário (ou o lembrete basta)? · Margem/leakage considerados? · Frete/políticas reais? · Urgência verdadeira? · Objeção com evidência? · Personalização com fallback? · Multi-item enxuto? · Cross-channel coordenado? · KPI de receita recuperada (open é secundário)? · Confunde recuperado com incremental? — se falhar, corrija.

## Formato da saída
O **fluxo por evento** — para cada mensagem: `Papel | Quando | Assunto | Preheader | Corpo | CTA (retoma o carrinho)`, com o bloco de produto dinâmico indicado. Depois, as **regras de automação**: gatilho por evento, janelas de tempo, **saída por compra**, supressões e prioridade entre fluxos. O incentivo (se houver) fica claramente condicional.

Sob pedido: o mapa dos eventos (navegação/carrinho/checkout/pagamento) com a mensagem de cada um, a coordenação com SMS/WhatsApp, a auditoria de um fluxo existente, ou só a copy. Nada de relatório por padrão.

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
