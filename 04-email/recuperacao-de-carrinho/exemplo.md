# Recuperação de Carrinho — exemplo real

## Entrada
```
Loja: Passo Firme — calçados de couro masculinos
Público: homens 30–55 que valorizam durabilidade e conforto
Tom da marca: direto, confiável, sem firula
Objeções comuns: dúvida de numeração e receio de couro que aperta no começo
Apoios reais: troca de numeração sem custo em 30 dias, pagamento por Pix e cartão, atendimento por WhatsApp
Incentivo: não informado
Link do carrinho: {{ url_carrinho }}
```

## Saída

**E-mail 1 — Lembrete gentil (2h depois)**
- Assunto: Guardamos seu carrinho
- Preheader: Ele está aqui, do jeitinho que você deixou.
- Corpo:
  Você separou um par na Passo Firme e a gente guardou pra você.
  Sempre que quiser continuar, é só um clique — o carrinho está do jeito que você deixou.
  **CTA: Voltar ao meu carrinho**

**E-mail 2 — Tira a dúvida (dia seguinte)**
- Assunto: Ficou com dúvida na numeração?
- Preheader: A gente resolve isso sem custo, com calma.
- Corpo:
  Comprar sapato sem provar dá um receio — a gente sabe.
  Por isso, se a numeração não vier perfeita, a **troca é sem custo em até 30 dias**. E o couro cede um pouco com o uso, ganhando o formato do seu pé.
  Ainda em dúvida entre dois tamanhos? Responda este e-mail ou chame no WhatsApp que a gente te ajuda a escolher.
  **CTA: Retomar a compra**

**E-mail 3 (opcional) — Incentivo (3 dias depois)**
- Assunto: Seu par continua reservado
- Preheader: E uma condição pra facilitar, se ajudar.
- Corpo:
  Seu par ainda está no carrinho, esperando você decidir com tranquilidade.
  [Se você tiver um cupom real: **preencher código e valor** — para dar aquele empurrãozinho.]
  Pagamento no Pix ou cartão, e a troca de numeração continua garantida. Qualquer coisa, é só responder.
  **CTA: Finalizar meu pedido**

Como agendar: gatilho = carrinho abandonado. Janelas: E1 em 2h, E2 em 24h, E3 em 72h. Ative o E3 só se você tiver um incentivo real para oferecer — sem incentivo, pare no E2.

> Referência: o E1 é puro lembrete acolhedor, sem culpa e sem cupom; o E2 ataca a objeção verdadeira (numeração) com um apoio real (troca sem custo), não com pressão; o incentivo do E3 fica condicionado a existir de verdade e o valor não foi inventado; tom da marca preservado, frases curtas.
