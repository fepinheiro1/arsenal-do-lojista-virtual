---
name: recuperacao-de-carrinho
description: Escreve uma sequência de 2 a 3 e-mails para quem adicionou ao carrinho e não finalizou — do lembrete gentil ao incentivo, tratando a dúvida real da compra sem urgência falsa. Use ao montar o fluxo de carrinho abandonado na ferramenta de e-mail.
---

# Recuperação de Carrinho

## O que faz
Cria o fluxo que reencontra quem estava a um passo de comprar: e-mail 1 é um lembrete gentil, e-mail 2 trata a objeção que costuma travar a compra (dúvida, frete, confiança) e o e-mail 3 (opcional) traz um incentivo real. Recupera receita da visita que já aconteceu — sem parecer cobrança.

## Quando usar
- Ao montar (ou melhorar) a automação de carrinho abandonado.
- Quando muita gente adiciona ao carrinho e some no checkout.
- Para complementar a mensagem genérica "você esqueceu algo" que não converte.

## O que a IA precisa de você
- `[nome da loja]` e o que vende.
- `[público]` — para calibrar o tom.
- `[tom da marca]` — como a loja fala.
- `[objeções comuns]` — o que costuma travar a compra (frete, prazo, dúvida de tamanho, segurança do pagamento).
- `[apoios reais]` — o que a loja oferece e é verdade: troca facilitada, pagamento seguro, atendimento humano, frete em condição X. Se não tiver certeza, marque `[preencher]`.
- `[incentivo]` (opcional) — cupom ou condição real para o 3º e-mail. Valor entra como `[preencher]` se não informado.
- `[link do carrinho]` — a tag que a ferramenta usa para retomar o carrinho.

## Instruções (o cérebro da skill)
Escreva de 2 a 3 e-mails:

1. **E-mail 1 — Lembrete gentil (1 a 3 horas depois).** Curto e acolhedor. "Guardamos seu carrinho." Mostra o(s) item(ns) e um CTA direto para retomar. Sem cupom ainda — muita gente volta só com o lembrete. Tom de gentileza, nunca de cobrança.
2. **E-mail 2 — Tira a dúvida (dia seguinte).** Vá na objeção real: reforce os apoios verdadeiros (troca, pagamento seguro, atendimento). Uma frase que convida a responder o e-mail com qualquer dúvida. CTA para o carrinho.
3. **E-mail 3 (opcional) — Incentivo (2 a 3 dias depois).** Só se houver incentivo real. Apresente a condição com calma, ligada ao benefício, e mantenha o carrinho acessível. Sem "só até meia-noite" nem contagem regressiva fabricada.

Cada e-mail: **assunto** (até ~45 caracteres), **preheader** e **corpo** curto com 1 CTA que retoma o carrinho.

## Regras de qualidade
- Lembrete é gentileza, não cobrança. Nunca fazer a pessoa se sentir culpada por "abandonar".
- Sem urgência ou escassez falsa. Se houver prazo real de cupom ou estoque, dizer com calma e só se for verdade.
- Não prometer o que a loja não cumpre (frete grátis, entrega em X dias): marcar `[preencher]`.
- Nunca inventar valor de cupom ou desconto.
- Um CTA por e-mail, sempre retomando o carrinho. Benefício antes da pressão. Frases curtas.
- Voz da marca do lojista — a Performa não assina.

## Formato da saída
Sequência numerada. Para cada e-mail: **momento de envio**, **assunto**, **preheader** e **corpo**. No fim, orientação de agendamento (gatilho: carrinho abandonado; janelas de tempo) e um lembrete de ativar o 3º e-mail só com incentivo real.

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
