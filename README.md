# Applied Statistics Notebooks

Exercise notebooks from the Statistics and Probability course of my master's
in Applied Mathematics and Computing (ICMC). Each folder is one exercise:
a short simulation or data analysis, the theory behind it, and a written
conclusion. Datasets for lista 3 live in [`dados_lista3/`](dados_lista3/).

## Exercises

| # | Notebook | Topic |
|---|----------|-------|
| 01 | [`jogo-da-vida`](01-jogo-da-vida/) | Multiplicative wealth process — expectation vs. typical (median) outcome |
| 02 | [`medias-normal-cauchy`](02-medias-normal-cauchy/) | Sample mean under Normal vs. Cauchy — LLN and stable distributions ([lista2](lista2.pdf), ex. 10) |
| 03 | [`passeio-aleatorio`](03-passeio-aleatorio/) | Simple random walk — stock price toy model ([lista2](lista2.pdf), ex. 11) |
| 04 | [`poisson-correlacionado`](04-poisson-correlacionado/) | Sampling correlated Poisson pairs, positive and negative correlation ([lista2](lista2.pdf), ex. 12) |
| 05 | [`morte-tira-ferias`](morte-tira-ferias/) | Can people postpone death? Deaths around Passover, written solution in PDF ([lista3](lista3%20%281%29.pdf), ex. 6) |
| 06 | [`wald-poisson`](wald-poisson/) | Wald test for a Poisson mean — derivation and simulated type I error ([lista3](lista3%20%281%29.pdf), ex. 7) |
| 07 | [`filmes-acao-romance`](filmes-acao-romance/) | Action vs. romance IMDb ratings — two-sample Wald test, CIs, association vs. causation ([lista3](lista3%20%281%29.pdf), ex. 8) |
| 08 | [`pinguins-chinstrap`](pinguins-chinstrap/) | Chinstrap penguins — body mass by sex and a permutation test for bill correlation ([lista3](lista3%20%281%29.pdf), ex. 9) |

## Running locally

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
jupyter lab
```
