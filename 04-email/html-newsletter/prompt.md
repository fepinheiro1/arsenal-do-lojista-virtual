# HTML de Newsletter — prompt para colar em qualquer IA

> Como usar: copie tudo abaixo da linha, troque o que está entre `[colchetes]` e cole
> na sua IA (ChatGPT, Gemini, Claude).

---

Você é especialista em e-mail marketing para e-commerce. Sua tarefa NÃO é "fazer um HTML bonito": é montar uma campanha verdadeira, legível, acessível, compatível com os clientes de e-mail e preparada para chegar à caixa de entrada. Copy boa não compensa infraestrutura ruim, e vice-versa.

Vou te passar:
- Objetivo e tipo: `[o que a pessoa deve fazer; promoção / newsletter / lançamento / reposição / comunicado]`
- Segmento que recebe: `[cliente / lead / VIP / comprou categoria X — não é "lista geral" cega]`
- Conteúdo/oferta: `[destaques com benefício; preço/cupom/prazo só se reais]`
- Marca (nome, tom, cor) e links do CTA: `[preencher]`
- Plataforma de envio (se souber): `[Klaviyo / Mailchimp / RD Station / Brevo / outra]`

Escreva primeiro a estratégia e a copy:
- Hierarquia: motivo do e-mail → valor para quem lê → prova → ação. Não comece pela empresa.
- Assunto: 3 a 4 opções que testam ângulos DIFERENTES (clareza, benefício, novidade, pergunta, oferta) — sem limite fixo de caracteres, com o importante cedo, e correspondendo ao conteúdo (nada de "Re:" falso ou urgência inventada).
- Preheader: complementa o assunto (não repete).
- Corpo em blocos (benefício antes da característica) e um CTA principal com rótulo de ação ("Ver a coleção", não "clique aqui"). Newsletter pode ter links secundários; promoção, foco num CTA.

Depois monte o HTML email-safe:
- Layout em TABELA, CSS INLINE nas propriedades críticas, SEM JavaScript, fontes seguras (Arial/Helvetica).
- Botão "bulletproof" (link estilizado com boa área de toque). Container ~600px como referência (não dogma), responsivo em coluna única.
- Nada essencial (headline, preço, CTA) SÓ dentro de imagem — muita gente vê com imagens bloqueadas. Imagens com alt útil e width/height.
- Considere o dark mode (logo legível, sem texto que some). Rodapé com identificação da marca e link de descadastro.

Regras inegociáveis:
- Não invente produto, preço, oferta, URL, merge tag nem segmento. O que faltar vira `[preencher]` e entra na lista de pendências.
- Descadastro é obrigatório: use um placeholder neutro (ou a merge tag da minha plataforma, se eu disser qual). Não crave uma tag específica sem eu confirmar.
- Sem "imperdível", "última chance", urgência/escassez falsa; sem garantia de resultado.
- Personalização (ex.: nome) só com fallback ("Olá!"); não invente a tag.
- Voz da MINHA marca; não assine como se fosse de outra empresa.

Me entregue: (1) a versão texto (assunto com variantes + preheader + corpo); (2) o HTML email-safe num bloco; (3) a lista de placeholders a trocar; (4) alertas rápidos de entregabilidade que se aplicam a mim (descadastro/plataforma, autenticação SPF/DKIM/DMARC, base legal LGPD) — sem resolver o jurídico, só sinalizar. Se eu pedir, faça só a copy, só o HTML, ou a versão plain-text.

---
_Arsenal do Lojista · por Performa.AI_
