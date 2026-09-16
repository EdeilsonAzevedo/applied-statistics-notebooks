# Médias amostrais: Normal vs. Cauchy

## O exercício

Lista 2, exercício 10. Duas sequências independentes:

- `X_1, ..., X_n` iid `N(0, 1)`;
- `Y_1, ..., Y_n` iid Cauchy padrão, `f_Y(y) = 1 / (π(1 + y²))`.

Definimos as médias amostrais `X̄_n` e `Ȳ_n` e comparamos seu comportamento
quando `n` cresce (`n = 1, ..., 10000`):

- previsão qualitativa antes de simular;
- trajetória de `X̄_n` e `Ȳ_n` em função de `n`;
- histogramas de `X̄_n` e `Ȳ_n` para `n = 10, 100, 1000, 10000`;
- comparação com a teoria: `X̄_n ~ N(0, 1/n)`, enquanto `Ȳ_n` continua
  Cauchy padrão para qualquer `n` (a distribuição de Cauchy é estável);
- repetir usando a **mediana** amostral de `Y_i` em vez da média.

## A conclusão

Para `X̄_n` (Normal) a convergência é clara: a média amostral vai pra 0 e a dispersão cai com `1/√n`,
como previsto por `X̄_n ~ N(0, 1/n)`.

Para `Ȳ_n` (Cauchy) a média amostral não converge — a trajetória continua "pulando" mesmo com `n`
grande e os histogramas não ficam mais estreitos, porque `Ȳ_n` continua Cauchy(0,1) pra qualquer `n`
(a LGN não vale, já que a Cauchy não tem média finita).

Trocando a média pela mediana amostral de `Y_i`, o comportamento muda: a mediana converge pra 0 e o
desvio padrão dela cai com `n`, mostrando na prática que a mediana é um estimador mais robusto que a
média para distribuições de cauda pesada.
