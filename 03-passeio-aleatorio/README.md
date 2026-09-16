# Passeio aleatório simples: preço de uma ação

## O exercício

Lista 2, exercício 11. `Y_1, ..., Y_n` iid, `P(Y_i = 1) = P(Y_i = -1) = 1/2`
(alta ou queda de R$1 no preço de uma ação no dia `i`), e `X_n = Σ Y_i` é a
variação acumulada após `n` dias.

- simular e plotar realizações de `X_n` para `n = 1, ..., 1000`;
- `E[X_n] = 0` e `Var(X_n) = n` — e o que isso implica (ou não) sobre `X_n`
  ficar perto de zero quando `n` é grande;
- `K_n` = número de dias de alta entre os `n` primeiros; `X_n = 2K_n - n`,
  com `K_n ~ Binomial(n, 1/2)` — daí a distribuição de `X_n`;
- histogramas de `X_n` para `n = 10, 100, 1000` comparados com a teoria, e o
  desvio-padrão (`√n`) como medida da largura típica das flutuações.

## A conclusão

As trajetórias simuladas não convergem pra nenhum valor fixo — o passeio se afasta da origem conforme `n`
cresce. `E[X_n] = 0` não significa que `X_n` fica perto de zero: como `Var(X_n) = n` cresce sem limite, as
flutuações típicas (`√n`) também crescem, só que mais devagar que `n`.

Escrever `X_n = 2K_n - n` com `K_n ~ Binomial(n, 1/2)` dá a distribuição exata de `X_n` (não só
assintótica), e os histogramas simulados batem bem com essa PMF teórica para `n = 10, 100, 1000`. O
desvio-padrão empírico também fica bem próximo de `√n` em cada caso, confirmando que a largura típica das
flutuações cresce como `√n`.
