# Oferta e Pop-up de Saída — exemplos reais

## Exemplo A — Exibir, com consentimento separado e grupo de controle
Entrada:
```
Página: produto, numa loja de café especial em grãos · Objetivo: primeira compra
O que se sabe: muitos visitantes novos saem da página de produto (dado da loja, sem detalhe)
Oferta real: 10% na primeira compra, válido por 7 dias após o cadastro, pedidos acima de R$ 80
O que pede: e-mail — e a loja quer mandar novidades depois
Automação: a sequência de boas-vindas por e-mail também oferece 10% no primeiro e-mail
Tom: acolhedor, próximo
```
Saída:
```
Decisão: EXIBIR, como teste, só para visitantes novos na página de produto. Não aparece no
carrinho nem no checkout. É hipótese: falta saber se o pop-up gera compra a mais ou só dá
desconto para quem já compraria — por isso o teste abaixo.

Conflito resolvido: a sequência de boas-vindas já dá 10%. O pop-up passa a ser a PORTA de entrada
dessa sequência (o cupom chega no 1º e-mail) — um só cupom, não dois.

Quem vê: primeira visita, sem compra anterior conhecida. Não vê de novo quem se cadastrou, quem
usou o cupom ou quem fechou o pop-up nos últimos 30 dias (intervalo como hipótese). Uma vez por
visitante.
Gatilho: computador → cursor saindo da janela (sinal imperfeito) depois de 20 s na página.
  Celular → não existe intenção de saída confiável: slide-in discreto no rodapé após rolar 60% da
  página, sem cobrir o botão de compra.

Texto
Título: Que tal levar o primeiro café com 10% de desconto?
Apoio:  Deixe seu e-mail e enviamos o cupom de 10% para a primeira compra. Vale por 7 dias, em
        pedidos acima de R$ 80.
Botão:  Quero meu cupom
Recusa: Continuar navegando
[ ] Também quero receber novidades e promoções por e-mail  (desmarcada; o cupom chega com ou sem)
Variações de título: (A) Seu primeiro café com 10% de desconto · (B) Boas-vindas: 10% na sua
  primeira compra

Fechar: "×" visível, funciona no toque, no teclado e no Esc; o foco volta para a página ao fechar.

Medição: 50% dos visitantes novos elegíveis veem o pop-up e 50% não veem (sorteio fixo por
  visitante), por pelo menos 2 semanas inteiras. Métrica principal: receita por visitante, já
  descontado o cupom. Proteção: rejeição, descadastros, e quantos dos cupons foram usados por quem
  compraria de qualquer jeito (comparando com o grupo sem pop-up).

Fora, de propósito: "sem queimar margem em quem já ia comprar" — é exatamente o que o grupo sem
pop-up vai mostrar.
Pendências: cupom ativo e testado no sistema; confirmar que a validade de 7 dias é contada no fuso
da loja.
```

## Exemplo B — Recomendar NÃO exibir
Entrada:
```
O lojista quer, no CHECKOUT:
"ESPERA! 15% OFF só pra você — oferta expira em 10:00" (o contador reinicia a cada visita)
Botões: "Quero o desconto" / "Não, prefiro pagar mais caro"
Motivo: "muita gente sai no checkout"
```
Saída:
```
Decisão: NÃO EXIBIR. Quatro motivos:
1. Checkout é o ponto mais quente da compra. Interromper ali pode atrapalhar quem ia concluir.
2. O contador que reinicia é falso, e "prefiro pagar mais caro" é uma recusa humilhante. Os dois
   são padrões manipuladores.
3. 15% para quem chega ao checkout ensina o cliente a começar a compra e sair para ganhar desconto,
   e dá desconto para quem já ia pagar o preço cheio.
4. No celular não existe "intenção de saída" confiável. O pop-up apareceria em momentos
   aleatórios.

No lugar:
- Descobrir POR QUE saem do checkout: frete que aparece tarde, falta de Pix, erro de pagamento?
  → otimizacao-de-checkout.
- No carrinho (não no checkout), um bloco fixo com frete, prazo e política de troca reais.
- Para quem saiu de fato, a mensagem certa é a da recuperacao-de-carrinho (frente 04), sem cupom
  por padrão.
```

> Referência: a decisão vem antes do texto (e "não exibir" é resposta válida); o gatilho é honesto
> por dispositivo; quem já converteu ou recusou não vê de novo; a oferta é real e não duplica a das
> outras automações; o consentimento para marketing é separado; fechar é fácil e acessível; e o
> resultado se mede contra um grupo sem pop-up.
