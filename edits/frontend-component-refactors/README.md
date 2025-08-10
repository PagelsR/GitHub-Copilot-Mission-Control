# Frontend, Component Refactors

## Mission
Use Copilot Edits to extract smaller components, improve naming, and add type safety without changing behavior.

## Why this matters
Small, predictable refactors make the UI easier to test and extend.

## Copilot mode
Copilot Edits for code changes, Chat to summarize diffs.

## Prerequisites
- React app builds and runs
- A feature branch
```bash
git checkout -b demo/edits-frontend-refactors
```

## Steps
1) Extract a row item component
Open the planes list file, select the row markup, then ask in Edits
> Extract a <PlaneRow /> component with typed props. Keep behavior identical and update imports and usages.

2) Standardize date formatting
Edits prompt
> Add a small date util that formats departure and arrival times as local time strings. Replace inline formatting calls with this util. No behavior change besides formatting consistency.

3) Improve names and props
Edits prompt
> Rename ambiguous props like data or item to plane or planes. Add explicit types. Update all call sites.

4) Summarize diffs
Chat prompt
> Summarize the refactor changes and point out any risky areas.

5) Run and verify
```bash
npm run dev   # or your package script
```

6) Commit
```bash
git add -A
git commit -m "Extract PlaneRow, standardize date util, clarify prop names"
```
