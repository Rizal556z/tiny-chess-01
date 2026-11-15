# Tiny Chess Engine

A 4 KB Python chess engine for the make.fun tiny-chess-01 bounty:
strongest engine in 4,096 bytes.

`main.py` is the whole engine (alpha-beta + quiescence, transposition
table, null-move pruning, history/killer ordering, endgame king table).
It plays over HTTP against the make.fun environment (`MAKEFUN_ENV_URL`).

Pure Python standard library only. No model calls, no clock-based
decisions: every search uses a fixed node budget, so play is fully
deterministic and replayable.
