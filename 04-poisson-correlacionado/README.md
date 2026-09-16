# Variáveis Poisson correlacionadas

## O exercício

Lista 2, exercício 12 (o de maior peso, 6.0 pontos). Objetivo: gerar pares
`(X, Y)` com `X ~ Poisson(μX)`, `Y ~ Poisson(μY)` e `corr(X, Y) ≠ 0`.

- **(a)** amostrador da PMF conjunta da Eq. (5) e histogramas 2D (`ρXY ≥ 0`);
- **(b)** método alternativo por soma de variáveis independentes (`X = Z1+Z3`,
  `Y = Z2+Z3`, com `Z1, Z2, Z3` Poisson independentes) — só gera `ρXY ≥ 0`;
- **(c)** cálculo analítico de `cov(X, Y)` e `ρXY` a partir do método de (b);
- **(d)** distribuição da Eq. (6) (Ghosh, Marques & Chakraborty, 2021), que
  permite `ρXY < 0` via condicionais `X|Y=y ~ Poisson(λX·λʸ)` e
  `Y|X=x ~ Poisson(λY·λˣ)` — amostrador e histograma 2D com correlação
  negativa.

## A conclusão

Os métodos (a) e (b) dão exatamente a mesma distribuição (a PMF direta da Eq. 5 e a soma `X=Z1+Z3,
Y=Z2+Z3` batem empiricamente), e a covariância desse par é `Cov(X,Y) = theta ≥ 0` — por isso esses métodos
nunca geram correlação negativa, só a parte "compartilhada" `Z3` (que é uma variância) pode empurrar `X` e
`Y` para o mesmo lado.

Para correlação negativa foi preciso trocar de abordagem: usar a distribuição de Ghosh, Marques &
Chakraborty (2021) — artigo em `ghosh2021NewBivariate.pdf` nesta pasta —, definida pelas condicionais
`X|Y=y ~ Poisson(λX·λʸ)` e `Y|X=x ~ Poisson(λY·λˣ)`. Como a constante de normalização dessa distribuição
não tem forma fechada simples, o amostrador foi implementado via Gibbs sampling nas próprias condicionais.
A correlação empírica obtida (`≈ -0.56` para `λ=0.03` e `≈ -0.055` para `λ=0.97`, com `λX=λY=2`) ficou bem
próxima dos valores reportados pelos próprios autores nas Figuras 5 e 6 do artigo.
