# Auditoria de Página de Produto — exemplo real

## Entrada
```
Conteúdo da página: Título "Cafeteira CF-900 Inox". Descrição: "Cafeteira elétrica
  900W, jarra 1,5L, sistema corta-pingo. Produto de alta qualidade." 3 bullets com specs.
Fotos: 2 fotos com fundo branco, a cafeteira sozinha, de frente. Sem vídeo.
Produto e público: cafeteira elétrica de filtro, para casa/escritório pequeno.
Preço e condições: R$ 289 em até 6x. Frete e prazo: [preencher]
Prova social: 12 avaliações, média 4,7. Sem depoimentos escritos.
Dúvidas do atendimento: "cabe quantas xícaras?", "desliga sozinha?", "a jarra é de vidro?"
```

## Saída
```
RESUMO
A página tem preço claro e boa nota de avaliação, mas perde venda em três frentes:
foto que não mostra o produto em uso, título sem benefício e dúvidas de compra que
a página não responde. A maior alavanca aqui é a foto — é o item que mais segura a
decisão neste tipo de produto.

TABELA
Ponto             | Status   | Observação                              | O que fazer
Título            | Ajustar  | Só diz o que é, não o ganho             | "Cafeteira 12 xícaras que mantém o café quente — CF-900 Inox 1,5L"
Fotos e vídeo     | Falta    | 2 fotos, produto isolado, sem escala    | Adicionar: cafeteira na bancada, café sendo servido, detalhe do corta-pingo, foto com xícaras ao lado para dar escala
Primeira dobra    | OK       | Nome, preço e foto aparecem juntos      | Manter; garantir botão visível sem rolar
Descrição/bullets | Ajustar  | "alta qualidade" não diz nada           | Trocar por benefício: "Serve a mesa toda numa leva — jarra de 1,5L"
Prova social      | Ajustar  | 12 avaliações 4,7 não estão em destaque | Subir a nota para perto do título; convidar quem já comprou a avaliar para crescer a base
Preço/condições   | Ajustar  | Preço ok, frete/prazo ausentes          | Exibir frete e prazo na página: [preencher]
Botão de compra   | OK       | Presente e claro                        | Repetir o botão ao fim da descrição
Objeções          | Falta    | Não responde xícaras, desligar, jarra   | Criar mini-FAQ: capacidade em xícaras, desligamento automático [preencher], material da jarra [preencher]
Confiança         | Ajustar  | Sem política de troca visível           | Mostrar prazo de troca e selo de compra segura: [preencher]

PLANO PRIORIZADO
1. Fotos em uso, com escala e detalhe (impacto alto · esforço médio)
2. Mini-FAQ com as 3 dúvidas do atendimento (impacto alto · esforço baixo)
3. Novo título com benefício + capacidade (impacto médio · esforço baixo)
4. Destacar a nota 4,7 perto do título (impacto médio · esforço baixo)
5. Exibir frete, prazo e política de troca [preencher] (impacto médio · esforço baixo)
6. Reescrever bullets pelo benefício (impacto médio · esforço médio)
```

> Referência: a auditoria prioriza pelo que mais destrava venda (foto e objeções),
> confirma o que já está bom, usa a prova real (12 avaliações, sem inflar) e marca
> `[preencher]` em todo dado que o lojista não passou — nunca chuta frete, prazo ou
> política de troca.
