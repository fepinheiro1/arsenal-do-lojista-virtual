---
name: texto-de-retargeting
description: Escreve copy de retargeting para quem já visitou a loja, viu um produto ou abandonou o carrinho — no tom de quem já conhece a marca, tratando a objeção que travou a compra em vez de reapresentar tudo do zero. Use para campanhas de remarketing no Facebook e Instagram por estágio do funil.
---

# Texto de Retargeting

## O que faz
Cria anúncios para **quem já esteve na sua loja** — visitou a página, olhou um produto ou deixou o carrinho cheio e saiu. Essa pessoa não precisa ser apresentada à marca de novo; ela precisa de um empurrão que resolva o que a fez hesitar. A skill escreve a copy no tom de "você já nos conhece" e mira na **objeção real** de cada estágio, não numa oferta genérica.

## Quando usar
- Você vai montar campanhas de remarketing (públicos personalizados: visitantes do site, quem viu produto, quem adicionou ao carrinho, quem iniciou o checkout).
- O tráfego chega mas muita gente sai sem comprar, e você quer reconquistar quem já demonstrou interesse.
- Após uma campanha de aquisição, para trabalhar quem foi impactado mas não converteu.

## O que a IA precisa de você
- `[produto ou loja]` — o que a pessoa viu (um produto específico ou a loja em geral).
- `[estágio]` — em que ponto ela parou: visitou o site / viu o produto / abandonou o carrinho / iniciou o checkout. Pode pedir mais de um.
- `[objeção provável]` — o que costuma travar a compra (frete, preço, dúvida de tamanho, confiança, "vou pensar"). Se não souber, a skill sugere as mais comuns do estágio.
- `[argumentos reais que respondem à objeção]` — frete grátis acima de X, troca facilitada, garantia, prova social, parcelamento. Só o que for verdade; sem dado, marca `[preencher]`.
- `[tom da marca]` — como a loja fala.

## Instruções (o cérebro da skill)
Para **cada estágio** pedido, entregue um bloco com **texto principal, título e botão**, seguindo a lógica do funil:

1. **Reconheça sem constranger.** Fale como quem continua uma conversa, de leve — nunca cobre ("você esqueceu", "você abandonou", "você deixou pra trás"). Retomar é convite, não bronca.
2. **Trate a objeção do estágio**, do topo para o fundo:
   - **Visitou o site / viu a categoria** → reforça o posicionamento e o benefício central da loja; ainda é sobre desejo e confiança.
   - **Viu um produto específico** → traz de volta aquele produto, responde a dúvida mais provável (tamanho, uso, material) e adiciona prova.
   - **Abandonou o carrinho** → foca em remover o atrito final: frete, prazo, segurança da compra, parcelamento — o que estava faltando decidir.
   - **Iniciou o checkout** → o empurrão mais direto e curto; a pessoa estava a um clique. Reforça segurança e a facilidade de concluir.
3. **Use a proximidade a favor:** copy mais curta que a de aquisição, tom mais direto, benefício-chave logo na 1ª linha (a pessoa já sabe o que é).
4. **Ofereça um incentivo só se ele for real e autorizado pelo lojista.** Nunca crie cupom, desconto ou frete grátis por conta própria — se não veio nos dados, marque `[preencher: incentivo, se houver]` e escreva a versão sem depender dele.

## Regras de qualidade
- Persuasão ética: sem "melhor do mundo", "imperdível", "última chance", contagem regressiva falsa, "seu carrinho expira em 1h" inventado, ou garantia de resultado.
- **Nunca culpar nem envergonhar** quem não comprou. Nada de "você desistiu", "não perca de novo", "ainda está aí parado". Tom de reencontro, não de cobrança.
- Nenhum incentivo, desconto ou prazo inventado — dado real ou `[preencher]`.
- Respeite a privacidade: não dê a entender vigilância ("vimos que você olhou 3 vezes"). Retargeting é lembrete gentil, não perseguição.
- A voz é da marca do lojista. A Performa não aparece na copy.

## Formato da saída
Um bloco por estágio, na ordem do funil, cada um com: **Estágio + objeção mirada** · Texto principal · Título · Botão. Se houver mais de uma objeção forte no mesmo estágio, ofereça 2 variações.

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
