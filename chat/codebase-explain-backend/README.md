# Codebase Explain, Backend

**Goal**  
Get a clear overview of the Wright Brothers API, routes, models, and test surface, then produce a short demo plan.

**Time** 5 to 8 minutes  
**Best for** First run in any repo

## Prerequisites
- .NET 8 SDK installed
- VS Code with GitHub Copilot Chat
- Repo path: `backend/WrightBrothersApi` and `backend/WrightBrothersApi.Tests`

## Step 1, Open the repo
```bash
cd backend/WrightBrothersApi
code .
```

## Step 2, Explain the codebase
Copy the prompt below into **Copilot Chat**. Paste one block at a time.
```
Explain this codebase at a high level. Identify projects, key folders, controllers, models, and DTOs. 
List public endpoints with HTTP verbs and route templates. Return a concise table.
```

## Step 3, Find safe refactor targets
Copy the prompt below into **Copilot Chat**. Paste one block at a time.
```
From this codebase, list three safe refactor candidates for Copilot Edits. 
Prefer repeated validation, long methods, or duplicate mapping logic. 
Return a checklist with file names and function names.
```

## Step 4, Propose a test plan
Copy the prompt below into **Copilot Chat**. Paste one block at a time.
```
Propose a test plan for this API using xUnit. Include unit tests for services, a minimal controller test, 
and a smoke test that builds and runs the API with dotnet. Include exact shell commands.
```

## Step 5, Draft a 3 minute demo script
Copy the prompt below into **Copilot Chat**. Paste one block at a time.
```
Draft a 3 minute demo script. Sections: Intro, Codebase tour, Refactor target, Test plan, Close. 
Keep it concise. Use bullet points.
```


### Verify
- Follow the on screen instructions
- If Copilot changes more than expected, say: **Keep scope small, do not change behavior** and retry


## Optional, quick route inventory
```bash
dotnet build
dotnet watch run
# Open Swagger UI and compare with Copilot's inventory
```
