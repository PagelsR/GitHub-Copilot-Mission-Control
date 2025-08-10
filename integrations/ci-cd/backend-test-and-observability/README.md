# Backend Tests and Observability

## Mission
Tighten local testing, logs, and health checks. Show patterns that translate well into CI.

## Why this matters
Strong demos show green tests, clear logs, and simple checks that signal health.

## Copilot modes
Chat for scaffolding and ideas, Edits for instrumentation.

## Prerequisites
- WrightBrothersApi and WrightBrothersApi.Tests build
- dotnet test passes on main

## Steps
1) Add or confirm a health endpoint  
Chat prompt  
> If not present, add GET /health that returns 200 OK with app name and version from assembly info.

2) Add structured logging  
Edits prompt  
> Add structured logging in startup and PlaneController. Log route, status code, and execution time. Keep logs concise.

3) Expand tests with one happy path and one edge case  
Chat prompt  
> Propose two xUnit tests for PlaneService, one happy path and one failure. Generate the test methods with clear Arrange, Act, Assert.

4) Run locally and show the flow  
```bash
dotnet test
dotnet watch run
# In a new terminal
curl -i http://localhost:5000/health
```

5) CI ready notes  
Chat prompt  
> Write a short section for a CI job that runs dotnet build and dotnet test with trx output, and publishes the test results artifact.
