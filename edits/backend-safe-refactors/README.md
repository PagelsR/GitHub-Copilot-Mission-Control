# Backend, Safe Refactors

**Goal**  
Apply small refactors with Copilot Edits, keep behavior identical, and pass tests.

**Time** 8 to 12 minutes  
**Best for** Readability, duplication, consistent docs

## Prerequisites
- Branch created for refactor
```bash
git checkout -b demo/edits-refactors
```
- Tests compile
```bash
dotnet build && dotnet test
```

## Step 1, Extract validation
Open the file that contains Plane creation logic. Select the method body.
Copy the prompt below into **Copilot Chat**. Paste one block at a time.
```
Extract validation logic into a helper method named ValidatePlaneInput with clear error messages. 
Keep behavior identical. Update all call sites. Do not change public signatures.
```

## Step 2, Summarize the diff
Copy the prompt below into **Copilot Chat**. Paste one block at a time.
```
Summarize the diff. Call out any behavior changes or risk areas.
```

## Step 3, Improve names and docs
Select the changed files and run another Edit.
Copy the prompt below into **Copilot Chat**. Paste one block at a time.
```
Improve naming for clarity and add XML doc comments for public methods. 
Do not change behavior. Keep the signature of existing methods.
```

## Step 4, Test
```bash
dotnet test
dotnet watch run
```

## Step 5, Commit
```bash
git add -A
git commit -m "Refactor validation and docs, no behavior change"
```


### Verify
- Follow the on screen instructions
- If Copilot changes more than expected, say: **Keep scope small, do not change behavior** and retry
