# Benchmark Gist

Interactive site: https://ThomSerg.github.io/bench-gist-results/

## Experiments

| # | Experiment | Tracks | cpmpy commit | Created | Last Run | Solved |
|---|-----------|--------|--------------|---------|----------|--------|
| 1 | **MDD global** 🔄 | XCSP3-2025-CSP25 | `—` | 2026-05-26 16:50:39 | 2026-05-26 18:49:04 | 268/888 |
| 2 | **linearize_reified_variables for OR-Tools** | XCSP3-2025-COP25, XCSP3-2025-CSP25 | `—` | 2026-05-26 13:50:16 | 2026-05-26 16:38:08 | 321/450 |
| 3 | **baseline** | XCSP3-2025-COP25, XCSP3-2025-CSP25 | `45fc0181 — Deprecate old runner` | 2026-05-21 16:23:19 | 2026-05-26 15:47:47 | 1519/3800 |
| 4 | **Submission 2025** | XCSP3-2025-CSP25 | `1e446eaf — Add count to second decompose_numerical location` | 2026-05-22 12:57:37 | 2026-05-22 22:44:59 | 210/1400 |

---

## MDD global _(running)_

_Tracks: XCSP3-2025-CSP25 · cpmpy: `—` · Created: 2026-05-26 16:50:39 · Last run: 2026-05-26 18:49:04_

### Live Progress

| Solver | Track | Status | Progress | Started | Elapsed |
|--------|-------|--------|----------|---------|---------|
| `ortools` | XCSP3-2025-CSP25 | ✅ done | 200/200 | 2026-05-26 16:50:52 | — |
| `exact` | XCSP3-2025-CSP25 | ✅ done | 200/200 | 2026-05-26 17:15:15 | — |
| `gurobi` | XCSP3-2025-CSP25 | ✅ done | 200/200 | 2026-05-26 17:47:22 | — |
| `pumpkin` | XCSP3-2025-CSP25 | ✅ done | 200/200 | 2026-05-26 18:18:37 | — |
| `z3` | XCSP3-2025-CSP25 | 🔄 running | 88/200 | 2026-05-26 18:49:13 | 16m 41s |
| `cpo` | XCSP3-2025-CSP25 | ⏳ pending | 0/200 | — | — |
| `highs` | XCSP3-2025-CSP25 | ⏳ pending | 0/200 | — | — |
| `pindakaas` | XCSP3-2025-CSP25 | ⏳ pending | 0/200 | — | — |
| `scip` | XCSP3-2025-CSP25 | ⏳ pending | 0/200 | — | — |

### Track: XCSP3-2025-CSP25

#### Performance Profile

![XCSP3-2025-CSP25 profile](./profile_MDD_global_XCSP3-2025-CSP25.svg)

#### Solver Ranking

![XCSP3-2025-CSP25 ranking](./ranking_MDD_global_XCSP3-2025-CSP25.svg)

#### Solve Status

| Solver | SAT | UNSAT | TIMEOUT | UNKNOWN | TOTAL |
|--------|-----|-------|---------|---------|-------|
| `ortools` | 73 | 24 | 4 | 99 | 200 |
| `exact` | 35 | 12 | 101 | 52 | 200 |
| `gurobi` | 32 | 13 | 68 | 87 | 200 |
| `pumpkin` | 38 | 6 | 30 | 126 | 200 |
| `z3` | 25 | 10 | 3 | 50 | 88 |

#### Solution Checker

| Solver | Valid | Invalid | Skipped | Total |
|--------|-------|---------|---------|-------|
| `ortools` | 174 | 0 | 26 | 200 |
| `exact` | 86 | 0 | 114 | 200 |
| `gurobi` | 146 | 0 | 54 | 200 |
| `pumpkin` | 168 | 0 | 32 | 200 |
| `z3` | 77 | 0 | 11 | 88 |

---

## linearize_reified_variables for OR-Tools

_Tracks: XCSP3-2025-COP25, XCSP3-2025-CSP25 · cpmpy: `—` · Created: 2026-05-26 13:50:16 · Last run: 2026-05-26 16:38:08_

### Track: XCSP3-2025-COP25

#### Performance Profile

![XCSP3-2025-COP25 profile](./profile_linearize_reified_variables_for_OR-Tools_XCSP3-2025-COP25.svg)

#### Solver Ranking

![XCSP3-2025-COP25 ranking](./ranking_linearize_reified_variables_for_OR-Tools_XCSP3-2025-COP25.svg)

#### Solve Status

| Solver | SAT | UNSAT | TIMEOUT | UNKNOWN | TOTAL |
|--------|-----|-------|---------|---------|-------|
| `ortools` | 203 | 22 | 2 | 23 | 250 |

#### Solution Checker

| Solver | Valid | Invalid | Skipped | Total |
|--------|-------|---------|---------|-------|
| `ortools` | 229 | 0 | 21 | 250 |

### Track: XCSP3-2025-CSP25

#### Performance Profile

![XCSP3-2025-CSP25 profile](./profile_linearize_reified_variables_for_OR-Tools_XCSP3-2025-CSP25.svg)

#### Solver Ranking

![XCSP3-2025-CSP25 ranking](./ranking_linearize_reified_variables_for_OR-Tools_XCSP3-2025-CSP25.svg)

#### Solve Status

| Solver | SAT | UNSAT | TIMEOUT | UNKNOWN | TOTAL |
|--------|-----|-------|---------|---------|-------|
| `ortools` | 72 | 24 | 2 | 102 | 200 |

#### Solution Checker

| Solver | Valid | Invalid | Skipped | Total |
|--------|-------|---------|---------|-------|
| `ortools` | 171 | **3** | 26 | 200 |

---

## baseline

_Tracks: XCSP3-2025-COP25, XCSP3-2025-CSP25 · cpmpy: `45fc0181 — Deprecate old runner` · Created: 2026-05-21 16:23:19 · Last run: 2026-05-26 15:47:47_

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
| `ortools` | 202 | 22 | 4 | 22 | 250 |
| `cpo` | 170 | 16 | 27 | 37 | 250 |
| `gurobi` | 149 | 14 | 31 | 56 | 250 |
| `highs` | 114 | 9 | 67 | 60 | 250 |
| `exact` | 97 | 13 | 99 | 41 | 250 |
| `z3` | 96 | 13 | 48 | 93 | 250 |
| `scip` | 98 | 10 | 51 | 91 | 250 |
| `pumpkin` | 103 | 0 | 21 | 126 | 250 |

#### Solution Checker

| Solver | Valid | Invalid | Skipped | Total |
|--------|-------|---------|---------|-------|
| `ortools` | 228 | 0 | 22 | 250 |
| `cpo` | 193 | **4** | 53 | 250 |
| `gurobi` | 189 | **2** | 59 | 250 |
| `highs` | 165 | 0 | 85 | 250 |
| `exact` | 107 | **1** | 142 | 250 |
| `z3` | 174 | **2** | 74 | 250 |
| `scip` | 143 | 0 | 107 | 250 |
| `pumpkin` | 151 | **2** | 97 | 250 |

---

## Submission 2025

_Tracks: XCSP3-2025-CSP25 · cpmpy: `1e446eaf — Add count to second decompose_numerical location` · Created: 2026-05-22 12:57:37 · Last run: 2026-05-22 22:44:59_

### Track: XCSP3-2025-CSP25

#### Performance Profile

![XCSP3-2025-CSP25 profile](./profile_Submission_2025_XCSP3-2025-CSP25.svg)

#### Solver Ranking

![XCSP3-2025-CSP25 ranking](./ranking_Submission_2025_XCSP3-2025-CSP25.svg)

#### Solve Status

| Solver | SAT | UNSAT | TIMEOUT | UNKNOWN | TOTAL |
|--------|-----|-------|---------|---------|-------|
| `ortools` | 72 | 21 | 1 | 106 | 200 |
| `z3` | 23 | 13 | 6 | 158 | 200 |
| `gurobi` | 20 | 12 | 15 | 153 | 200 |
| `cpo` | 21 | 5 | 1 | 173 | 200 |
| `exact` | 20 | 3 | 38 | 139 | 200 |
| `pumpkin` | 0 | 0 | 0 | 200 | 200 |
| `scip` | 0 | 0 | 0 | 200 | 200 |

#### Solution Checker

| Solver | Valid | Invalid | Skipped | Total |
|--------|-------|---------|---------|-------|
| `ortools` | 79 | 0 | 121 | 200 |
| `z3` | 83 | 0 | 117 | 200 |
| `gurobi` | 81 | 0 | 119 | 200 |
| `cpo` | 47 | 0 | 153 | 200 |
| `exact` | 30 | 0 | 170 | 200 |
| `pumpkin` | 0 | 0 | 200 | 200 |
| `scip` | 0 | 0 | 200 | 200 |
