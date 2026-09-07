---
name: urgencia-honesta
description: Comunica urgência e escassez reais (estoque baixo de verdade, promoção com data real, reposição a caminho) sem apelar para contador falso ou "última chance". Use quando existe um motivo verdadeiro para a pessoa decidir agora.
---

# Urgência Honesta

## O que faz
Transforma um motivo real de urgência — estoque de fato baixo, uma promoção que termina em data marcada, um lote limitado, prazo de entrega que depende de comprar até certo dia — em uma mensagem clara que ajuda a pessoa a decidir agora. Urgência honesta informa um fato verdadeiro; urgência falsa fabrica pressão. Esta skill só faz a primeira.

## Quando usar
- Estoque realmente baixo de um item (o número no sistema é pequeno).
- Promoção ou coleção com data de fim definida de verdade.
- Lote/edição limitada, pré-venda com vagas, ou prazo de corte para entrega em data (ex.: comprar até X para chegar no Natal).

## O que a IA precisa de você
- `[produto ou campanha]` — o que é e onde a mensagem aparece.
- `[fato de urgência real]` — o dado verdadeiro: quantas unidades restam, data de fim da promoção, tamanho do lote, prazo de corte. **Só um fato que existe no sistema.**
- `[o que acontece depois]` — repõe? volta ao preço cheio? esgota mesmo? Isso define o tom.
- `[público e tom da marca]` — para calibrar a linguagem.

## Instruções (o cérebro da skill)
1. **Confirme que há urgência real.** Se o lojista não tem um fato verdadeiro (estoque baixo, data, lote), a skill não fabrica um. Nesse caso, diga isso e sugira vender pelo benefício, sem urgência.
2. **Escreva a mensagem a partir do fato**, de forma calma e específica:
   - **Estoque baixo real**: informe o dado ("Últimas 4 unidades desta cor"). Número verdadeiro, atualizado pelo sistema. Sem "resta 1" fixo.
   - **Promoção com data**: informe quando termina ("A oferta vai até domingo, 14/09"). Data real, sem cronômetro que reinicia.
   - **Lote/edição limitada**: diga o tamanho do lote e o que acontece depois ("Lote de 50 peças; a próxima leva chega em [preencher]").
   - **Prazo de entrega**: conecte a compra ao ganho ("Peça até quinta para receber antes do fim de semana").
3. **Enquadre pelo benefício de decidir agora**, não pelo medo de perder. "Garanta a sua cor antes que ela esgote" pesa melhor que "corra ou vai se arrepender".
4. **Diga o que acontece depois** com honestidade: se repõe, a pessoa sabe que haverá outra chance; se esgota mesmo, o fato fala por si.
5. Entregue a mensagem em 2–3 formatos de uso: selo curto na página, linha no carrinho e (se fizer sentido) uma frase para e-mail/WhatsApp.

## Regras de qualidade
- **Todo número e data são reais e verificáveis.** Estoque exibido reflete o sistema; data de fim é a data de verdade.
- **Proibido**: cronômetro que reinicia, "só hoje" que é todo dia, "resta 1" fixo, "últimas unidades" com galpão cheio, "X pessoas vendo agora" inventado.
- Sem "última chance", "imperdível", "corra", "não perca" nem ameaça de arrependimento.
- Se não há fato de urgência, não crie um — recomende vender pelo valor.
- Não invente a data, o número ou o prazo — marque `[preencher]` para o lojista confirmar.
- A mensagem é da marca do lojista, em tom calmo e confiante.

## Formato da saída
1. **Checagem**: qual é o fato real de urgência (ou aviso de que não há um, e o que fazer no lugar).
2. **Mensagens prontas**: selo curto na página, linha no carrinho e (opcional) frase para e-mail/WhatsApp.
3. **Nota de honestidade**: o que precisa estar ligado ao sistema (estoque real, data configurada) para a mensagem não virar promessa falsa.

---
Arsenal do Lojista · por **Performa.AI** — performance digital para e-commerce.
