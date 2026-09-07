---
name: angulos-de-anuncio
description: Gera vários ângulos diferentes para anunciar o mesmo produto no Facebook e Instagram — dor, desejo, prova, comparação e história — cada um com a ideia central e um texto principal de abertura. Use quando um criativo cansou, o custo por resultado subiu, ou você vai começar a testar um produto e não sabe por onde atacar.
---

# Ângulos de Anúncio

## O que faz
Pega um único produto e cria vários **ângulos de venda** diferentes — jeitos distintos de contar a mesma história para o mesmo público. Um produto não tem uma copy só: tem a versão que fala da dor, a que fala do desejo, a que mostra prova, a que compara com a alternativa antiga e a que conta uma história. Cada ângulo vira um anúncio novo para testar, sem precisar de um produto novo.

## Quando usar
- O criativo atual "cansou" (o custo por resultado começou a subir).
- Você vai lançar um produto e quer 5 apostas na mesa em vez de uma.
- O público responde, mas você não sabe qual dor ou desejo puxa mais a compra.
- Antes de gravar vídeo ou pedir arte — o ângulo define a cena.

## O que a IA precisa de você
- `[produto]` — nome e o que é.
- `[público]` — para quem vende (ex.: mãe de recém-nascido, corredor amador).
- `[transformação]` — o antes → depois que o produto entrega (o que muda na vida da pessoa).
- `[diferenciais]` — o que ele tem de real (material, tecnologia, garantia, origem).
- `[provas]` (opcional) — avaliações, número de clientes, selo, resultado medido. Sem isso, a prova fica marcada `[preencher]`.
- `[tom da marca]` — como a loja fala.

## Instruções (o cérebro da skill)
Gere **5 ângulos**, um de cada tipo abaixo. Para cada ângulo, entregue: **nome do ângulo · ideia central (1 frase) · gancho (a 1ª linha do anúncio) · texto principal curto (2–4 frases) · para quem esse ângulo funciona melhor**.

1. **Dor** — parte de um incômodo real e concreto do dia a dia do público, sem dramatizar nem culpar a pessoa. Mostra a situação, depois o produto como saída natural.
2. **Desejo** — parte do resultado que a pessoa quer alcançar (a versão dela com o problema resolvido). Vende o depois, não o produto.
3. **Prova** — abre com a evidência: número de clientes, avaliação, um depoimento curto, um resultado medido. Se não houver dado real, marque `[preencher: avaliação / nº de clientes]` — nunca invente.
4. **Comparação** — coloca lado a lado o jeito antigo/comum e o jeito que o produto propõe. Compara com a *alternativa* (o método velho), nunca ataca um concorrente pelo nome.
5. **História** — micro-narrativa de uma pessoa real (ou plausível) passando pela transformação. Começo, virada, fim. Humano, específico, sem final milagroso.

Regras de encaixe no Meta:
- O **gancho** é a primeira linha e precisa fazer sentido sozinho — no feed a pessoa vê ~2 linhas antes do "ver mais".
- Cada ângulo é independente: dá pra rodar sozinho como um anúncio.
- Ao final, indique qual ângulo você testaria **primeiro** e por quê (com base no público informado).

## Regras de qualidade
- Persuasão ética: sem "melhor do mundo", "imperdível", "última chance", "explosão de vendas", urgência ou escassez falsa, e nenhuma garantia de resultado.
- Ângulo de dor mostra a situação, nunca acusa a pessoa ("você está perdendo", "você não sabe"). A dor é do contexto, não uma falha dela.
- Prova só com dado real. Faltou dado, marque `[preencher]`.
- Comparação nunca cita concorrente pelo nome nem o diminui.
- A voz é da marca do lojista. A Performa não aparece na copy.
- Benefício antes de característica. Frases curtas.

## Formato da saída
5 blocos, um por ângulo, cada um com: **Ângulo (tipo)** · Ideia central · Gancho · Texto principal · Melhor para. No fim, uma linha de recomendação: qual testar primeiro e por quê.

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
