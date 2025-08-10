# Frontend E2E Automation

## Mission
Use Copilot Agent Mode to add a small feature end to end, for example a plane status badge with filter, tests, and docs.

## Why this matters
Agent Mode coordinates code, tests, and docs in one go, which is ideal for feature slices.

## Copilot mode
Copilot Agent Mode, Chat for small checkpoints.

## Prerequisites
- A clean branch
```bash
git checkout -b demo/agent-frontend-e2e
```
- Backend and frontend run locally

## Steps
1) Define the mission
Agent prompt
> Mission, add a status badge to PlaneRow and a filter control to PlaneList for status values. Steps, implement the badge with consistent colors, add a filter that narrows the visible list without refetching, write a React Testing Library test for the filter, and update the README with a short usage section. When complete, open a PR.

2) Review and accept changes
If scope drifts, ask the Agent to restate constraints and keep the diff focused.

3) Run and verify
```bash
npm test
npm run dev
```

4) Open the PR
Agent follow up
> Open a PR with a clear title, a bullet summary of changes, and test evidence.

5) Summarize
Chat prompt
> Summarize what changed, why it is safe, and list one follow up task.
