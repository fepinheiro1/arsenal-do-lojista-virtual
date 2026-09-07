---
name: variacoes-teste-ab
description: Gera variações da copy de um anúncio para teste A/B mudando UMA variável por vez — gancho, prova, benefício, CTA ou abordagem — para você descobrir o que move o resultado sem embaralhar as causas. Use quando um anúncio já roda e você quer otimizar com método, não no chute.
---

# Variações para Teste A/B

## O que faz
Pega a copy de um anúncio que já existe e cria **variações controladas**: cada versão muda **um único elemento** (o gancho, ou a prova, ou o CTA), mantendo o resto igual. Assim, quando uma vencer, você sabe *por que* venceu — e leva o aprendizado para o próximo anúncio. É o oposto de trocar tudo de uma vez e ficar sem saber o que funcionou.

## Quando usar
- Um anúncio já roda e você quer melhorar o custo por resultado com método.
- Você tem verba para rodar 2–4 versões em paralelo (teste A/B).
- Quer aprender o que o seu público responde (qual gancho, qual prova, qual CTA), não só "achar um vencedor".

## O que a IA precisa de você
- `[anúncio atual]` — o texto principal, o título e o CTA que já estão no ar (ou um rascunho).
- `[produto e público]` — para as variações fazerem sentido.
- `[variável a testar]` (opcional) — o que você quer isolar: gancho, prova, ângulo/dor, benefício-topo ou CTA. Se não escolher, a skill testa o **gancho** primeiro (o de maior impacto) e sugere a próxima rodada.
- `[provas / ofertas reais]` (opcional) — dados que a skill pode usar. Sem eles, marca `[preencher]`.
- `[tom da marca]` — para não sair da voz.

## Instruções (o cérebro da skill)
1. **Registre o controle (versão A)**: reescreva de forma limpa o anúncio atual, marcando qual é o gancho, a prova, o benefício-topo e o CTA. Essa é a base de comparação.
2. **Escolha a variável**: se o lojista não indicou, teste o **gancho** (maior alavanca). Isole UMA variável por rodada.
3. **Gere 2 a 3 variantes (B, C, D)** que mudam **só** aquela variável — todo o resto fica idêntico ao controle, palavra por palavra. Deixe explícito, em cada variante, "o que mudou".
4. **Nomeie a hipótese** de cada variante: o que você espera aprender se ela vencer (ex.: "hipótese: abrir pela prova social convence mais do que abrir pela dor").
5. **Dê o próximo passo**: qual variável testar na rodada seguinte, depois que esta decidir.

Boas práticas de teste que a skill respeita:
- **Uma variável por teste.** Se mudar gancho e CTA juntos, o resultado não ensina nada.
- Variações **suficientemente diferentes** para gerar diferença de comportamento — não sinônimos.
- Mesma oferta e mesma verdade em todas as versões; muda a forma, não o fato.

## Regras de qualidade
- Persuasão ética em todas as variantes: sem "melhor do mundo", "imperdível", "última chance", urgência ou escassez falsa, nem garantia de resultado.
- Nenhuma variante inventa prova, número ou oferta para "ganhar" o teste — dado real ou `[preencher]`.
- Não vale criar uma variante enganosa/clickbait só para subir CTR; o teste é para aprender, não para inflar métrica vazia.
- Só o elemento em teste muda entre as versões — o restante é idêntico.
- A voz é da marca do lojista. A Performa não aparece na copy.

## Formato da saída
- **Versão A (controle)** com os elementos marcados.
- **Variável em teste** desta rodada (1 linha).
- **Versões B, C (e D)** — cada uma com o texto completo + "o que mudou" + "hipótese".
- **Próxima rodada sugerida** (qual variável isolar depois).

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
