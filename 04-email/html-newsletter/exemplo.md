# HTML de Newsletter — exemplos ilustrativos

> Casos de demonstração: o e-mail só descreve o que veio na entrada — e todo item da entrada aparece.

## Exemplo A — Campanha completa (newsletter de produto)
Entrada:
```
Objetivo/tipo: levar à página da coleção / newsletter editorial de produto
Segmento: clientes que já compraram café na loja
Conteúdo: 3 grãos novos (Cerrado, Sul de Minas, Chapada) — notas de sabor diferentes
  (as notas de cada um ainda não vieram)
Marca: Café da Serra, tom próximo/barista, cor #6B4226
Link do CTA: https://cafedaserra.com.br/origem-unica
Plataforma: não informada
```
Saída:
```
VERSÃO TEXTO

Assunto (variantes por ângulo):
- (clareza)    Três origens novas na sua próxima xícara
- (benefício)  Compare três cafés e ache o seu preferido
- (pergunta)   Você sente a diferença de onde o café nasce?
- (novidade)   Chegaram: Cerrado, Sul de Minas e Chapada

Preheader (complementa, não repete): Cada origem tem um sabor — dá para provar e comparar em casa.

Corpo:
- Cada origem, um sabor — O solo, a altitude e o clima mudam o que você sente na xícara.
  Trouxemos três origens para você comparar em casa.
- Cerrado — [notas de sabor do Cerrado]
- Sul de Minas — [notas de sabor do Sul de Minas]
- Chapada — [notas de sabor da Chapada]
- Escolha pela sua manhã — Prove, compare e fique com o que combina com o seu ritmo.

CTA: Conhecer as origens
```
As notas de sabor de cada café não vieram — ficam como placeholder (não invento "achocolatado"
ou "floral": é a ficha do torrador que diz). Também não completei "Cerrado Mineiro" nem
"Chapada Diamantina": existe mais de uma região com esses nomes.
```html
<table role="presentation" width="100%" cellpadding="0" cellspacing="0" style="background:#f4f1ec;margin:0;padding:24px 0;">
  <tr><td align="center">
    <table role="presentation" width="600" cellpadding="0" cellspacing="0" style="max-width:600px;width:100%;background:#ffffff;font-family:Arial,Helvetica,sans-serif;">
      <tr><td style="background:#6B4226;padding:20px 24px;text-align:center;">
        <span style="color:#ffffff;font-size:20px;font-weight:bold;">Café da Serra</span>
      </td></tr>
      <tr><td>
        <img src="[URL_IMAGEM]" alt="Três pacotes de café: Cerrado, Sul de Minas e Chapada" width="600" height="400" style="width:100%;height:auto;display:block;">
      </td></tr>
      <tr><td style="padding:28px 24px 8px 24px;">
        <h1 style="margin:0 0 8px 0;font-size:22px;color:#2b2b2b;">Cada origem, um sabor</h1>
        <p style="margin:0;font-size:16px;line-height:1.5;color:#4a4a4a;">O solo, a altitude e o clima mudam o que você sente na xícara. Trouxemos três origens para você comparar em casa.</p>
      </td></tr>
      <tr><td style="padding:12px 24px;">
        <h2 style="margin:0 0 6px 0;font-size:17px;color:#6B4226;">Cerrado</h2>
        <p style="margin:0;font-size:16px;line-height:1.5;color:#4a4a4a;">[NOTAS_CERRADO]</p>
      </td></tr>
      <tr><td style="padding:12px 24px;">
        <h2 style="margin:0 0 6px 0;font-size:17px;color:#6B4226;">Sul de Minas</h2>
        <p style="margin:0;font-size:16px;line-height:1.5;color:#4a4a4a;">[NOTAS_SUL_DE_MINAS]</p>
      </td></tr>
      <tr><td style="padding:12px 24px 4px 24px;">
        <h2 style="margin:0 0 6px 0;font-size:17px;color:#6B4226;">Chapada</h2>
        <p style="margin:0;font-size:16px;line-height:1.5;color:#4a4a4a;">[NOTAS_CHAPADA]</p>
      </td></tr>
      <tr><td style="padding:24px;text-align:center;">
        <a href="https://cafedaserra.com.br/origem-unica" style="background:#6B4226;color:#ffffff;text-decoration:none;font-size:16px;font-weight:bold;padding:14px 32px;border-radius:6px;display:inline-block;">Conhecer as origens</a>
      </td></tr>
      <tr><td style="padding:20px 24px;background:#f4f1ec;text-align:center;">
        <p style="margin:0 0 6px 0;font-size:12px;color:#6b6b6b;">Café da Serra · [ENDEREÇO_POSTAL, se a sua plataforma exigir]</p>
        <p style="margin:0;font-size:12px;color:#6b6b6b;">Você recebe este e-mail porque já comprou com a gente.<br><a href="[LINK_DESCADASTRO]" style="color:#6b6b6b;">Descadastrar</a></p>
      </td></tr>
    </table>
  </td></tr>
</table>
```
A headline "Cada origem, um sabor" e o CTA estão em TEXTO (não dentro da imagem) — o e-mail se
entende mesmo com as imagens bloqueadas. As cores do rodapé foram escurecidas para o texto não
sumir no dark mode.
```
PLAIN-TEXT (alternativa text/plain)
Cada origem, um sabor.
O solo, a altitude e o clima mudam o que você sente na xícara. Três origens para comparar em casa:
- Cerrado: [notas]
- Sul de Minas: [notas]
- Chapada: [notas]
Conheça as origens: https://cafedaserra.com.br/origem-unica
Você recebe porque já comprou com a gente. Descadastrar: [LINK_DESCADASTRO]

PLACEHOLDERS A TROCAR (o link do CTA já entrou, porque veio na entrada)
- [NOTAS_CERRADO] / [NOTAS_SUL_DE_MINAS] / [NOTAS_CHAPADA] → as notas de sabor da ficha de cada
  café (no HTML e no plain-text)
- [URL_IMAGEM] → foto dos três cafés (ajuste a altura à foto real, ou remova o bloco de imagem)
- [LINK_DESCADASTRO] → a merge tag de descadastro da sua ferramenta (Klaviyo/Mailchimp/RD/Brevo)
- [ENDEREÇO_POSTAL] → só se a sua plataforma/lista exigir endereço no rodapé

ALERTAS DE ENTREGABILIDADE (sinalização, não configuração)
- Descadastro real é obrigatório — troque o placeholder pela tag da sua plataforma antes de enviar.
- Confirme SPF, DKIM e DMARC do seu domínio; sem isso a entrega sofre (é no provedor/plataforma,
  não neste HTML).
- Envie só para quem tem base legal para receber (cliente/consentimento). Lista comprada
  dificilmente tem base legal na LGPD — e queima a reputação do domínio.
- Ao medir, olhe cliques e vendas, não só a taxa de abertura (o Apple Mail infla as aberturas).
```

## Exemplo B — Auditar entregabilidade (por que cai no spam)
Entrada:
```
Meus e-mails estão caindo no spam. Uso a palavra "grátis" no assunto, será que é isso?
```
Saída:
```
"Grátis" no assunto quase nunca é o motivo — isso é um mito. Spam moderno depende de reputação,
autenticação e engajamento, não de palavras isoladas. O que realmente pesa:

1. Autenticação (o primeiro a conferir): SPF, DKIM e DMARC do seu domínio de envio. Para quem
   envia em volume, Gmail e Yahoo exigem autenticação e DMARC (regra em vigor desde 2024 — confira
   o limite e os requisitos atuais); sem isso, a entrega cai. Resolve-se na plataforma e no DNS,
   não no HTML.
2. Descadastro: precisa de um link real e fácil (e, em volume, o de um clique). Sem ele, as
   reclamações sobem e a reputação cai.
3. Conteúdo: e-mail só de imagem com pouco texto tende a cair; link encurtado suspeito também.
   Garanta texto real e links do seu próprio domínio.
4. Engajamento: mandar para base antiga/fria derruba tudo. Limpe os inativos.

Pode continuar com "grátis" no assunto se o conteúdo cumprir o que promete — o que pesa é o resto.
```

> Referência: as três camadas (estratégia, copy, HTML email-safe) mais a de entregabilidade;
> o essencial fora da imagem, descadastro como placeholder neutro, plain-text incluído, os três
> cafés presentes sem nota de sabor inventada, e os alertas técnicos SINALIZADOS (com "confira a
> regra vigente") — sem a skill fingir que configura DNS ou resolve o jurídico.
