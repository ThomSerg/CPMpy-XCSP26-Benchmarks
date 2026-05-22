# baseline

```js
const results = await FileAttachment("../data/results.csv").csv({typed: true});
const summary = await FileAttachment("../data/solver_summary.csv").csv({typed: true});
const curves = await FileAttachment("../data/curves.json").json();
const sessionSlug = "baseline";
const sessionResults = results.filter(d => d.session_slug === sessionSlug);
const sessionSummary = summary.filter(d => d.session_slug === sessionSlug);
const tracks = Array.from(new Set(sessionResults.map(d => d.track))).sort();
```

```js
const track = view(Inputs.select(tracks, {label: "Track"}));
const solvers = Array.from(new Set(sessionResults.filter(d => d.track === track).map(d => d.solver))).sort();
const selectedSolvers = view(Inputs.checkbox(solvers, {label: "Solvers", value: solvers}));
```

```js
const trackCurves = curves.sessions?.[sessionSlug]?.tracks?.[track]?.completion?.series ?? [];
const curveRows = trackCurves
  .filter(s => selectedSolvers.includes(s.solver))
  .flatMap(s => s.x.map((x, i) => ({solver: s.solver, seconds: x, solved: s.y[i]})));
display(Plot.plot({
  height: 420,
  x: {label: "Time (s)", grid: true},
  y: {label: "Instances solved", grid: true},
  color: {legend: true},
  marks: [
    Plot.lineY(curveRows, {x: "seconds", y: "solved", stroke: "solver", curve: "step-after", strokeWidth: 2}),
    Plot.ruleY([0])
  ]
}));
```

## Ranking

```js
const ranking = sessionSummary
  .filter(d => d.track === track && selectedSolvers.includes(d.solver))
  .map(d => ({...d, solved: d.sat + d.unsat}))
  .sort((a, b) => b.solved - a.solved || a.solver.localeCompare(b.solver));
display(Inputs.table(ranking, {
  columns: ["solver", "solved", "sat", "unsat", "timeout", "unknown", "total", "checker_valid", "checker_invalid"]
}));
```

## Results

```js
display(Inputs.table(sessionResults
  .filter(d => d.track === track && selectedSolvers.includes(d.solver)), {
  columns: ["solver", "instance", "status", "seconds", "objective", "checker_valid", "termination_reason"]
}));
```
