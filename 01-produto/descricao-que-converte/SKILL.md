---
name: descricao-que-converte
description: Cria ou otimiza a descrição de um produto de e-commerce com foco em conversão, clareza, SEO natural e precisão factual. Aceita dados soltos, uma descrição existente ou uma URL, detecta sozinha se é para criar ou melhorar, e adapta a estrutura à categoria e ao ticket do produto. Use ao cadastrar um produto novo ou melhorar a descrição de um que já vende.
---

# Descrição que Converte

## O que faz
Escreve a descrição de um produto pronta para publicar — ou melhora uma que já existe — começando pelo benefício, na ordem em que a pessoa decide comprar, otimizada para busca sem soar robótica. Infere sozinha o que der (categoria, público, palavra-chave, tom, profundidade), pergunta pouco e nunca inventa dado que não recebeu.

Regra de ouro: **simples na superfície, especialista por baixo.** O lojista não precisa saber copywriting, SEO ou estrutura de página — só dizer o que é o produto.

## Quando usar
- Cadastrar um produto novo, a partir de dados soltos, uma ficha, o que tiver.
- Melhorar uma descrição fraca que já está no ar (cole o texto ou a URL).
- Padronizar um catálogo inteiro no mesmo tom e na mesma estrutura.

## O que a IA precisa de você
No mínimo, **uma** destas coisas:
- os **dados do produto** (nome + o que você souber: características, preço, público), ou
- uma **descrição atual** para melhorar, ou
- uma **URL** do produto (se você tiver navegação disponível; se não tiver, cole o texto da página).

Todo o resto é **opcional** e só afina o resultado: palavra-chave alvo, tom da marca, diferenciais, prova (reviews), garantia, prazo, concorrentes. Se você não informar, a IA infere com segurança o que for possível e só pergunta 1 ou 2 coisas curtas quando a falta realmente impedir uma boa descrição.

## Como funciona (por baixo)

**1. Detecta o modo, sozinha.**
- **Criar** — recebeu dados soltos/ficha, ou o pedido é "crie uma descrição". Monta do zero.
- **Otimizar** — recebeu uma descrição pronta ou uma URL, ou o pedido é "melhore / revise / deixe mais persuasivo". Aí preserva os fatos, corta exagero, repetição e frase genérica, melhora hierarquia e benefícios, e devolve uma versão superior — sem reconstruir do zero à toa.

**2. Infere com segurança (e pergunta pouco).** Do que recebeu, deduz o que der: tipo de produto, categoria, público provável, intenção de busca, palavra-chave principal, tom e profundidade. Só pergunta 1–2 coisas quando a ausência impede a qualidade. Sem interrogatório.

**3. Palavra-chave natural.** Se você não deu a palavra-chave, ela infere a expressão que a pessoa realmente busca (ex.: "Tênis NimbusFlow, corrida, masculino" → *tênis de corrida masculino*). Usa essa expressão nos pontos que importam (headline, abertura, um subtítulo, um bullet) e variações naturais no resto. Nunca empilha palavra-chave nem sacrifica a leitura por SEO.

**4. Adapta a estrutura à categoria.** Prioriza o que decide a compra naquele tipo de produto:

| Categoria | Prioriza |
|---|---|
| Moda | tecido, composição, caimento, modelagem, ocasião, tamanho, cuidados |
| Calçados | uso, conforto, amortecimento, solado, peso, ajuste, terreno, numeração |
| Eletrônicos | função, desempenho, conectividade, compatibilidade, autonomia, garantia |
| Casa & decoração | dimensões, material, ambiente, montagem, durabilidade, limpeza |
| Beleza | finalidade, textura, modo de uso, ativos, indicação, restrições |
| Alimentos & bebidas | sabor, composição, modo de consumo, origem, peso, conservação, alergênicos |
| Infantil | faixa etária, segurança, material, certificações, cuidados |
| Esporte | uso, nível, material, resistência, desempenho, contexto de prática |

Outra categoria? Aplica o mesmo raciocínio: o que a pessoa precisa saber para decidir se aquilo serve para ela.

**5. Adapta o tamanho ao ticket/complexidade.** Produto simples e barato (cabo, caneca) → descrição curta. Intermediário (tênis, eletroportátil) → média. Alto ticket / complexo (notebook, colchão) → detalhada, com mais especificação e redução de risco. A profundidade é decidida automaticamente.

**6. Transforma característica em benefício — sem inventar.** Da especificação para o ganho, com a evidência junto e o benefício plausível:
- Vira: *"Mais conforto nas passadas — entressola de 32 mm em espuma EVA."*
- Não vira: *"protege seus joelhos"* (alegação não comprovada).

## Instruções (o cérebro da skill)
1. Identifique o **modo** (criar / otimizar) e organize o que recebeu.
2. Classifique a **categoria** e infira **público, palavra-chave, tom e profundidade** com segurança.
3. Escreva na estrutura abaixo, benefício antes da característica, pensada para o celular:
   - **Headline** — benefício principal + o produto, com a palavra-chave natural.
   - **Abertura** — 2 a 4 frases: para quem é, para qual situação, por que importa.
   - **Benefícios** — 4 a 6 bullets no formato `Benefício — característica que o sustenta`.
   - **Especificações** — lista limpa, só fatos informados ou verificáveis.
   - **Redução de risco** — garantia, troca, suporte, certificação (só se houver o dado).
   - **CTA** — curto, no tom da marca.
4. Rode o **Quality Gate** (abaixo) em silêncio e corrija antes de entregar.
5. Entregue a descrição pronta para colar, com 2 variações de headline para teste.

## Regras de qualidade
- **Nunca invente** material, medida, certificação, origem, garantia, duração, performance, compatibilidade, benefício de saúde, resultado, estoque, prazo, avaliação ou prova social. Faltou o dado? Omita e, no fim, sinalize ao lojista em uma linha o que completaria a descrição.
- **Distinga sempre**: fato informado (pode afirmar — "5000 mAh") · inferência segura (com cautela — "bateria de alta capacidade") · alegação não comprovada (proibida sem evidência — "dura o dia inteiro").
- **Claims sensíveis** (saúde, cosmético, suplemento, infantil, segurança): nada de "elimina dores", "cura", "protege totalmente", "garante resultado". Só linguagem compatível com o dado real do produto.
- **Persuasão ética**: sem "melhor do mundo", "imperdível", "última chance", urgência ou escassez falsa.
- **Voz do lojista, não da Performa**: infira o tom pela categoria, faixa de preço, público e texto atual, e escreva como a loja falaria. Nunca use um tom genérico de fornecedor de tecnologia.
- **Dados conflitantes** (ex.: "100% algodão" vs "95% algodão + 5% elastano"): não escolha no silêncio — peça uma confirmação curta.
- **Mobile-first**: parágrafos e frases curtas, uma ideia por bullet, o que importa primeiro, sem parede de texto nem adjetivo vazio.

### Quality Gate (silencioso, antes de entregar)
Inventei algum dado? · Alguma promessa não comprovada? · Benefício veio antes da característica? · Ficou claro para quem o produto é? · Destaquei o diferencial? · Tem frase genérica pra cortar? · Soa humano e escaneável no celular? · O SEO ficou natural? · Repeti informação? · Omiti alguma característica que importa? · O CTA combina com a marca?

## Formato da saída
Por padrão, **só a descrição pronta para copiar e colar** (headline, abertura, bullets, especificações, redução de risco, CTA) mais 2 variações de headline. Nada de análise, score ou lista de técnicas.

Se faltou algo relevante, uma linha curta no fim — ex.: *"Se você me passar o tecido e a garantia, deixo a descrição bem mais específica."*

Sob pedido (ou em modo avançado), a skill também entrega: SEO title, meta description, versão curta, versão para marketplace ou Google Merchant, ou mais variações de headline.

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
