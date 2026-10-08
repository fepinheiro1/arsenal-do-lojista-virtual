# Copy para Performance Max — exemplos reais

## Exemplo A — Varejo com feed, um modelo (atributo sem esticar)
Entrada:
```
Grupo de recursos: NimbusFlow X1 (grupo de listagem = as variantes do NimbusFlow X1 no feed)
Objetivo: vender · Marca: PisoLeve · Tom: técnico, direto
Página: loja.com.br/tenis-corrida-masculino
Confirmados (ficha técnica): malha respirável, entressola de alta absorção, 268 g
Oferta real: frete para todo o Brasil, troca de numeração facilitada, 3 meses de garantia
  contra defeito — valem para este modelo
Público: corredor amador que treina 3–4x por semana
Automação (textos gerados / expansão de URL): não sei
```
Saída:
```
Escopo: um modelo só, então todo claim abaixo vale para o grupo inteiro.

Títulos (até 30)
 1. Tênis de Corrida Masculino (26)       categoria
 2. NimbusFlow X1 (13)                    produto
 3. Leve, com Apenas 268 g (22)           benefício
 4. Feito com Malha Respirável (26)       característica
 5. Entressola de Alta Absorção (27)      característica
 6. Frete para Todo o Brasil (24)         oferta
 7. Troca de Numeração Facilitada (29)    confiança
 8. Garantia de 3 Meses (19)              confiança
 9. Para Seus Treinos da Semana (27)      uso
10. Escolha Sua Numeração (21)            ação
11. Veja o NimbusFlow X1 (20)             ação

Títulos longos (até 90)
 1. NimbusFlow X1: tênis de corrida masculino leve, com apenas 268 g. (65)
 2. Malha respirável e entressola de alta absorção para os seus treinos de corrida. (79)
 3. Frete para todo o Brasil, troca de numeração facilitada e garantia de 3 meses. (78)
 4. Um tênis de corrida para quem treina algumas vezes por semana e quer leveza no pé. (82)

Descrições (até 90)
 1. [curta] Tênis de corrida leve, com 268 g e malha respirável. (52)
 2. Entressola de alta absorção e malha respirável em um tênis de corrida de 268 g. (79)
 3. Frete para todo o Brasil e troca de numeração facilitada se o tamanho não servir. (81)
 4. 3 meses de garantia contra defeito. Escolha sua numeração e peça o seu NimbusFlow X1. (85)

Nome da empresa (até 25)
 1. PisoLeve (8)

CTA: uma opção de compra da lista da interface (ou automática) — o público já escolhe modelo.
Contagem exata, tudo dentro do limite.

O que ficou de fora, de propósito: "menos impacto no joelho" (efeito no corpo que a ficha não
prova), "pé seco do início ao fim" (respirável ≠ pé seco), "estável em qualquer piso" (não
informado), "PisoLeve Oficial" (oficial do quê?). Para mais títulos: avaliações reais, preço,
parcelamento.

Pendências
- Feed: título, preço e estoque das variantes no Merchant Center batem com a página?
- Automação: se os textos gerados estiverem ligados, o Google pode ler a página — confira se não
  há faixa de promoção vencida nela. Se a expansão de URL estiver ligada, revise excluir:
  trocas e devoluções, política de privacidade e itens esgotados.
- Sem vídeo enviado, o Google pode criar um; revise marca e claims antes de deixar rodar.
```

## Exemplo B — Coleção heterogênea, Ad Strength "Excelente" e ROAS baixo
Entrada:
```
Grupo de recursos: "Corrida", com 3 linhas no feed:
  NimbusFlow X1 (asfalto) — frete para todo o Brasil, garantia de 3 meses
  TrailRock (trilha)      — frete só Sul e Sudeste, garantia não informada
  UrbanStride (asfalto)   — saindo de linha; estoque do feed atualizado há 10 dias
Textos atuais incluem: "Frete para Todo o Brasil", "Garantia de 3 Meses", "Para o Asfalto",
  "Últimas Unidades"
Ad Strength: Excelente · ROAS abaixo do esperado · O lojista pediu "mais títulos"
```
Saída:
```
1. Mais títulos não resolvem ROAS. Ad Strength mede variedade dos textos, não lucro. ROAS baixo
   com Ad Strength alto pede diagnóstico econômico: margem por linha, preço, feed, página e
   medição. Sem margem informada, não dá para calcular o ROAS de equilíbrio.

2. Os textos atuais prometem o que não vale para o grupo todo:
   - "Frete para Todo o Brasil": só o NimbusFlow. O TrailRock entrega no Sul e Sudeste. Remover.
   - "Garantia de 3 Meses": só confirmada no NimbusFlow. Remover.
   - "Para o Asfalto": não vale para o TrailRock. Remover.
   - "Últimas Unidades": escassez sem base (o estoque do feed está 10 dias atrasado). Remover e
     atualizar o feed. Se o UrbanStride sai de linha, avaliar tirá-lo do grupo de listagem.

3. Duas saídas:
   a) Dividir o grupo (se houver volume): "Corrida de rua" (NimbusFlow + UrbanStride) e "Trilha"
      (TrailRock). Cada um ganha textos com a verdade dos próprios produtos — inclusive o frete
      nacional no grupo onde ele vale.
   b) Manter um grupo só, com o que é comum a todos:
      Títulos: Tênis de Corrida (16) · Modelos Para Asfalto e Trilha (29) ·
               Escolha Sua Numeração (21) · Veja os Modelos de Corrida (26)
      Descrição curta: Tênis de corrida para asfalto e trilha. Veja os modelos. (56)
   Recomendação: (a), porque o claim mais forte (frete nacional) só aparece onde é verdade.

4. Depois de mudar: uma coisa por vez. Corrigir feed e textos primeiro; não mexer em orçamento
   e meta junto, senão não dá para saber o que mudou o resultado.
```

> Referência: o escopo do grupo vem antes do texto; todo claim vale para todos os produtos
> cobertos; o atributo confirmado não vira efeito no corpo; a contagem é exata; a automação do
> Google (textos gerados, expansão de URL, vídeo) entra como pendência; e Ad Strength alto com
> ROAS baixo leva a um diagnóstico econômico, não a mais copy.
