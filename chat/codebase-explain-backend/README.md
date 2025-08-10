# Codebase Explain, Backend

## Mission
Use Copilot Chat to understand the API quickly, identify endpoints and models, and plan the next steps.

## Why this matters
You move faster when you start with a clear picture. Chat gives you a concise map and a short plan you can follow.

## Copilot mode
Copilot Chat in the VS Code side panel.

## Prerequisites
- .NET 8 SDK
- WrightBrothersApi opened in VS Code
- Copilot Chat enabled

## Steps
1) Create a map of the backend  
Prompt in Chat  
> Explain this codebase at a high level. Identify projects, key folders, controllers, models, and DTOs. List the public endpoints with HTTP verbs, route templates, and short summaries.

2) Find hotspots worth demoing  
Prompt in Chat  
> Based on the structure, which parts are good candidates for Copilot Edits, for example repeated logic, long methods, and missing validation. Return a checklist.

3) Generate a test plan outline  
Prompt in Chat  
> Propose a test plan for the API. Cover unit tests for services, minimal controller tests, and a smoke test with dotnet test. Include command examples.

4) Produce a short demo script  
Prompt in Chat  
> Draft a three minute demo script with intro, steps, and expected outputs. Optimize for using Chat to understand, Edits to refactor, and Agent Mode to finish the task.

5) Optional, quick endpoint inventory  
Commands  
```bash
cd backend/WrightBrothersApi
dotnet build
dotnet watch run
# Open Swagger UI and confirm routes
```
