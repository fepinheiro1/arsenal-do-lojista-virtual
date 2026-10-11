# Otimização de Checkout — exemplos reais

## Exemplo A — Auditoria por descrição (relato, não navegação)
Entrada:
```
Fluxo (descrito pelo lojista): 4 telas — (1) criar conta obrigatório, (2) endereço, (3) frete,
  (4) pagamento
Campos: nome, e-mail, CPF, RG, telefone, data de nascimento, endereço completo
Frete: só aparece na tela 3. Frete grátis acima de R$ 199 (regiões: não informado)
Pagamento: só cartão de crédito · Plataforma: Nuvemshop (gateway: não informado)
Atendimento: clientes reclamam "não tem Pix"
```
Saída:
```
O que examinei: só a descrição do lojista. Não naveguei pelo checkout: tudo abaixo é relato ou
hipótese. Prints do celular confirmariam vários pontos.

Etapa      | Achado                          | Evidência          | Gravid. | Ação                                   | Depende de
Pagamento  | sem Pix; clientes pedem         | relatado (atend.)  | alta    | ver se o gateway atual oferece Pix na  | gateway/
           |                                 |                    |         | Nuvemshop; se não, avaliar trocar      | plataforma
Frete      | custo só aparece na tela 3,     | relatado (lojista) | alta    | mostrar estimativa de frete e prazo    | plataforma
           | depois de preencher tudo        |                    |         | cedo (no carrinho), dizendo que depende|
           |                                 |                    |         | do CEP                                 |
Frete grátis| regra de R$ 199, regiões      | relatado           | média   | confirmar regiões e exclusões antes de | lojista
           | desconhecidas                   |                    |         | mostrar "faltam R$ X"                  |
Conta      | criação obrigatória             | relatado           | média   | ativar compra como convidado, se nada  | plataforma
           |                                 |                    |         | na operação exigir conta               |
Campos     | RG e data de nascimento         | relatado           | média   | PERGUNTAR por que são pedidos (gateway,| lojista/
           |                                 |                    |         | antifraude, produto com restrição de   | gateway
           |                                 |                    |         | idade?). Só remover se não houver motivo|
Celular, erros, acessibilidade | não verificado | —              | —       | enviar prints do celular               | lojista

Se o Pix entrar, o fluxo precisa de: prazo de expiração real exibido, QR e copia-e-cola, caminho
de volta à loja e o pedido tratado como PENDENTE até o pagamento ser confirmado.

Fora, de propósito:
- "Adicionar Pix — esforço baixo na Nuvemshop": depende do gateway e do plano; conferir antes.
- "Juntar endereço e frete numa tela" como regra: menos telas não é automaticamente melhor. Pode
  virar teste.
- "Selo de compra segura": só se houver um verdadeiro.
- E-mail "seu carrinho está guardado": só se a plataforma reserva o carrinho. A mensagem de
  recuperação fica com a recuperacao-de-carrinho (frente 04).

Plano
Ajustes rápidos: compra como convidado; estimativa de frete cedo (se a Nuvemshop/tema permitir).
Projeto: Pix (gateway). Investigar: RG e data de nascimento.
Medir depois: início do checkout → pagamento iniciado → pedido criado → pagamento aprovado.
```

## Exemplo B — Diagnóstico com números (que não batem entre si)
Entrada:
```
30 dias. Plataforma: 820 pedidos criados (Pix 380, cartão 440)
Gateway: 700 pagamentos aprovados (Pix 260, cartão 440); 150 tentativas de cartão recusadas
  (não viraram pedido); 120 Pix expiraram sem pagamento
GA4: 610 eventos de compra (disparam na página de "obrigado")
```
Saída:
```
Primeiro, reconciliar: 610 (GA4) × 820 (pedidos criados) × 700 (pagos). São três definições:
- "Pedido criado" inclui Pix que nunca foi pago. Venda é o APROVADO: 700.
- O evento do GA4 dispara na página de "obrigado". Quem paga o Pix no app do banco e não volta,
  quem bloqueia cookies ou volta de um gateway em outro domínio não é contado. E ele pode estar
  contando Pix pendente como compra. Conferir onde e quando o evento dispara antes de usar o GA4
  como verdade.

Achados (medido, pelas fontes acima)
1. Pix: 120 de 380 cobranças expiraram (32%). Medido. Hipóteses: prazo de expiração curto ou pouco
   visível, instrução confusa, falta de caminho de volta. Validar: tempo de expiração real e teste
   com usuários no celular. Um lembrete honesto antes de expirar fica com a recuperacao-de-carrinho.
2. Cartão: 150 recusas em 590 tentativas (25%). Medido, mas a causa não: separar pelos códigos do
   gateway (emissor, antifraude, dado inválido) antes de agir. Não contornar o antifraude. Depois
   de uma recusa, oferecer tentar de novo ou pagar com Pix, sem perder o carrinho e sem cobrar
   duas vezes.
3. Medição: o GA4 subconta e mistura pendentes. Corrigir o evento para refletir a aprovação e
   checar a deduplicação.

Prioridade: (1) e (2) são falhas, não desistência — vêm antes de qualquer teste de layout.
Proteção ao mudar algo: taxa de aprovação, fraude, chamados no atendimento.
Sem "vai aumentar X%": medir de novo em 30 dias, com as mesmas definições.
```

> Referência: a auditoria diz que trabalhou com relato e não finge ter navegado; investiga por que
> um campo é pedido antes de mandar remover; não promete capacidade da plataforma; trata Pix
> pendente como não pago; separa desistência de falha de pagamento; reconcilia GA4, plataforma e
> gateway antes de concluir; e não cria reserva nem selo que não existem.
