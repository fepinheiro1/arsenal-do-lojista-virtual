# Descrição que Converte — exemplos ilustrativos

> Casos de demonstração: cada afirmação da saída vem da entrada. A skill se adapta ao
> que você manda — e encolhe a estrutura quando o dado é pouco. Três situações comuns:

## Exemplo A — Otimizar (entrada mínima)
Entrada:
```
Melhore essa descrição:
Tênis muito confortável feito com malha respirável e EVA.
```
Como a skill age: detecta que é OTIMIZAR, reconhece que é um tênis, infere a palavra-chave e melhora o texto — sem inventar peso, garantia ou tecnologia que você não deu. "Respirável" vira "favorece a ventilação", não "pé fresco nos treinos mais longos"; sem o peso, nada de "leve"; e o EVA não vira "entressola", porque a entrada não diz onde ele está. Com dois fatos, saem dois bullets — sem ficha técnica repetida nem headline alternativa (com tão pouco dado, seria paráfrase).

Saída:
```
Conforto para treinar, com malha respirável e EVA.

Um tênis pensado para o conforto no treino: a malha respirável favorece a
ventilação e o EVA, uma espuma macia, ajuda no conforto da pisada.

• Favorece a ventilação — malha respirável.
• Conforto na pisada — espuma EVA.

Escolha a sua numeração e leve o seu.

—
Para deixar a descrição mais completa, me passe o peso (e em qual numeração foi
medido), onde fica o EVA (entressola ou palmilha) e a garantia.
```

## Exemplo B — Criar (eletrônico, dados soltos)
Entrada:
```
Notebook XZ14
Ryzen 7 · 16 GB RAM · SSD 1 TB · Tela 14"
```
Como a skill age: detecta CRIAR e categoria eletrônicos — prioriza multitarefa e armazenamento, não a estrutura emocional de moda. Sem teste, não promete "não trava" nem "abre em segundos"; sem peso e dimensões, não fala em "leve" nem "cabe na mochila"; e não cita cor no CTA, porque variante não veio.

Saída:
```
Notebook XZ14: 16 GB de RAM e SSD de 1 TB para o seu dia de trabalho.

Para quem trabalha com várias abas e programas abertos e precisa de espaço para
guardar arquivos, fotos e projetos — numa tela de 14 polegadas.

• Folga para vários programas abertos — 16 GB de RAM com processador Ryzen 7.
• Espaço de sobra para arquivos — SSD de 1 TB.

Especificações
- Processador: Ryzen 7
- Memória: 16 GB RAM
- Armazenamento: SSD 1 TB
- Tela: 14"

Finalize o pedido e leve o seu XZ14.

Headlines alternativas para teste:
- 16 GB de RAM e 1 TB de SSD num notebook de 14 polegadas.
- Notebook XZ14 com Ryzen 7: memória e espaço para o dia de trabalho.

—
Se você me passar peso e dimensões, autonomia da bateria, a geração do processador
e a garantia, eu completo a ficha e a seção de compra segura.
```

## Exemplo C — Pouca informação (sem inventar)
Entrada:
```
Crie uma descrição para uma camiseta preta.
```
Como a skill age: não faz cinco perguntas. Escreve uma versão útil só com inferências seguras e, no fim, pede o essencial que falta — sem inventar tecido nem modelagem. Com só a cor, bullets e ficha técnica seriam a mesma frase repetida, então não entram.

Saída:
```
Camiseta preta para o dia a dia, fácil de combinar.

Uma peça curinga: o preto vai bem com jeans, sarja ou short, do trabalho ao fim de
semana.

—
Se você me passar o tecido (algodão? malha fria?) e a modelagem (justa, reta,
oversized), eu deixo a descrição bem mais específica e certeira.
```

> Referência: em todos, benefício antes da característica, palavra-chave natural,
> estrutura do tamanho do dado (menos bullets, sem ficha repetida, headline alternativa
> só quando há ângulo) e zero dado inventado — o que falta vira um pedido curto no fim.
