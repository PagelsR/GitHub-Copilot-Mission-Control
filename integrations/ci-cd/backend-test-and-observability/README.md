# Backend Tests and Observability

**Goal**  
Add a health endpoint, structured logs, and two unit tests. Prepare notes for CI.

**Time** 10 to 15 minutes

## Prerequisites
- API builds locally
```bash
cd backend/WrightBrothersApi && dotnet build
```

## Step 1, Health endpoint
Copy the prompt below into **Copilot Chat**. Paste one block at a time.
```
If not present, add GET /health that returns 200 OK and JSON: { "app": "<name>", "version": "<1.0.0>" }. 
Read version from assembly info. Keep the controller small.
```

## Step 2, Structured logging
Copy the prompt below into **Copilot Chat**. Paste one block at a time.
```
Add structured logging in startup and PlaneController. Log route, status code, and execution time. 
Keep logs concise and avoid PII.
```

## Step 3, Tests
Copy the prompt below into **Copilot Chat**. Paste one block at a time.
```
In WrightBrothersApi.Tests, add two xUnit tests for PlaneService. 
One happy path, one failure case. Use Arrange, Act, Assert. Keep them fast and deterministic.
```

## Step 4, Run locally
```bash
dotnet test
dotnet watch run
curl -i http://localhost:5000/health
```

## Step 5, CI notes
Copy the prompt below into **Copilot Chat**. Paste one block at a time.
```
Write a short CI section that runs dotnet build and dotnet test with trx output and publishes test results as an artifact.
```


### Verify
- Follow the on screen instructions
- If Copilot changes more than expected, say: **Keep scope small, do not change behavior** and retry
