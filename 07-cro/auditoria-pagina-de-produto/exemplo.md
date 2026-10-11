# Auditoria de Página de Produto — exemplos reais

## Exemplo A — Só texto colado (muita coisa fica "não verificado")
Entrada:
```
Texto da página: título "Cafeteira CF-900 Inox". Descrição: "Cafeteira elétrica 900W, jarra 1,5L,
  sistema corta-pingo. Produto de alta qualidade." 3 bullets com especificações.
Fotos (descritas pelo lojista): 2 fotos em fundo branco, a cafeteira sozinha, de frente. Sem vídeo.
Público: casa e escritório pequeno · Preço: R$ 289 em até 6x · Frete e prazo: não informados
Prova: 12 avaliações, nota 4,7
Atendimento pergunta: "cabe quantas xícaras?", "desliga sozinha?", "a jarra é de vidro?"
```
Saída:
```
O que examinei: só o texto e a descrição das fotos. Não vi a página: layout, posição do botão,
zoom, celular e velocidade ficam NÃO VERIFICADOS.

Resumo: o sinal mais forte vem do atendimento — três perguntas que a página não responde (hipótese
de que isso trava compras, com evidência boa). Em segundo lugar, a página mostra pouco do produto.

Componente        | Status         | Evidência e local                      | O que fazer
Conteúdo/dúvidas  | observado      | atendimento repete 3 perguntas; texto  | responder na página: capacidade em
                  |                | não traz capacidade em xícaras,        | xícaras, desligamento automático e
                  |                | desligamento nem material da jarra     | material da jarra — SÓ com o dado do
                  |                |                                        | fabricante (hoje: pendência). → faq-do-produto
Identificação     | observado      | título "Cafeteira CF-900 Inox"         | incluir o que é e a capacidade confirmada
                  |                |                                        | (1,5 L). → titulo-que-rankeia
Descrição         | observado      | "alta qualidade" não informa nada      | trocar por fatos: 900 W, jarra 1,5 L,
                  |                |                                        | corta-pingo. → descricao-que-converte
Mídia             | observado*     | 2 fotos, produto isolado, sem escala   | incluir detalhe do corta-pingo, foto com
                  | (*pelo relato) |                                        | xícaras ao lado para escala. → frente 02
Prova             | observado      | 12 avaliações, 4,7                     | mostrar perto do nome, com acesso às notas
                  |                |                                        | e às críticas
Preço/frete       | hipótese       | frete e prazo não informados           | conferir se a página permite calcular frete
                  |                |                                        | sem atrito; prazo real: pendência
Layout e botão    | não verificado | sem print                              | enviar prints do celular e do computador
Velocidade        | não verificado | sem dados                              | pedir dados de campo, se houver

Fora, de propósito:
- Sugerir o título "Cafeteira 12 xícaras que mantém o café quente": ninguém sabe a capacidade em
  xícaras (é justamente a dúvida dos clientes) nem se ela mantém o café quente.
- "Selo de compra segura": só se a loja tiver um selo verdadeiro. Política de troca e contato
  visíveis dizem mais.
- "Foto é o que mais derruba conversão": não há dado aqui que mostre isso.

Plano
CORRIGIR JÁ: (1) responder as 3 dúvidas com dados do fabricante — impacto alto, esforço baixo,
  confiança média-alta; (2) descrição com fatos no lugar de "alta qualidade" — impacto médio,
  esforço baixo.
TESTAR (se houver tráfego): galeria com foto de escala e de uso × galeria atual. Hipótese: quem
  pergunta "quantas xícaras?" decide melhor vendo a escala. Métrica: taxa de carrinho. Proteção:
  devoluções.
Pendências: capacidade em xícaras, desligamento automático e material da jarra (fabricante);
  frete e prazo; prints da página.
Já está bom: preço e parcelamento claros; nota 4,7 real.
```

## Exemplo B — Prints do celular, dados do funil e queixa do atendimento
Entrada:
```
Produto: tênis casual (variantes de tamanho 37–44)
Dados de 30 dias: visualizações da página 10.000 (celular 7.000, computador 3.000);
  adicionar ao carrinho 451 (celular 217, computador 234)
Print do celular: o banner de cookies e a bolha do chat ficam sobre o botão "Adicionar"
Atendimento: "cliquei em comprar e não aconteceu nada"
Gravação (consentida): a pessoa clica em "Adicionar" sem escolher o tamanho e nada aparece
```
Saída:
```
O que examinei: print do celular, funil de 30 dias, relato do atendimento e uma gravação.
Não vi o computador nem dados de velocidade.

Taxas (com o denominador): carrinho ÷ visualizações = celular 217/7.000 = 3,1%; computador
234/3.000 = 7,8%. Antes de concluir, conferir se o evento de carrinho dispara uma vez por clique
e se o consentimento de cookies não está cortando dados do celular.

Componente        | Status    | Evidência e local                         | O que fazer
Botão (celular)   | observado | print: banner de cookies + bolha do chat  | tirar a sobreposição: o banner não pode
                  |           | cobrem o "Adicionar"                      | ficar fixo sobre o botão; mover a bolha
Retorno do clique | observado | gravação + atendimento: clicar sem        | mostrar "Escolha o tamanho" e levar até o
                  |           | tamanho não dá nenhum aviso               | seletor
Diferença celular | hipótese  | 3,1% × 7,8%; os dois defeitos acima       | depois de corrigir, comparar de novo
  × computador    |           | são do celular e explicam parte dela      | (amostra de 30 dias, mesmos canais)
Velocidade        | não verif.| sem dados de campo                        | medir antes de mexer

Plano
CORRIGIR JÁ (defeitos, sem teste): (1) sobreposição do botão no celular; (2) aviso "Escolha o
  tamanho". Impacto potencial alto (atinge 70% das visualizações), esforço baixo, confiança alta.
TESTAR depois: botão fixo na rolagem no celular. Hipótese: em página longa, o botão sempre visível
  ajuda quem já escolheu o tamanho. Métrica: taxa de carrinho no celular. Proteção: receita por
  visitante, acessibilidade (o botão fixo não pode cobrir conteúdo).
Depois de implantar: conferir que o evento de carrinho continua registrando, que nada quebrou no
  computador, e ter como voltar atrás.
```

> Referência: a auditoria diz o que examinou e não dá "OK" para o que não viu; cada achado tem
> status, evidência e local; nenhuma sugestão inventa capacidade, função, estatística ou selo; as
> taxas vêm com o denominador e a qualidade dos dados é conferida antes; e o defeito óbvio é
> corrigido já, enquanto a mudança de persuasão vai para teste.
