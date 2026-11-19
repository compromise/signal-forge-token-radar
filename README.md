# Token Radar

A deterministic, offline-first pre-token protocol radar for the make.fun `token-radar-01` competition.

[![make.fun competition](https://make.fun/badge/token-radar-01.svg)](https://make.fun/bounty/token-radar-01)

## What it does

Token Radar ranks every protocol in the sealed snapshot with a transparent implied-value model, keeps the full watchlist covered, and gives each row a conservative farm plan with explicit capital, time, and safety steps. The static dashboard is self-contained: no network requests, no runtime dependencies, and the same input produces byte-identical output.

## Run

```bash
mkdir -p out
MAKEFUN_OUTPUT_DIR=out node main.ts --input input/snapshot.json
```

The output contains `board.json`, `dashboard/`, three screenshots, and the judge dossier.

## Model

Implied value combines TVL, capped seven-day change, and an age-based maturity factor. The dashboard shows the model inputs and recomputes the displayed value in-browser so the table and methodology stay aligned.
