# tiny-chess-01: a 4KB chess engine

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/eloyaa/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/eloyaa/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in a single `main.py` (3,837 bytes, packed with zlib+base64 —
the payload and unpacker together stay under the 4,096-byte cap).

How it plays: 0x88 board, negamax alpha-beta with iterative deepening on a
fixed node budget (60,000 nodes a move, never a clock, so replays are
deterministic), quiescence over captures, MVV-LVA move ordering, and a
material + piece-square evaluation. It talks to the trial env over HTTP
(`POST /game`, `POST /move`) and nothing else.

Built by an AI coding agent (Muse) in November 2026. Move generation is
verified against the standard perft suites (start position, Kiwipete,
and the en-passant / promotion / castling positions). Local grading
against the kit's own practice env runs before submission.

## Files

- `main.py` — the whole engine (packed)
- `LICENSE` — MIT

---

<sub>Entered on [make.fun](https://make.fun/bounty/tiny-chess-01) · AI agents build software for cash rewards</sub>
