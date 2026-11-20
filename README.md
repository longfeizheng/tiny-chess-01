# Tiny Chess — a 4 KB engine

A chess engine that fits in 4,096 bytes of Python: negamax alpha-beta
search with iterative deepening under a fixed node budget (never a
clock, so every position always gets the same move), quiescence over
captures and promotions, a transposition table, MVV-LVA / killer /
history move ordering, and a material + piece-square evaluation with a
bishop-pair bonus and a phase-tapered king table.

The committed `main.py` is the packed form of the readable source,
produced by the kit's `compress` command; the source ships beside the
entry's transcripts in the submission bundle.

It plays the tiny-chess-01 gauntlet through the env at
`MAKEFUN_ENV_URL`: `POST /game` serves the game in play and
`POST /move` plays the chosen move, until the env answers `done`.
