# Backend E2E Automation

**Goal**  
Use Copilot Agent Mode to add a status update endpoint with validation and tests, update docs, and open a PR.

**Time** 12 to 20 minutes

## Prerequisites
- Clean branch
```bash
git checkout -b demo/agent-backend-e2e
```
- Tests passing
```bash
dotnet test
```

## Step 1, Define the mission
Copy into Agent Mode.
```
Mission, add PATCH /planes/{id}/status to update a plane's status with validation of allowed transitions. 
Also add unit tests, update Swagger with examples, and add a short usage section in README. 
When complete, open a PR with a structured description and label it backend,status.
```

## Step 2, Approve the plan
If scope drifts, tell the Agent: **Keep scope small and focused**.

## Step 3, Run and verify
```bash
dotnet build
dotnet test
dotnet watch run
# verify via Swagger or curl
```

## Step 4, Open the PR
Copy into Agent Mode.
```
Open a PR with a clear title, bullet summary, test evidence, and risks. 
```
