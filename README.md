# Arsenal do Lojista

**Um arsenal de skills de IA para quem vende online — do produto ao anúncio.**

Coleção curada e testada de habilidades de inteligência artificial, organizada por frente de trabalho do e-commerce. Cada skill é uma peça pronta: você abre, preenche o que é seu, e a IA entrega. Sem prompt genérico, sem achismo — cada uma foi lapidada pra um trabalho específico da operação.

> Feito para quem já vende: lojista com tráfego ativo que quer transformar mais do que já entra na loja em resultado.

---

## Como está organizado

O Arsenal é dividido em **8 frentes**. Cada frente é uma pasta; cada skill dentro dela é uma pasta própria com tudo que você precisa.

| Frente | O que resolve |
|--------|---------------|
| [`01-produto`](01-produto/) | Descrição, título, bullets e ficha do produto |
| [`02-imagem`](02-imagem/) | Prompts para foto de produto, banner e cena |
| [`03-social`](03-social/) | Post, legenda, roteiro de Reels e calendário |
| [`04-email`](04-email/) | HTML de e-mail, boas-vindas, recuperação e pós-compra |
| [`05-google-ads`](05-google-ads/) | Títulos, descrições, PMax e estrutura de campanha |
| [`06-meta-ads`](06-meta-ads/) | Ângulos, copy por público e roteiro de criativo |
| [`07-cro`](07-cro/) | Auditoria de página, prova social e checkout |
| [`08-atendimento-analise`](08-atendimento-analise/) | Atendimento, objeções, concorrência e precificação |

---

## Como usar

Cada skill vem em **dois formatos** — use o que combina com a sua ferramenta:

**1. Em qualquer IA (ChatGPT, Gemini, Claude no navegador)**
Abra o `prompt.md` da skill, copie o conteúdo, troque o que está entre `[colchetes]` pelos seus dados e cole na conversa. Pronto.

**2. No Claude (Claude Code, Claude Desktop com skills)**
Aponte para a pasta da skill. O `SKILL.md` é reconhecido automaticamente e a IA passa a operar naquele modo.

Todas trazem também um `exemplo.md` — um caso real de entrada e saída, pra você ver o resultado antes de rodar.

---

## Estrutura de cada skill

```
nome-da-skill/
├── SKILL.md      → a skill no formato Claude (invocável)
├── prompt.md     → o mesmo poder em prompt copia-e-cola (qualquer IA)
└── exemplo.md    → um caso real: entrada → saída
```

O molde padrão que toda skill segue está em [`_template/`](_template/).

---

Feito por **[Performa.AI](https://performa.ai)** — tecnologia de performance digital para e-commerce.
A Performa trabalha o tráfego que já entra na sua loja: mais conversão, mais ticket, mais previsibilidade.
