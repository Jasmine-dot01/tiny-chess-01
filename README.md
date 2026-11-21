# tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/jasmine-dot01/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/jasmine-dot01/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A 4 KB Python chess engine that plays through the make.fun env service with a fixed 100,000-node alpha-beta search, null-move pruning, killer and history move ordering, and a transposition table. It fits in 4,090 bytes as a self-extracting LZMA payload and plays deterministically with no model calls.

## How it plays

The engine is a single self-extracting LZMA payload (`main.py`, 4,090 bytes, Python 3.13 standard library only). Every move it runs a fixed 100,000-node alpha-beta search — deterministic, with no clock and no unseeded randomness — over a material and piece-square evaluation. The search uses null-move pruning, killer-move and history-heuristic move ordering, and a transposition table, plus a repetition penalty at the root so it does not drift into drawish threefold repetitions against weak opponents. There are no model calls.

## Run it

From inside the unpacked kit directory (downloaded separately from make.fun):

```sh
node cli/makefun.mjs grade-local --kit . --bot ../.. --driver docker
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=1cd4be5d&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
