# Compare Sessions

```js
const sessions = await FileAttachment("data/sessions.csv").csv({typed: true});
const results = await FileAttachment("data/results.csv").csv({typed: true});
```

```js
const baseline = view(Inputs.select(sessions, {label: "Baseline", format: d => d.name}));
const candidate = view(Inputs.select(sessions, {label: "Candidate", value: sessions[0], format: d => d.name}));
const sharedTracks = Array.from(new Set(results
  .filter(d => d.session_slug === baseline.slug || d.session_slug === candidate.slug)
  .map(d => d.track))).sort();
const track = view(Inputs.select(sharedTracks, {label: "Track"}));
const sharedSolvers = Array.from(new Set(results
  .filter(d => (d.session_slug === baseline.slug || d.session_slug === candidate.slug) && d.track === track)
  .map(d => d.solver))).sort();
const solver = view(Inputs.select(sharedSolvers, {label: "Solver"}));
```

```js
const key = d => `${d.instance}`;
const baseRows = results.filter(d => d.session_slug === baseline.slug && d.track === track && d.solver === solver);
const candRows = results.filter(d => d.session_slug === candidate.slug && d.track === track && d.solver === solver);
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
