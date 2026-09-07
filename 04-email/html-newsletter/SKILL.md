---
name: html-newsletter
description: Monta um e-mail pronto (newsletter ou promoção) em texto e em HTML responsivo de colar na ferramenta de e-mail — assunto, prévia, cabeçalho, blocos de conteúdo e botão de CTA. Use ao disparar um comunicado, lançamento ou oferta para a base de contatos.
---

# HTML de Newsletter

## O que faz
Transforma um assunto solto ("quero avisar da coleção nova") em um e-mail completo: linha de assunto, texto de prévia (preheader), cabeçalho, corpo dividido em blocos e um botão de ação claro. Entrega em dois formatos — o texto para revisar e um HTML responsivo pronto para colar em Klaviyo, Mailchimp, RD Station, Brevo, ou onde a loja dispara.

## Quando usar
- Ao anunciar uma coleção, lançamento ou reposição para a base.
- Ao comunicar uma oferta real (data e condição definidas).
- Ao mandar um informativo periódico (novidades, conteúdo, bastidores).

## O que a IA precisa de você
- `[assunto do e-mail]` — o que você quer comunicar (ex.: chegou a coleção de inverno).
- `[objetivo]` — o que a pessoa deve fazer (ver a coleção, aproveitar a condição, ler o conteúdo).
- `[público]` — quem recebe (clientes que já compraram, lista geral, um segmento).
- `[tom da marca]` — como a loja fala (ex.: acolhedor e próximo / técnico e direto).
- `[produtos ou destaques]` — o que entra no e-mail (nomes, benefícios; preço só se for informar).
- `[link do botão]` — para onde o CTA leva.
- `[nome da loja]` e `[cor principal]` (opcional) — para o cabeçalho e o botão.

## Instruções (o cérebro da skill)
1. **Linha de assunto**: 3 opções, cada uma com até ~45 caracteres, claras sobre o conteúdo. Uma direta, uma curiosa, uma focada no benefício. Sem "imperdível", "última chance" ou caixa-alta gritada.
2. **Preheader** (texto de prévia): 1 frase de ~80 caracteres que complementa o assunto, nunca o repete.
3. **Cabeçalho**: nome da loja (ou logo) e, se fizer sentido, uma linha-título.
4. **Corpo em blocos** (2 a 4): cada bloco tem um subtítulo curto e 1–2 frases que começam pelo benefício para quem lê. Um bloco por ideia.
5. **CTA único e claro**: um botão com verbo de ação no tom da marca (ex.: "Ver a coleção", "Conferir agora"). Um CTA principal por e-mail.
6. **Rodapé**: assinatura da loja, motivo do recebimento e espaço para link de descadastro — obrigatório por boa prática e lei.
7. Monte o HTML com tabela, largura máxima de 600px, CSS inline e fontes seguras (Arial/Helvetica). Botão como link estilizado (bulletproof), imagens com `alt`. Deixe placeholders `[LINK]`, `[URL_IMAGEM]` e `{{ link_descadastro }}` para o lojista completar.
8. Qualquer preço, prazo, cupom ou condição que você não recebeu vira `[preencher]` — nunca invente valor.

## Regras de qualidade
- Um objetivo, um CTA principal. E-mail que pede tudo não converte nada.
- Sem "melhor do mundo", "imperdível", "explosão de vendas", urgência ou escassez inventada. Oferta real é informada, não gritada.
- Sem garantia de resultado.
- Benefício antes da característica. Frases curtas, legível no celular (a maioria abre no celular).
- O texto é da marca do lojista. A Performa não assina o e-mail.
- HTML enxuto: só tabela e CSS inline, nada de JavaScript (clientes de e-mail bloqueiam).

## Formato da saída
Entregue em duas partes:
1. **Versão texto** — assunto (3 opções), preheader, e o corpo do e-mail em blocos, para revisar antes.
2. **Versão HTML** — um bloco de código HTML completo (largura máx. 600px, responsivo, CSS inline), pronto para colar. Ao final, liste os placeholders que o lojista precisa trocar (`[LINK]`, `[URL_IMAGEM]`, preços marcados como `[preencher]`, link de descadastro).

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
