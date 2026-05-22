# Benchmark Gist

Interactive site: https://ThomSerg.github.io/bench-gist-results/

## Experiments

| # | Experiment | Tracks | cpmpy commit | Created | Last Run | Solved |
|---|-----------|--------|--------------|---------|----------|--------|
| 1 | **baseline** | XCSP3-2025-COP25, XCSP3-2025-CSP25 | `45fc0181 — Deprecate old runner` | 2026-05-21 16:23:19 | 2026-05-22 15:30:41 | 450/1857 |
| 2 | **Submission 2025** 🔄 | XCSP3-2025-CSP25 | `1e446eaf — Add count to second decompose_numerical location` | 2026-05-22 12:57:37 | 2026-05-22 15:36:51 | 113/400 |

---

## baseline

_Tracks: XCSP3-2025-COP25, XCSP3-2025-CSP25 · cpmpy: `45fc0181 — Deprecate old runner` · Created: 2026-05-21 16:23:19 · Last run: 2026-05-22 15:30:41_

### Track: XCSP3-2025-CSP25

#### Performance Profile

![XCSP3-2025-CSP25 profile](./profile_baseline_XCSP3-2025-CSP25.svg)

#### Solver Ranking

![XCSP3-2025-CSP25 ranking](./ranking_baseline_XCSP3-2025-CSP25.svg)

#### Solve Status

| Solver | SAT | UNSAT | TIMEOUT | UNKNOWN | TOTAL |
|--------|-----|-------|---------|---------|-------|
| `ortools` | 73 | 24 | 4 | 99 | 200 |
| `exact` | 35 | 12 | 96 | 57 | 200 |
| `gurobi` | 33 | 14 | 55 | 98 | 200 |
| `pumpkin` | 38 | 7 | 25 | 130 | 200 |
| `z3` | 26 | 12 | 32 | 130 | 200 |
| `pindakaas` | 23 | 12 | 38 | 127 | 200 |
| `cpo` | 26 | 5 | 1 | 168 | 200 |
| `highs` | 20 | 10 | 71 | 99 | 200 |
| `scip` | 15 | 8 | 71 | 106 | 200 |

#### Solution Checker

| Solver | Valid | Invalid | Skipped | Total |
|--------|-------|---------|---------|-------|
| `ortools` | 171 | **3** | 26 | 200 |
| `exact` | 0 | 0 | 200 | 200 |
| `gurobi` | 153 | 0 | 47 | 200 |
| `pumpkin` | 0 | 0 | 200 | 200 |
| `z3` | 0 | 0 | 200 | 200 |
| `pindakaas` | 0 | 0 | 200 | 200 |
| `cpo` | 75 | 0 | 125 | 200 |
| `highs` | 0 | 0 | 200 | 200 |
| `scip` | 0 | 0 | 200 | 200 |

### Track: XCSP3-2025-COP25

#### Performance Profile

![XCSP3-2025-COP25 profile](./profile_baseline_XCSP3-2025-COP25.svg)

#### Solver Ranking

![XCSP3-2025-COP25 ranking](./ranking_baseline_XCSP3-2025-COP25.svg)

#### Solve Status

| Solver | SAT | UNSAT | TIMEOUT | UNKNOWN | TOTAL |
|--------|-----|-------|---------|---------|-------|
| `ortools` | 57 | 0 | 0 | 0 | 57 |

#### Solution Checker

| Solver | Valid | Invalid | Skipped | Total |
|--------|-------|---------|---------|-------|
| `ortools` | 57 | 0 | 0 | 57 |

---

## Submission 2025 _(running)_

_Tracks: XCSP3-2025-CSP25 · cpmpy: `1e446eaf — Add count to second decompose_numerical location` · Created: 2026-05-22 12:57:37 · Last run: 2026-05-22 15:36:51_

### Live Progress

| Solver | Track | Status | Progress | Started | Elapsed |
|--------|-------|--------|----------|---------|---------|
| `ortools` | XCSP3-2025-CSP25 | ✅ done | 200/200 | — | — |
| `exact` | XCSP3-2025-CSP25 | 🔄 running | 200/200 | 2026-05-22 15:42:28 | 16m 23s |

### Track: XCSP3-2025-CSP25

#### Performance Profile

![XCSP3-2025-CSP25 profile](./profile_Submission_2025_XCSP3-2025-CSP25.svg)

#### Solver Ranking

![XCSP3-2025-CSP25 ranking](./ranking_Submission_2025_XCSP3-2025-CSP25.svg)

#### Solve Status

| Solver | SAT | UNSAT | TIMEOUT | UNKNOWN | TOTAL |
|--------|-----|-------|---------|---------|-------|
| `ortools` | 72 | 21 | 1 | 106 | 200 |
| `exact` | 18 | 2 | 9 | 171 | 200 |

#### Solution Checker

| Solver | Valid | Invalid | Skipped | Total |
|--------|-------|---------|---------|-------|
| `ortools` | 79 | 0 | 121 | 200 |
| `exact` | 18 | 0 | 182 | 200 |
