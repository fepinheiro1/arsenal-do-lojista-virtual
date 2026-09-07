# Variações para Teste A/B — exemplo real

## Entrada
```
Anúncio atual:
  Texto principal: Cansada de secar o cabelo e ele armar de novo em 10 minutos?
    A escova secadora alisa e seca ao mesmo tempo, com cerdas que domam o frizz.
    Salão em casa, todo dia. Toca em Comprar agora.
  Título: Escova secadora que aliza e seca
  CTA: Comprar agora
Produto e público: escova secadora 2 em 1; mulheres 25–45 que lutam com frizz
Provas reais: 4,7 de 5 em 1.200 avaliações
Variável a testar: (não indicada — testar gancho)
Tom da marca: próximo, empolgado na medida, sem apelação
```

## Saída
```
VERSÃO A — CONTROLE
Texto principal: Cansada de secar o cabelo e ele armar de novo em 10 minutos? [GANCHO: dor]
A escova secadora alisa e seca ao mesmo tempo, com cerdas que domam o frizz. [BENEFÍCIO-TOPO]
Salão em casa, todo dia. Toca em Comprar agora. [CTA]
Título: Escova secadora que aliza e seca
(Sem prova social no texto atual.)

VARIÁVEL EM TESTE (rodada 1): o GANCHO (a 1ª linha). Todo o resto fica idêntico ao controle.

VERSÃO B — gancho por PROVA SOCIAL
Texto principal: 4,7 de 5 em 1.200 avaliações de quem cansou de brigar com o frizz.
A escova secadora alisa e seca ao mesmo tempo, com cerdas que domam o frizz.
Salão em casa, todo dia. Toca em Comprar agora.
Título: Escova secadora que aliza e seca
O que mudou: só a 1ª linha (dor → prova social). Resto igual ao A.
Hipótese: abrir mostrando que muita gente já aprovou convence mais do que abrir pela dor.

VERSÃO C — gancho por DESEJO / resultado
Texto principal: Aquele liso de escova, feito em casa, antes do café ficar pronto.
A escova secadora alisa e seca ao mesmo tempo, com cerdas que domam o frizz.
Salão em casa, todo dia. Toca em Comprar agora.
Título: Escova secadora que aliza e seca
O que mudou: só a 1ª linha (dor → desejo/resultado). Resto igual ao A.
Hipótese: mostrar o resultado desejado logo de cara atrai mais do que lembrar do problema.

VERSÃO D — gancho por PERGUNTA DE TEMPO
Texto principal: Quanto tempo você perde secando e pranchando toda manhã?
A escova secadora alisa e seca ao mesmo tempo, com cerdas que domam o frizz.
Salão em casa, todo dia. Toca em Comprar agora.
Título: Escova secadora que aliza e seca
O que mudou: só a 1ª linha (dor genérica → dor específica de tempo). Resto igual ao A.
Hipótese: a economia de tempo pesa mais na decisão do que o frizz em si.

PRÓXIMA RODADA SUGERIDA: com o gancho vencedor fixo, testar o CTA
("Comprar agora" × "Quero o meu" × "Ver oferta") — isolando só o botão/última linha.
```

> Referência de qualidade: uma variável só muda entre as versões (a 1ª linha), o corpo é
> idêntico palavra por palavra, cada variante traz uma hipótese clara de aprendizado, a
> prova usa o dado real (4,7/1.200) sem inventar, e nenhuma versão apela para urgência falsa
> ou clickbait. O próximo passo mantém o método (isolar o CTA na rodada seguinte).
