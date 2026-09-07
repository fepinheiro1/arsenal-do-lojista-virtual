# Oferta e Pop-up de Saída — exemplo real

## Entrada
```
Produto/página: página de produto de uma loja de café especial em grãos.
Público: quem está conhecendo a loja pela primeira vez, ainda na dúvida.
Oferta real: cupom de 10% na primeira compra, em troca do e-mail.
Condições: válido por 7 dias após o cadastro, em pedidos acima de R$ 80.
Tom da marca: acolhedor, próximo, sem formalidade.
O que pedir em troca: e-mail.
```

## Saída
```
OFERTA ESCOLHIDA
Cupom de 10% na primeira compra em troca do e-mail. Cabe bem no momento de saída de
quem chegou agora: dá um empurrão concreto para experimentar a loja e abre um canal
de relacionamento, sem queimar margem em quem já ia comprar.

TEXTO DO POP-UP
Título:  Que tal levar o primeiro café com 10% off?
Apoio:   Deixe seu e-mail e a gente te manda um cupom de 10% para a primeira compra.
         Vale por 7 dias, em pedidos acima de R$ 80.
CTA:     Quero meu cupom
Saída:   Continuar navegando

VARIAÇÕES DE TÍTULO
A) Seu primeiro café com 10% de desconto — é só pegar o cupom.
B) Um mimo de boas-vindas: 10% na sua primeira compra.

NOTA DE CONFIGURAÇÃO
- Gatilho: intenção de saída (cursor indo para fechar a aba) ou inatividade.
- Onde exibir: primeira visita, uma vez por sessão. Não repetir para quem já pegou o cupom.
- Validade real: 7 dias · pedido mínimo R$ 80 — confirmar se segue valendo: [preencher]
- O cupom precisa estar ativo no sistema antes de publicar o pop-up.
```

> Referência: a oferta é real e cumprível, o texto convida em tom da marca ("um mimo
> de boas-vindas") sem culpa nem "última chance", a saída é digna ("Continuar
> navegando") e a validade verdadeira fica anotada com `[preencher]` para o lojista
> confirmar — oportunidade honesta, não desespero.
