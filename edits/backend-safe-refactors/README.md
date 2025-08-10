# Backend, Safe Refactors

## Mission
Apply small, safe refactors with Copilot Edits to improve clarity without changing behavior.

## Why this matters
Edits are ideal when you want precise multi file changes with guardrails. You keep control and review each proposal.

## Copilot mode
Copilot Edits for the changes, Chat to summarize diffs.

## Prerequisites
- WrightBrothersApi open in VS Code
- Tests compile
- A feature branch
```bash
git checkout -b demo/edits-refactors
```

## Steps
1) Identify a target  
Pick one item from the checklist created in the Chat demo.

2) Create a focused Edit request  
Select the function or file, open Copilot Edits, then ask  
> Extract validation for Plane creation into a helper method with clear error messages. Keep behavior identical. Update all call sites.

3) Review the proposed changes  
Use Chat  
> Summarize the diff and call out any behavior changes or risk areas.

4) Run tests and smoke the API  
```bash
dotnet test
dotnet watch run
```

5) Do a second pass for naming and docs  
Open Edits again  
> Improve naming for clarity and add XML doc comments for public methods. Do not change behavior.

6) Commit  
```bash
git add -A
git commit -m "Refactor validations and docs, no behavior change"
```
