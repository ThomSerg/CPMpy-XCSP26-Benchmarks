# Benchmark Gist

Interactive site: https://ThomSerg.github.io/bench-gist-results/

## Experiments

| # | Experiment | Tracks | cpmpy commit | Created | Last Run | Solved |
|---|-----------|--------|--------------|---------|----------|--------|
| 1 | **NoOverlap via Cumulative linear decomp** | XCSP3-2025-CSP25 | `4566ba81 — Test: linear decomp nooverlap via cumulative` | 2026-05-29 10:57:41 | 2026-05-29 12:55:04 | 39/200 |
| 2 | **Positive MDD decomp** | XCSP3-2025-CSP25 | `85556f00 — Positive MDD test` | 2026-05-29 09:27:01 | 2026-05-29 09:57:51 | 40/200 |
| 3 | **Some transformation improvements - rerun** | XCSP3-2025-CSP25 | `6e268bb7 — Merge remote-tracking branch 'origin/master' into xcsp3_26` | 2026-05-28 16:55:01 | 2026-05-29 00:03:40 | 68/400 |
| 4 | **Table with MDD decomp** | XCSP3-2025-CSP25 | `3ed0f343 — Table global from master used in competition branch (to be able to use MDD decomposition)` | 2026-05-28 16:47:14 | 2026-05-29 05:10:05 | 397/1800 |
| 5 | **Some transformation improvements** | XCSP3-2025-CSP25 | `6e268bb7 — Merge remote-tracking branch 'origin/master' into xcsp3_26` | 2026-05-28 10:26:53 | 2026-05-28 15:47:34 | 435/1800 |
| 6 | **Use new MDD global in xcsp3 parser** | XCSP3-2025-COP25, XCSP3-2025-CSP25 | `—` | 2026-05-27 09:08:46 | 2026-05-27 20:08:47 | 1554/3800 |
| 7 | **MDD global** | XCSP3-2025-COP25, XCSP3-2025-CSP25 | `—` | 2026-05-26 16:50:39 | 2026-05-27 09:05:54 | 436/1807 |
| 8 | **linearize_reified_variables for OR-Tools** | XCSP3-2025-COP25, XCSP3-2025-CSP25 | `—` | 2026-05-26 13:50:16 | 2026-05-26 16:38:08 | 321/450 |
| 9 | **baseline** | XCSP3-2025-COP25, XCSP3-2025-CSP25 | `45fc0181 — Deprecate old runner` | 2026-05-21 16:23:19 | 2026-05-26 15:47:47 | 1519/3800 |
| 10 | **Submission 2025** | XCSP3-2025-CSP25 | `1e446eaf — Add count to second decompose_numerical location` | 2026-05-22 12:57:37 | 2026-05-22 22:44:59 | 210/1400 |

---

## NoOverlap via Cumulative linear decomp

_Tracks: XCSP3-2025-CSP25 · cpmpy: `4566ba81 — Test: linear decomp nooverlap via cumulative` · Created: 2026-05-29 10:57:41 · Last run: 2026-05-29 12:55:04_

### Track: XCSP3-2025-CSP25

#### Performance Profile

![XCSP3-2025-CSP25 profile](./profile_NoOverlap_via_Cumulative_linear_decomp_XCSP3-2025-CSP25.svg)

#### Solver Ranking

![XCSP3-2025-CSP25 ranking](./ranking_NoOverlap_via_Cumulative_linear_decomp_XCSP3-2025-CSP25.svg)

#### Solve Status

| Solver | SAT | UNSAT | TIMEOUT | UNKNOWN | TOTAL |
|--------|-----|-------|---------|---------|-------|
| `gurobi` | 25 | 14 | 23 | 138 | 200 |

#### Solution Checker

| Solver | Valid | Invalid | Skipped | Total |
|--------|-------|---------|---------|-------|
| `gurobi` | 111 | 0 | 89 | 200 |

---

## Positive MDD decomp

_Tracks: XCSP3-2025-CSP25 · cpmpy: `85556f00 — Positive MDD test` · Created: 2026-05-29 09:27:01 · Last run: 2026-05-29 09:57:51_

### Track: XCSP3-2025-CSP25

#### Performance Profile

![XCSP3-2025-CSP25 profile](./profile_Positive_MDD_decomp_XCSP3-2025-CSP25.svg)

#### Solver Ranking

![XCSP3-2025-CSP25 ranking](./ranking_Positive_MDD_decomp_XCSP3-2025-CSP25.svg)

#### Solve Status

| Solver | SAT | UNSAT | TIMEOUT | UNKNOWN | TOTAL |
|--------|-----|-------|---------|---------|-------|
| `gurobi` | 25 | 15 | 21 | 139 | 200 |

#### Solution Checker

| Solver | Valid | Invalid | Skipped | Total |
|--------|-------|---------|---------|-------|
| `gurobi` | 113 | 0 | 87 | 200 |

---

## Some transformation improvements - rerun

_Tracks: XCSP3-2025-CSP25 · cpmpy: `6e268bb7 — Merge remote-tracking branch 'origin/master' into xcsp3_26` · Created: 2026-05-28 16:55:01 · Last run: 2026-05-29 00:03:40_

### Track: XCSP3-2025-CSP25

#### Performance Profile

![XCSP3-2025-CSP25 profile](./profile_Some_transformation_improvements_-_rerun_XCSP3-2025-CSP25.svg)

#### Solver Ranking

![XCSP3-2025-CSP25 ranking](./ranking_Some_transformation_improvements_-_rerun_XCSP3-2025-CSP25.svg)

#### Solve Status

| Solver | SAT | UNSAT | TIMEOUT | UNKNOWN | TOTAL |
|--------|-----|-------|---------|---------|-------|
| `z3` | 24 | 13 | 26 | 137 | 200 |
| `highs` | 21 | 10 | 68 | 101 | 200 |

#### Solution Checker

| Solver | Valid | Invalid | Skipped | Total |
|--------|-------|---------|---------|-------|
| `z3` | 163 | 0 | 37 | 200 |
| `highs` | 106 | 0 | 94 | 200 |

---

## Table with MDD decomp

_Tracks: XCSP3-2025-CSP25 · cpmpy: `3ed0f343 — Table global from master used in competition branch (to be able to use MDD decomposition)` · Created: 2026-05-28 16:47:14 · Last run: 2026-05-29 05:10:05_

### Track: XCSP3-2025-CSP25

#### Performance Profile

![XCSP3-2025-CSP25 profile](./profile_Table_with_MDD_decomp_XCSP3-2025-CSP25.svg)

#### Solver Ranking

![XCSP3-2025-CSP25 ranking](./ranking_Table_with_MDD_decomp_XCSP3-2025-CSP25.svg)

#### Solve Status

| Solver | SAT | UNSAT | TIMEOUT | UNKNOWN | TOTAL |
|--------|-----|-------|---------|---------|-------|
| `ortools` | 76 | 25 | 2 | 97 | 200 |
| `cpo` | 63 | 9 | 10 | 118 | 200 |
| `pumpkin` | 36 | 5 | 28 | 131 | 200 |
| `exact` | 27 | 11 | 52 | 110 | 200 |
| `gurobi` | 24 | 14 | 25 | 137 | 200 |
| `z3` | 25 | 13 | 14 | 148 | 200 |
| `pindakaas` | 17 | 13 | 7 | 163 | 200 |
| `highs` | 13 | 10 | 34 | 143 | 200 |
| `scip` | 8 | 8 | 43 | 141 | 200 |

#### Solution Checker

| Solver | Valid | Invalid | Skipped | Total |
|--------|-------|---------|---------|-------|
| `ortools` | 174 | 0 | 26 | 200 |
| `cpo` | 173 | 0 | 27 | 200 |
| `pumpkin` | 168 | 0 | 32 | 200 |
| `exact` | 76 | 0 | 124 | 200 |
| `gurobi` | 110 | 0 | 90 | 200 |
| `z3` | 166 | 0 | 34 | 200 |
| `pindakaas` | 73 | 0 | 127 | 200 |
| `highs` | 93 | 0 | 107 | 200 |
| `scip` | 80 | 0 | 120 | 200 |

---

## Some transformation improvements

_Tracks: XCSP3-2025-CSP25 · cpmpy: `6e268bb7 — Merge remote-tracking branch 'origin/master' into xcsp3_26` · Created: 2026-05-28 10:26:53 · Last run: 2026-05-28 15:47:34_

### Track: XCSP3-2025-CSP25

#### Performance Profile

![XCSP3-2025-CSP25 profile](./profile_Some_transformation_improvements_XCSP3-2025-CSP25.svg)

#### Solver Ranking

![XCSP3-2025-CSP25 ranking](./ranking_Some_transformation_improvements_XCSP3-2025-CSP25.svg)

#### Solve Status

| Solver | SAT | UNSAT | TIMEOUT | UNKNOWN | TOTAL |
|--------|-----|-------|---------|---------|-------|
| `ortools` | 75 | 24 | 2 | 99 | 200 |
| `cpo` | 62 | 8 | 9 | 121 | 200 |
| `exact` | 37 | 13 | 99 | 51 | 200 |
| `gurobi` | 34 | 14 | 70 | 82 | 200 |
| `pumpkin` | 36 | 6 | 29 | 129 | 200 |
| `z3` | 24 | 13 | 31 | 132 | 200 |
| `pindakaas` | 24 | 12 | 35 | 129 | 200 |
| `highs` | 20 | 10 | 70 | 100 | 200 |
| `scip` | 14 | 9 | 76 | 101 | 200 |

#### Solution Checker

| Solver | Valid | Invalid | Skipped | Total |
|--------|-------|---------|---------|-------|
| `ortools` | 174 | 0 | 26 | 200 |
| `cpo` | 173 | 0 | 27 | 200 |
| `exact` | 87 | 0 | 113 | 200 |
| `gurobi` | 151 | 0 | 49 | 200 |
| `pumpkin` | 168 | 0 | 32 | 200 |
| `z3` | 163 | 0 | 37 | 200 |
| `pindakaas` | 98 | 0 | 102 | 200 |
| `highs` | 105 | 0 | 95 | 200 |
| `scip` | 89 | 0 | 111 | 200 |

---

## Use new MDD global in xcsp3 parser

_Tracks: XCSP3-2025-COP25, XCSP3-2025-CSP25 · cpmpy: `—` · Created: 2026-05-27 09:08:46 · Last run: 2026-05-27 20:08:47_

### Track: XCSP3-2025-CSP25

#### Performance Profile

![XCSP3-2025-CSP25 profile](./profile_Use_new_MDD_global_in_xcsp3_parser_XCSP3-2025-CSP25.svg)

#### Solver Ranking

![XCSP3-2025-CSP25 ranking](./ranking_Use_new_MDD_global_in_xcsp3_parser_XCSP3-2025-CSP25.svg)

#### Solve Status

| Solver | SAT | UNSAT | TIMEOUT | UNKNOWN | TOTAL |
|--------|-----|-------|---------|---------|-------|
| `ortools` | 74 | 24 | 5 | 97 | 200 |
| `cpo` | 62 | 9 | 12 | 117 | 200 |
| `exact` | 35 | 12 | 99 | 54 | 200 |
| `gurobi` | 32 | 13 | 69 | 86 | 200 |
| `pumpkin` | 38 | 6 | 32 | 124 | 200 |
| `z3` | 26 | 12 | 29 | 133 | 200 |
| `pindakaas` | 23 | 12 | 34 | 131 | 200 |
| `highs` | 20 | 10 | 71 | 99 | 200 |
| `scip` | 11 | 8 | 69 | 112 | 200 |

#### Solution Checker

| Solver | Valid | Invalid | Skipped | Total |
|--------|-------|---------|---------|-------|
| `ortools` | 174 | 0 | 26 | 200 |
| `cpo` | 174 | 0 | 26 | 200 |
| `exact` | 85 | 0 | 115 | 200 |
| `gurobi` | 149 | 0 | 51 | 200 |
| `pumpkin` | 167 | 0 | 33 | 200 |
| `z3` | 159 | 0 | 41 | 200 |
| `pindakaas` | 98 | 0 | 102 | 200 |
| `highs` | 106 | 0 | 94 | 200 |
| `scip` | 97 | 0 | 103 | 200 |

### Track: XCSP3-2025-COP25

#### Performance Profile

![XCSP3-2025-COP25 profile](./profile_Use_new_MDD_global_in_xcsp3_parser_XCSP3-2025-COP25.svg)

#### Solver Ranking

![XCSP3-2025-COP25 ranking](./ranking_Use_new_MDD_global_in_xcsp3_parser_XCSP3-2025-COP25.svg)

#### Solve Status

| Solver | SAT | UNSAT | TIMEOUT | UNKNOWN | TOTAL |
|--------|-----|-------|---------|---------|-------|
| `ortools` | 202 | 22 | 5 | 21 | 250 |
| `cpo` | 164 | 20 | 36 | 30 | 250 |
| `gurobi` | 148 | 17 | 52 | 33 | 250 |
| `highs` | 113 | 12 | 75 | 50 | 250 |
| `scip` | 97 | 14 | 68 | 71 | 250 |
| `z3` | 94 | 16 | 54 | 86 | 250 |
| `exact` | 88 | 17 | 122 | 23 | 250 |
| `pumpkin` | 102 | 1 | 24 | 123 | 250 |

#### Solution Checker

| Solver | Valid | Invalid | Skipped | Total |
|--------|-------|---------|---------|-------|
| `ortools` | 228 | 0 | 22 | 250 |
| `cpo` | 192 | 0 | 58 | 250 |
| `gurobi` | 191 | 0 | 59 | 250 |
| `highs` | 162 | 0 | 88 | 250 |
| `scip` | 142 | 0 | 108 | 250 |
| `z3` | 175 | 0 | 75 | 250 |
| `exact` | 107 | 0 | 143 | 250 |
| `pumpkin` | 153 | 0 | 97 | 250 |

---

## MDD global

_Tracks: XCSP3-2025-COP25, XCSP3-2025-CSP25 · cpmpy: `—` · Created: 2026-05-26 16:50:39 · Last run: 2026-05-27 09:05:54_

### Track: XCSP3-2025-CSP25

#### Performance Profile

![XCSP3-2025-CSP25 profile](./profile_MDD_global_XCSP3-2025-CSP25.svg)

#### Solver Ranking

![XCSP3-2025-CSP25 ranking](./ranking_MDD_global_XCSP3-2025-CSP25.svg)

#### Solve Status

| Solver | SAT | UNSAT | TIMEOUT | UNKNOWN | TOTAL |
|--------|-----|-------|---------|---------|-------|
| `ortools` | 73 | 24 | 4 | 99 | 200 |
| `cpo` | 61 | 8 | 11 | 120 | 200 |
| `exact` | 35 | 12 | 101 | 52 | 200 |
| `gurobi` | 32 | 13 | 68 | 87 | 200 |
| `pumpkin` | 38 | 6 | 30 | 126 | 200 |
| `z3` | 27 | 12 | 34 | 127 | 200 |
| `pindakaas` | 23 | 12 | 36 | 129 | 200 |
| `highs` | 21 | 10 | 71 | 98 | 200 |
| `scip` | 14 | 8 | 77 | 101 | 200 |

#### Solution Checker

| Solver | Valid | Invalid | Skipped | Total |
|--------|-------|---------|---------|-------|
| `ortools` | 174 | 0 | 26 | 200 |
| `cpo` | 173 | 0 | 27 | 200 |
| `exact` | 86 | 0 | 114 | 200 |
| `gurobi` | 146 | 0 | 54 | 200 |
| `pumpkin` | 168 | 0 | 32 | 200 |
| `z3` | 160 | 0 | 40 | 200 |
| `pindakaas` | 96 | 0 | 104 | 200 |
| `highs` | 110 | 0 | 90 | 200 |
| `scip` | 93 | 0 | 107 | 200 |

### Track: XCSP3-2025-COP25

#### Performance Profile

![XCSP3-2025-COP25 profile](./profile_MDD_global_XCSP3-2025-COP25.svg)

#### Solver Ranking

![XCSP3-2025-COP25 ranking](./ranking_MDD_global_XCSP3-2025-COP25.svg)

#### Solve Status

| Solver | SAT | UNSAT | TIMEOUT | UNKNOWN | TOTAL |
|--------|-----|-------|---------|---------|-------|
| `ortools` | 7 | 0 | 0 | 0 | 7 |

#### Solution Checker

| Solver | Valid | Invalid | Skipped | Total |
|--------|-------|---------|---------|-------|
| `ortools` | 7 | 0 | 0 | 7 |

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
