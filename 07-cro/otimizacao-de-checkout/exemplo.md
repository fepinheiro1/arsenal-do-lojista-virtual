# Otimização de Checkout — exemplo real

## Entrada
```
Fluxo atual: 4 telas — (1) criar conta obrigatório, (2) endereço, (3) frete, (4) pagamento.
Campos do formulário: nome, e-mail, CPF, RG, telefone, data de nascimento, endereço completo.
Frete: só aparece na tela 3, depois de já ter cadastrado tudo. Frete grátis acima de R$ 199.
Meios de pagamento: só cartão de crédito.
Plataforma: Nuvemshop.
Onde abandona: não tenho o número, mas o suporte diz que reclamam "não tem Pix".
```

## Saída
```
RESUMO
O maior vazamento está no pagamento (só cartão, sem Pix) e no frete que só aparece
na tela 3, depois de a pessoa preencher tudo. Somados a conta obrigatória e campos
demais, esses pontos empurram a desistência antes do "confirmar".

TABELA
Ponto                 | Atrito encontrado                          | Correção
Número de etapas      | 4 telas, uma só para criar conta           | Juntar endereço+frete numa tela; remover a etapa de conta
Login obrigatório     | Exige criar conta antes de comprar         | Ativar compra como convidado; oferecer conta no fim (opcional)
Campos do formulário  | Pede RG e data de nascimento sem necessidade | Manter nome, CPF, e-mail, telefone e endereço; cortar RG e nascimento; autopreencher endereço pelo CEP
Frete                 | Só aparece na tela 3                        | Calcular frete no carrinho; mostrar "faltam R$ X para o frete grátis"
Meios de pagamento    | Só cartão de crédito                        | Adicionar Pix (na Nuvemshop, via gateway já integrado) e boleto; deixar parcelamento claro: [preencher condições]
Custo total           | Total só na última tela                     | Mostrar subtotal + frete no carrinho, antes de iniciar o checkout
Confiança no pagamento| Sem selo/política visível                   | Exibir selo de compra segura e prazo de troca: [preencher]
Erros e recuperação   | Sem lembrete de carrinho                    | Ativar e-mail de carrinho abandonado como convite ("seu carrinho está guardado"), sem contador falso

PLANO PRIORIZADO
1. Adicionar Pix como meio de pagamento (impacto alto · esforço baixo na Nuvemshop)
2. Mostrar frete já no carrinho + "faltam R$ X para o grátis" (impacto alto · esforço baixo)
3. Ativar compra como convidado (impacto alto · esforço baixo)
4. Cortar RG e data de nascimento; autopreencher endereço pelo CEP (impacto médio · esforço baixo)
5. Juntar endereço e frete numa etapa (impacto médio · esforço médio)
6. E-mail de carrinho abandonado como convite honesto (impacto médio · esforço médio)
7. Selo de segurança e política de troca visíveis [preencher] (impacto médio · esforço baixo)
```

> Referência: ataca primeiro o que mais pesa no abandono (Pix e frete cedo), respeita
> o que a Nuvemshop permite, transforma o lembrete de carrinho em convite sem culpa
> nem contador falso, e marca `[preencher]` nas condições de parcelamento e política
> que o lojista não informou.
