# Compare Sessions

```js
import * as Plot from "npm:@observablehq/plot";
const sessions = await FileAttachment("data/sessions.csv").csv({typed: true});
const results = await FileAttachment("data/results.csv").csv({typed: true});
const curves = await FileAttachment("data/curves.json").json();
```

```js
const baseline = view(Inputs.select(sessions, {label: "Baseline", format: d => d.name}));
const candidate = view(Inputs.select(sessions, {label: "Candidate", value: sessions[0], format: d => d.name}));
```

```js
const baselineRows = results.filter(d => d.session_slug === baseline.slug);
const candidateRows = results.filter(d => d.session_slug === candidate.slug);
const baselineTracks = new Set(baselineRows.map(d => d.track));
const candidateTracks = new Set(candidateRows.map(d => d.track));
const commonTracks = [...baselineTracks].filter(t => candidateTracks.has(t)).sort();
const allTracks = Array.from(new Set([...baselineTracks, ...candidateTracks])).sort();
const trackOptions = commonTracks.length ? commonTracks : allTracks;
const selectedTrack = view(Inputs.select(trackOptions, {label: "Track"}));
```

```js
const track = trackOptions.includes(selectedTrack) ? selectedTrack : trackOptions[0];
const baselineTrackRows = baselineRows.filter(d => d.track === track);
const candidateTrackRows = candidateRows.filter(d => d.track === track);
const baselineSolvers = new Set(baselineTrackRows.map(d => d.solver));
const candidateSolvers = new Set(candidateTrackRows.map(d => d.solver));
const commonSolvers = [...baselineSolvers].filter(s => candidateSolvers.has(s)).sort();
const allSolvers = Array.from(new Set([...baselineSolvers, ...candidateSolvers])).sort();
const solverOptions = commonSolvers.length ? commonSolvers : allSolvers;
const selectedSolver = view(Inputs.select(solverOptions, {label: "Solver"}));
```

```js
const solver = solverOptions.includes(selectedSolver) ? selectedSolver : solverOptions[0];
```

## Performance Profile Overlay

```js
const baselineSeries = curves.sessions?.[baseline.slug]?.tracks?.[track]?.completion?.series ?? [];
const candidateSeries = curves.sessions?.[candidate.slug]?.tracks?.[track]?.completion?.series ?? [];
const overlayRows = [
  ...baselineSeries
    .filter(s => s.solver === solver)
    .flatMap(s => s.x.map((x, i) => ({session: baseline.name, seconds: x, solved: s.y[i]}))),
  ...candidateSeries
    .filter(s => s.solver === solver)
    .flatMap(s => s.x.map((x, i) => ({session: candidate.name, seconds: x, solved: s.y[i]})))
];
const profileTitle = `${track} · ${solver} · ${baseline.name} vs ${candidate.name}`;
display(Plot.plot({
  title: profileTitle,
  height: 420,
  x: {label: "Time (s)", grid: true},
  y: {label: "Instances solved", grid: true},
  color: {
    domain: [baseline.name, candidate.name],
    range: ["#2563eb", "#dc2626"],
    legend: true
  },
  marks: [
    Plot.lineY(overlayRows, {
      x: "seconds",
      y: "solved",
      stroke: "session",
      curve: "step-after",
      strokeWidth: 2.5
    }),
    Plot.ruleY([0])
  ]
}));
```

```js
const key = d => `${d.instance}`;
const baseRows = baselineTrackRows.filter(d => d.solver === solver);
const candRows = candidateTrackRows.filter(d => d.solver === solver);
const baseByInstance = new Map(baseRows.map(d => [key(d), d]));
const candByInstance = new Map(candRows.map(d => [key(d), d]));
const instances = Array.from(new Set([...baseByInstance.keys(), ...candByInstance.keys()])).sort();
const solved = d => d && (d.status === "SAT" || d.status === "UNSAT");
const comparison = instances.map(instance => {
  const before = baseByInstance.get(instance);
  const after = candByInstance.get(instance);
  const beforeSolved = solved(before);
  const afterSolved = solved(after);
  const beforeSeconds = before?.seconds ?? null;
  const afterSeconds = after?.seconds ?? null;
  const speedup = beforeSeconds && afterSeconds ? beforeSeconds / afterSeconds : null;
  let change = "same";
  if (!beforeSolved && afterSolved) change = "newly solved";
  else if (beforeSolved && !afterSolved) change = "lost solve";
  else if (beforeSolved && afterSolved && speedup !== null && speedup >= 1.1) change = "faster";
  else if (beforeSolved && afterSolved && speedup !== null && speedup <= 0.9) change = "slower";
  else if (before?.checker_valid === "true" && after?.checker_valid === "false") change = "checker regression";
  return {
    instance,
    before_status: before?.status ?? "",
    after_status: after?.status ?? "",
    before_seconds: beforeSeconds,
    after_seconds: afterSeconds,
    speedup,
    before_checker: before?.checker_valid ?? "",
    after_checker: after?.checker_valid ?? "",
    change
  };
});
```

```js
const totals = {
  "newly solved": comparison.filter(d => d.change === "newly solved").length,
  "lost solve": comparison.filter(d => d.change === "lost solve").length,
  faster: comparison.filter(d => d.change === "faster").length,
  slower: comparison.filter(d => d.change === "slower").length,
  "checker regression": comparison.filter(d => d.change === "checker regression").length
};
display(Plot.plot({
  marginLeft: 120,
  x: {grid: true},
  marks: [
    Plot.barX(Object.entries(totals).map(([change, count]) => ({change, count})), {x: "count", y: "change", fill: "change"}),
    Plot.ruleX([0])
  ]
}));
display(Inputs.table(comparison, {
  columns: ["change", "instance", "before_status", "after_status", "before_seconds", "after_seconds", "speedup", "before_checker", "after_checker"]
}));
```
