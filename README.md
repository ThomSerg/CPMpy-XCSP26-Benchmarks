# Benchmark Gist

## Experiments

| # | Experiment | Tracks | cpmpy commit | Created | Last Run | Solved |
|---|-----------|--------|--------------|---------|----------|--------|
| 1 | **baseline** 🔄 | XCSP3-2025-CSP25 | `45fc0181 — Deprecate old runner` | 2026-05-21 16:23:19 | 2026-05-22 10:34:03 | 362/1600 |

---

## baseline _(running)_

_Tracks: XCSP3-2025-CSP25 · cpmpy: `45fc0181 — Deprecate old runner` · Created: 2026-05-21 16:23:19 · Last run: 2026-05-22 10:34:03_

### Live Progress

| Solver | Track | Status | Progress | Started | Elapsed |
|--------|-------|--------|----------|---------|---------|
| `ortools` | XCSP3-2025-CSP25 | ✅ done | 200/200 | 2026-05-21 20:25:09 | — |
| `exact` | XCSP3-2025-CSP25 | ✅ done | 200/200 | 2026-05-21 16:59:21 | — |
| `gurobi` | XCSP3-2025-CSP25 | ✅ done | 200/200 | 2026-05-22 09:28:32 | — |
| `pumpkin` | XCSP3-2025-CSP25 | ✅ done | 200/200 | 2026-05-21 17:37:28 | — |
| `z3` | XCSP3-2025-CSP25 | ✅ done | 200/200 | 2026-05-21 18:07:56 | — |
| `pindakaas` | XCSP3-2025-CSP25 | ✅ done | 200/200 | 2026-05-21 19:54:47 | — |
| `highs` | XCSP3-2025-CSP25 | ✅ done | 200/200 | 2026-05-21 18:43:07 | — |
| `scip` | XCSP3-2025-CSP25 | ✅ done | 200/200 | 2026-05-21 19:19:25 | — |
| `cpo` | XCSP3-2025-CSP25 | ⏳ pending | 0/200 | — | — |

### Track: XCSP3-2025-CSP25

![XCSP3-2025-CSP25](./profile_baseline_XCSP3-2025-CSP25.svg)

#### Solve Status

| Solver | SAT | UNSAT | TIMEOUT | UNKNOWN | TOTAL |
|--------|-----|-------|---------|---------|-------|
| `ortools` | 73 | 24 | 2 | 101 | 200 |
| `exact` | 35 | 12 | 96 | 57 | 200 |
| `gurobi` | 33 | 14 | 53 | 100 | 200 |
| `pumpkin` | 38 | 7 | 25 | 130 | 200 |
| `z3` | 26 | 12 | 32 | 130 | 200 |
| `pindakaas` | 23 | 12 | 38 | 127 | 200 |
| `highs` | 20 | 10 | 71 | 99 | 200 |
| `scip` | 15 | 8 | 71 | 106 | 200 |

#### Solution Checker

| Solver | Valid | Invalid | Skipped | Total |
|--------|-------|---------|---------|-------|
| `ortools` | 0 | 0 | 200 | 200 |
| `exact` | 0 | 0 | 200 | 200 |
| `gurobi` | 151 | 0 | 49 | 200 |
| `pumpkin` | 0 | 0 | 200 | 200 |
| `z3` | 0 | 0 | 200 | 200 |
| `pindakaas` | 0 | 0 | 200 | 200 |
| `highs` | 0 | 0 | 200 | 200 |
| `scip` | 0 | 0 | 200 | 200 |
