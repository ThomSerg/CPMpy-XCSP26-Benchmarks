# Submission 2025

```js
import * as Plot from "npm:@observablehq/plot";
const results = await FileAttachment("../data/results.csv").csv({typed: true});
const summary = await FileAttachment("../data/solver_summary.csv").csv({typed: true});
const curves = await FileAttachment("../data/curves.json").json();
const sessionSlug = "Submission_2025";
const sessionResults = results.filter(d => d.session_slug === sessionSlug);
const sessionSummary = summary.filter(d => d.session_slug === sessionSlug);
const tracks = Array.from(new Set(sessionResults.map(d => d.track))).sort();
```

```js
const selectedTrack = view(Inputs.select(tracks, {label: "Track"}));
```

```js
const activeTrack = tracks.includes(selectedTrack) ? selectedTrack : tracks[0];
const trackResults = activeTrack
  ? sessionResults.filter(d => d.track === activeTrack)
  : sessionResults;
const trackSummary = activeTrack
  ? sessionSummary.filter(d => d.track === activeTrack)
  : sessionSummary;
const solvers = Array.from(new Set(trackResults.map(d => d.solver))).sort();
```

```js
const selectedSolverInput = view(Inputs.checkbox(solvers, {
  label: "Solvers",
  value: solvers
}));
```

```js
const selectedSolverValues =
  Array.isArray(selectedSolverInput) ? selectedSolverInput
  : selectedSolverInput instanceof Set ? Array.from(selectedSolverInput)
  : typeof selectedSolverInput === "string" ? [selectedSolverInput]
  : selectedSolverInput && typeof selectedSolverInput[Symbol.iterator] === "function" ? Array.from(selectedSolverInput)
  : [];
const activeSolvers = selectedSolverValues
  .filter(s => typeof s === "string" && solvers.includes(s));
const visibleSolvers = activeSolvers.length ? activeSolvers : solvers;
```

```js
const trackCurves = curves.sessions?.[sessionSlug]?.tracks?.[activeTrack]?.completion?.series ?? [];
const allSolverNames = Array.from(new Set(sessionResults.map(d => d.solver))).sort();
const solverPalette = [
  "#2563eb", "#dc2626", "#16a34a", "#9333ea", "#ea580c",
  "#0891b2", "#be123c", "#4d7c0f", "#7c3aed", "#ca8a04",
  "#0f766e", "#c2410c", "#1d4ed8", "#a21caf", "#15803d"
];
const solverColor = new Map(allSolverNames.map((solver, i) => [
  solver,
  solverPalette[i % solverPalette.length]
]));
const curveRows = trackCurves
  .filter(s => visibleSolvers.includes(s.solver))
  .flatMap(s => s.x.map((x, i) => ({
    solver: s.solver,
    seconds: x,
    solved: s.y[i],
    label: `${s.solver}\n${x.toFixed(1)}s: ${s.y[i]} solved`
  })));
display(Plot.plot({
  height: 420,
  x: {label: "Time (s)", grid: true},
  y: {label: "Instances solved", grid: true},
  color: {
    domain: allSolverNames,
    range: allSolverNames.map(s => solverColor.get(s)),
    legend: true
  },
  marks: [
    Plot.lineY(curveRows, {
      x: "seconds",
      y: "solved",
      stroke: "solver",
      curve: "step-after",
      strokeWidth: 2.25,
      title: "label"
    }),
    Plot.ruleY([0])
  ]
}));
```

## Ranking

```js
const ranking = trackSummary
  .filter(d => visibleSolvers.includes(d.solver))
  .map(d => ({...d, solved: d.sat + d.unsat}))
  .sort((a, b) => b.solved - a.solved || a.solver.localeCompare(b.solver));
display(Inputs.table(ranking, {
  columns: ["solver", "solved", "sat", "unsat", "timeout", "unknown", "total", "checker_valid", "checker_invalid"]
}));
```

## Results

```js
display(Inputs.table(trackResults
  .filter(d => visibleSolvers.includes(d.solver)), {
  columns: ["solver", "instance", "status", "seconds", "objective", "checker_valid", "termination_reason"]
}));
```
