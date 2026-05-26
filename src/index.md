# Benchmark Explorer

```js
import * as Plot from "npm:@observablehq/plot";
const sessions = await FileAttachment("data/sessions.csv").csv({typed: true});
const tracks = await FileAttachment("data/tracks.csv").csv({typed: true});
const summary = await FileAttachment("data/solver_summary.csv").csv({typed: true});
```

<div class="hero">
  <div>
    <h2>CPMpy benchmark sessions</h2>
    <p>Interactive static explorer generated from bench_gist metadata.</p>
  </div>
  <a class="button" href="https://ThomSerg.github.io/bench-gist-results/compare.html">Compare sessions</a>
</div>

```js
display(Inputs.table(sessions, {
  columns: ["name", "tracks", "cpmpy_commit", "created_at", "last_run_at", "solved", "total", "active"],
  header: {
    name: "Session",
    cpmpy_commit: "CPMpy commit",
    last_run_at: "Last run"
  }
}));
```

```js
const session = view(Inputs.select(sessions, {
  label: "Session",
  format: d => `${d.name} (${d.tracks || "no track"})`
}));
```

```js
const sessionTracks = tracks.filter(d => d.session_slug === session.slug);
const sessionSummary = summary.filter(d => d.session_slug === session.slug);
```

## Selected Session

```js
display(html`<p><a class="button" href="./session/${session.slug}.html">Open ${session.name}</a></p>`);
display(Inputs.table(sessionTracks, {columns: ["track", "solvers"]}));
display(Inputs.table(sessionSummary, {
  columns: ["track", "solver", "sat", "unsat", "timeout", "unknown", "total", "checker_valid", "checker_invalid"]
}));
```
