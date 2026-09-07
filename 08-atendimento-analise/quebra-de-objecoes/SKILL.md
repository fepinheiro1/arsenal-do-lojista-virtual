---
name: quebra-de-objecoes
description: Gera respostas para as objeções mais comuns na hora da compra — preço, frete, confiança e "vou pensar" — validando o cliente e reconduzindo à decisão sem pressão. Use quando o cliente hesita ou quase fecha e você quer responder de um jeito que conduz, não empurra.
---

# Quebra de Objeções

## O que faz
Transforma a hesitação do cliente em conversa. Para cada objeção comum — "está caro", "o frete é alto", "não conheço a loja", "vou pensar" — entrega uma resposta que valida o que a pessoa sentiu, explora o que está por trás e reconduz à decisão, sem pressionar e sem prometer o que a loja não pode cumprir.

## Quando usar
- No atendimento, quando o cliente levanta uma objeção antes de fechar.
- Para treinar a equipe de vendas/atendimento a responder sem partir para o desconto na hora.
- Para preparar respostas-padrão às dúvidas que mais travam a compra.

## O que a IA precisa de você
- `[objeção]` — o que o cliente disse (cole a fala dele, se tiver).
- `[produto / oferta]` — o que ele está avaliando.
- `[diferenciais reais]` — o que a loja de fato entrega (qualidade, garantia, atendimento, prazo). Só o que for verdade.
- `[tom da marca]` — como a loja fala.
- `[margem de negociação]` (opcional) — se há desconto/condição real disponível. Se não passar, a IA não inventa oferta.

## Instruções (o cérebro da skill)
Para cada objeção, responda no método **validar → explorar → reconduzir**, nunca "combater":

1. **Validar** — dê razão ao sentimento antes de qualquer argumento. "Faz sentido pensar no preço", "Comparar antes de decidir é o certo a fazer". Nunca contrarie de cara.
2. **Explorar** — uma pergunta que traz a real dúvida à tona. Preço → "caro comparado a quê?"; "vou pensar" → "o que ainda ficou em aberto pra você decidir?".
3. **Reconduzir** — traga o diferencial real que responde àquela dúvida específica, ligado ao que a pessoa quer. Termine com um convite calmo à decisão, sem "última chance" nem contagem regressiva.

Guias por objeção:
- **Preço ("está caro")**: nunca defenda o preço nem corra para o desconto. Reancore no valor e no custo de não resolver o problema. Desconto só se houver `[margem de negociação]` real.
- **Frete ("frete alto")**: reconheça, explique o que o frete garante (rastreio, prazo, segurança) e ofereça alternativa real se houver (retirada, outra transportadora, valor para frete grátis) — só se confirmado.
- **Confiança ("não conheço a loja")**: acolha a cautela e ofereça prova concreta e verificável (avaliações reais, política de troca, canais de contato, tempo de mercado). Nunca invente número de vendas ou avaliação.
- **"Vou pensar"**: não pressione. Descubra o que falta decidir e deixe a porta aberta com um próximo passo leve (tirar uma última dúvida, guardar o item, avisar quando voltar ao estoque).

## Regras de qualidade
- Objeção se conduz, não se combate. Validar sempre vem antes de argumentar.
- Proibido medo artificial, urgência falsa, escassez inventada ou "imperdível".
- Nunca invente prova social (número de vendas, avaliações) nem oferta — use `[preencher]` ou omita.
- Sem garantia de resultado. Fale em potencial e no que a loja de fato entrega.
- Desconto nunca é o primeiro recurso, e só aparece se houver margem real informada.
- Respeite o `[tom da marca]`. Tom calmo, de quem ajuda a decidir.

## Formato da saída
Para a objeção informada, entregue:
- **1 resposta pronta** (validar → explorar → reconduzir), no tom da marca.
- **A pergunta-chave** isolada, para o vendedor usar solta na conversa.
- **1 variação** mais curta para WhatsApp.

Se vierem várias objeções, repita o bloco para cada uma.

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
