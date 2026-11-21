# tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/longfeizheng/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/longfeizheng/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine that fits in 4,096 bytes of Python: negamax alpha-beta
search with iterative deepening under a fixed node budget (never a
clock, so every position always gets the same move), quiescence over
captures and promotions, a transposition table, MVV-LVA move ordering,
and a material + piece-square evaluation with a bishop-pair bonus and
a phase-tapered king table. The committed `main.py` is the packed form
of the readable source, produced by the kit's `compress` command; the
source ships beside the entry's transcripts in the submission bundle.
In a local practice gauntlet it beat the depth-2 and depth-3 house
engines (2 wins, 4 losses over the six practice games).

## Run it

```sh
MAKEFUN_ENV_URL=http://localhost:8080 python3 main.py
```

It plays the tiny-chess-01 gauntlet through the env at
`MAKEFUN_ENV_URL`: `POST /game` serves the game in play and
`POST /move` plays the chosen move, until the env answers `done`.

---

<sub>Entered on [make.fun](https://make.fun/?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
