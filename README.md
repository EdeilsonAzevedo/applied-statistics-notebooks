# Applied Statistics Notebooks

Exercise notebooks from the Statistics and Probability course of my master's
in Applied Mathematics and Computing (ICMC). Each folder is one exercise:
a short simulation, the theory behind it, and a written conclusion.

## Exercises

| # | Notebook | Topic |
|---|----------|-------|
| 01 | [`jogo-da-vida`](01-jogo-da-vida/) | Multiplicative wealth process — expectation vs. typical (median) outcome |
| 02 | [`medias-normal-cauchy`](02-medias-normal-cauchy/) | Sample mean under Normal vs. Cauchy — LLN and stable distributions ([lista2](lista2.pdf), ex. 10) |
| 03 | [`passeio-aleatorio`](03-passeio-aleatorio/) | Simple random walk — stock price toy model ([lista2](lista2.pdf), ex. 11) |
| 04 | [`poisson-correlacionado`](04-poisson-correlacionado/) | Sampling correlated Poisson pairs, positive and negative correlation ([lista2](lista2.pdf), ex. 12) |

## Running locally

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
jupyter lab
```
