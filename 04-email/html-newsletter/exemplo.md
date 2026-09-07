# HTML de Newsletter — exemplo real

## Entrada
```
Assunto: chegou a linha de café especial de origem única
Objetivo: levar para a página da coleção
Público: clientes que já compraram café na loja
Tom da marca: próximo, cuidadoso, meio conversa de barista
Destaques: 3 grãos novos (Cerrado, Sul de Minas, Chapada) — notas de sabor diferentes
Preço/condição: não informado
Link do botão: https://cafedaserra.com.br/origem-unica
Nome da loja: Café da Serra
Cor principal: #6B4226
```

## Saída

**Versão texto**

Assunto (3 opções):
- A) Três origens novas na sua próxima xícara
- B) Você sente a diferença de onde o café nasce?
- C) Café de origem única, escolhido grão a grão

Preheader: Cerrado, Sul de Minas e Chapada — cada um com um sabor pra chamar de seu.

Corpo:
- **Cada origem, um sabor** — Café não é tudo igual. O solo, a altitude e o clima mudam o que você sente na xícara. Trouxemos três origens para você comparar em casa.
- **Cerrado Mineiro** — Encorpado e achocolatado, para quem gosta de um café que preenche a manhã.
- **Chapada Diamantina** — Mais leve e floral, bom para a tarde sem pesar.
- **Escolha pela sua manhã** — Não precisa decidir tudo hoje. Prove, compare e fique com o que combina com o seu ritmo.

CTA: Conhecer as origens

Rodapé: Café da Serra · Você recebe este e-mail porque já comprou com a gente. · [link de descadastro]

**Versão HTML**
```html
<table role="presentation" width="100%" cellpadding="0" cellspacing="0" style="background:#f4f1ec;margin:0;padding:24px 0;">
  <tr>
    <td align="center">
      <table role="presentation" width="600" cellpadding="0" cellspacing="0" style="max-width:600px;width:100%;background:#ffffff;font-family:Arial,Helvetica,sans-serif;">
        <!-- Cabeçalho -->
        <tr>
          <td style="background:#6B4226;padding:20px 24px;text-align:center;">
            <span style="color:#ffffff;font-size:20px;font-weight:bold;letter-spacing:0.5px;">Café da Serra</span>
          </td>
        </tr>
        <!-- Imagem topo (opcional) -->
        <tr>
          <td>
            <img src="[URL_IMAGEM]" alt="Três pacotes de café de origem única" width="600" style="width:100%;height:auto;display:block;">
          </td>
        </tr>
        <!-- Bloco 1 -->
        <tr>
          <td style="padding:28px 24px 8px 24px;">
            <h1 style="margin:0 0 8px 0;font-size:22px;color:#2b2b2b;">Cada origem, um sabor</h1>
            <p style="margin:0;font-size:16px;line-height:1.5;color:#4a4a4a;">Café não é tudo igual. O solo, a altitude e o clima mudam o que você sente na xícara. Trouxemos três origens para você comparar em casa.</p>
          </td>
        </tr>
        <!-- Bloco 2 -->
        <tr>
          <td style="padding:12px 24px;">
            <h2 style="margin:0 0 6px 0;font-size:17px;color:#6B4226;">Cerrado Mineiro</h2>
            <p style="margin:0;font-size:16px;line-height:1.5;color:#4a4a4a;">Encorpado e achocolatado, para quem gosta de um café que preenche a manhã.</p>
          </td>
        </tr>
        <!-- Bloco 3 -->
        <tr>
          <td style="padding:12px 24px 4px 24px;">
            <h2 style="margin:0 0 6px 0;font-size:17px;color:#6B4226;">Chapada Diamantina</h2>
            <p style="margin:0;font-size:16px;line-height:1.5;color:#4a4a4a;">Mais leve e floral, bom para a tarde sem pesar.</p>
          </td>
        </tr>
        <!-- CTA -->
        <tr>
          <td style="padding:24px;text-align:center;">
            <a href="[LINK]" style="background:#6B4226;color:#ffffff;text-decoration:none;font-size:16px;font-weight:bold;padding:14px 32px;border-radius:6px;display:inline-block;">Conhecer as origens</a>
          </td>
        </tr>
        <!-- Rodapé -->
        <tr>
          <td style="padding:20px 24px;background:#f4f1ec;text-align:center;">
            <p style="margin:0 0 6px 0;font-size:12px;color:#8a8a8a;">Café da Serra</p>
            <p style="margin:0;font-size:12px;color:#8a8a8a;">Você recebe este e-mail porque já comprou com a gente.<br><a href="{{ link_descadastro }}" style="color:#8a8a8a;">Descadastrar</a></p>
          </td>
        </tr>
      </table>
    </td>
  </tr>
</table>
```

Placeholders para trocar antes de enviar:
- `[LINK]` → https://cafedaserra.com.br/origem-unica
- `[URL_IMAGEM]` → imagem dos três cafés (ou remova o bloco de imagem)
- `{{ link_descadastro }}` → tag de descadastro da sua ferramenta de e-mail

> Referência: um só objetivo e um só CTA, benefício antes da característica, HTML de tabela com CSS inline e largura de 600px que abre bem no celular, zero urgência falsa, e nenhum preço inventado (não foi informado, então não apareceu).
