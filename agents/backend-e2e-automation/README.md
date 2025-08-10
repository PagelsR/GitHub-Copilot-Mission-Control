# Backend E2E Automation

## Mission
Use Copilot Agent Mode to add a small feature, update tests and docs, and open a PR.

## Why this matters
Agent Mode can coordinate work across files and tasks. This is ideal when a single request touches routes, models, tests, and docs.

## Copilot mode
Copilot Agent Mode, with Chat for quick checkpoints.

## Prerequisites
- A clean branch
```bash
git checkout -b demo/agent-backend-e2e
```
- dotnet test is passing
- API runs locally

## Steps
1) Define the mission in one shot  
Agent prompt  
> Mission, add an update endpoint for Plane status with validation and tests. Steps, create PATCH /planes/{id}/status, validate allowed transitions, add unit tests, update Swagger docs with examples, and update README with a short usage section. Open a PR when done.

2) Review and approve the plan  
Check the file list and diffs. If scope drifts, ask the Agent to restate constraints.

3) Run and verify  
```bash
dotnet build
dotnet test
dotnet watch run
# verify new endpoint via curl or Swagger
```

4) Ask for a PR with a structured description  
Agent follow up  
> Open a PR with a clear title, bullet summary, test evidence, and risks. Label it backend and status update.

5) Summarize the result with Chat  
> Summarize what changed and why this was safe. List any follow ups.
