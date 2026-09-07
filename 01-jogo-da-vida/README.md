# Jogo da vida: quando a média mente

## O exercício

Simulação de um processo multiplicativo de fortuna: cada jogador começa com
`c0 = 100` e, a cada rodada, aposta tudo o que tem.

- com probabilidade `p = 0.5`, dobra a fortuna (`× 2`);
- com probabilidade `1 - p = 0.5`, perde metade (`× 0.5`).

São simulados milhares de jogadores independentes por várias rodadas, e o
resultado é comparado com a teoria:

- `E[Y] = p·2 + (1-p)·0.5 = 5/4` → o multiplicador esperado por rodada;
- `E[X_n] = c0 · (5/4)^n` → a fortuna esperada cresce exponencialmente;
- `Var(X_n) = c0² · (E[Y²]ⁿ − E[Y]²ⁿ)`, com `E[Y²] = 17/8`.

O notebook compara essa previsão teórica com a média, a mediana e as
trajetórias simuladas (incluindo o jogador mais sortudo e os grupos dos que
mais ganharam/perderam).

## A conclusão

A média da fortuna cresce sem parar (fator `5/4` por rodada), mas isso é
sustentado por uma minoria cada vez menor de jogadores extremamente
sortudos. O jogador típico não segue a média: como `E[ln Y] = 0.5·ln2 +
0.5·ln0.5 = 0`, a fortuna **típica** (a mediana) não cresce nem cai em
média — e, na prática, a maioria das trajetórias individuais tende a
zero, porque perdas e ganhos não se cancelam simetricamente em escala
multiplicativa.

É o exemplo clássico de **média (esperança) ≠ comportamento típico** em
processos multiplicativos: olhar só para `E[X_n]` dá uma falsa sensação de
que "o jogo é bom", quando na verdade quase todo mundo perde e o resultado
médio é carregado por raríssimos grandes vencedores.
