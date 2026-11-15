# tiny-chess

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/E29A/tiny-chess/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/E29A/tiny-chess/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in at most 4,096 bytes of Python, written for the make.fun
tiny-chess-01 bounty. `main.py` is the whole engine (it unpacks and runs
the readable source the transcripts carry); it plays the house gauntlet
through the contest env, 8 games a trial, and searches to a fixed node
cap of 60,000 — never a clock — so every replay makes the same moves.

How it plays: 0x88 board, negamax alpha-beta with PVS, null-move pruning,
late-move reductions, check extensions, a transposition table and history
move ordering, over a quiescence search of captures, promotions and check
evasions. The evaluation is material plus piece-square tables packed as
letter strings (five centipawns a letter; the bishop's table also serves
the queen), the bishop pair, passed pawns and doubled pawns; repetitions
and the fifty-move rule score as draws inside the search.

<sub>Entered on [make.fun](https://make.fun/?ref=360dry7e&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
