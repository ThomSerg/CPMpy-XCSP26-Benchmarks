# Benchmark Gist

## Experiments

| # | Experiment | Tracks | cpmpy commit | Created | Last Run | Solved |
|---|-----------|--------|--------------|---------|----------|--------|
| 1 | **baseline** 🔄 | XCSP3-2025-CSP25 | `45fc0181 — Deprecate old runner` | 2026-05-21 16:23:19 | 2026-05-21 19:19:21 | 257/999 |

---

## baseline _(running)_

_Tracks: XCSP3-2025-CSP25 · cpmpy: `45fc0181 — Deprecate old runner` · Created: 2026-05-21 16:23:19 · Last run: 2026-05-21 19:19:21_

### Live Progress

| Solver | Track | Status | Progress | Started | Elapsed |
|--------|-------|--------|----------|---------|---------|
| `exact` | XCSP3-2025-CSP25 | ✅ done | 200/200 | 2026-05-21 16:59:21 | — |
| `highs` | XCSP3-2025-CSP25 | 🔄 running | 199/200 | 2026-05-21 18:43:07 | 36m 15s |
| `ortools` | XCSP3-2025-CSP25 | ⏳ pending | 200/200 | — | — |
| `pindakaas` | XCSP3-2025-CSP25 | ⏳ pending | 0/200 | — | — |
| `pumpkin` | XCSP3-2025-CSP25 | ✅ done | 200/200 | 2026-05-21 17:37:28 | — |
| `scip` | XCSP3-2025-CSP25 | ⏳ pending | 0/200 | — | — |
| `z3` | XCSP3-2025-CSP25 | ✅ done | 200/200 | 2026-05-21 18:07:56 | — |

### Track: XCSP3-2025-CSP25

![XCSP3-2025-CSP25](./profile_baseline_XCSP3-2025-CSP25.svg)

#### Solve Status

| Solver | SAT | UNSAT | TIMEOUT | UNKNOWN | TOTAL |
|--------|-----|-------|---------|---------|-------|
| `exact` | 35 | 12 | 96 | 57 | 200 |
| `highs` | 20 | 10 | 70 | 99 | 199 |
| `ortools` | 73 | 24 | 48 | 55 | 200 |
| `pumpkin` | 38 | 7 | 25 | 130 | 200 |
| `z3` | 26 | 12 | 32 | 130 | 200 |

#### Solution Checker

| Solver | Valid | Invalid | Skipped | Total |
|--------|-------|---------|---------|-------|
| `exact` | 0 | 0 | 200 | 200 |
| `highs` | 0 | 0 | 199 | 199 |
| `ortools` | 0 | 0 | 200 | 200 |
| `pumpkin` | 0 | 0 | 200 | 200 |
| `z3` | 0 | 0 | 200 | 200 |
