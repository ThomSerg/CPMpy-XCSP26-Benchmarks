# Benchmark Gist

## Experiments

| # | Experiment | Tracks | cpmpy commit | Created | Last Run | Solved |
|---|-----------|--------|--------------|---------|----------|--------|
| 1 | **baseline** 🔄 | XCSP3-2025-CSP25 | `45fc0181 — Deprecate old runner` | 2026-05-21 16:23:19 | 2026-05-22 10:34:17 | 379/1645 |

---

## baseline

_Tracks: unknown · cpmpy: `—` · Created: 2026-05-21 16:23:19 · Last run: 2026-05-22 10:34:17_

### Track: unknown

![unknown](./profile_baseline_unknown.svg)

#### Solve Status

| Solver | SAT | UNSAT | TIMEOUT | UNKNOWN | TOTAL |
|--------|-----|-------|---------|---------|-------|
| `ortools` | 73 | 24 | 2 | 101 | 200 |
| `exact` | 35 | 12 | 96 | 57 | 200 |
| `gurobi` | 33 | 14 | 55 | 98 | 200 |
| `pumpkin` | 38 | 7 | 25 | 130 | 200 |
| `z3` | 26 | 12 | 32 | 130 | 200 |
| `pindakaas` | 23 | 12 | 38 | 127 | 200 |
| `highs` | 20 | 10 | 71 | 99 | 200 |
| `scip` | 15 | 8 | 71 | 106 | 200 |
| `cpo` | 15 | 2 | 0 | 28 | 45 |

#### Solution Checker

| Solver | Valid | Invalid | Skipped | Total |
|--------|-------|---------|---------|-------|
| `ortools` | 0 | 0 | 200 | 200 |
| `exact` | 0 | 0 | 200 | 200 |
| `gurobi` | 153 | 0 | 47 | 200 |
| `pumpkin` | 0 | 0 | 200 | 200 |
| `z3` | 0 | 0 | 200 | 200 |
| `pindakaas` | 0 | 0 | 200 | 200 |
| `highs` | 0 | 0 | 200 | 200 |
| `scip` | 0 | 0 | 200 | 200 |
| `cpo` | 17 | 0 | 28 | 45 |
