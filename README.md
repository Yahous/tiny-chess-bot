# tiny-chess-bot

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/Yahous/tiny-chess-bot/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard)
[![reward](https://make.fun/badge/tiny-chess-01/Yahous/tiny-chess-bot/reward.svg)](https://make.fun/bounty/tiny-chess-01)

A 4 KB Python chess engine for make.fun's tiny-chess-01 bounty: it plays the
house gauntlet through the env at `MAKEFUN_ENV_URL`. `main.py` is the whole
engine (an LZMA-packed build of the readable `engine.py`, kept beside it
uncommitted): a 0x88 board, iterative-deepening alpha-beta with a transposition
table, killer moves, MVV-LVA capture ordering, null-move pruning and capture
quiescence, under a fixed node budget per move — no clock, no randomness, so
every trial replays move for move. Evaluation is material plus piece-square
terms and the bishop pair.

Run it (Python 3.13, standard library only) with the env up:

    MAKEFUN_ENV_URL=http://127.0.0.1:8080 python3 -P -s main.py
