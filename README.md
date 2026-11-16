# makefun-tiny-chess

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/Andy74453533/makefun-tiny-chess/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/Andy74453533/makefun-tiny-chess/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in 4,096 bytes of Python: a 0x88 board, alpha-beta search with
a transposition table, quiescence, null-move pruning, late-move reductions,
history ordering and a tapered piece-square evaluation, searching to a fixed
node budget per move. No clock, no randomness: the same position always gets
the same move, so a trial's live pass and its replay agree. `main.py` is the
whole engine, packed from its readable source with the kit's `makefun
compress`; it plays the house gauntlet through the trial env over HTTP.

## Run it

```sh
python3 main.py
```

Runs on Python 3.13 with the standard library only, no dependencies. It
expects `MAKEFUN_ENV_URL` to point at the trial env, plays every game of the
gauntlet through it, and exits when the trial reports done.

---

<sub>Entered on [make.fun](https://make.fun/?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
