# Codebase Explain, Frontend

**Goal**  
Map the React app, data flow to the backend, and prepare a plan for refactors and tests.

**Time** 5 to 8 minutes

## Prerequisites
- React app opened in VS Code
- Backend running locally

## Step 1, Explain the app
Copy the prompt below into **Copilot Chat**. Paste one block at a time.
```
Explain this React app. Identify entry point, routing, key components, shared UI, and API calls. 
List components and their props.
```

## Step 2, Trace data flow
Copy the prompt below into **Copilot Chat**. Paste one block at a time.
```
Show where we fetch plane data, how it is transformed, and where it is displayed. 
Identify duplication and missing loading or error states.
```

## Step 3, Pick three improvements
Copy the prompt below into **Copilot Chat**. Paste one block at a time.
```
Propose three improvements for Copilot Edits, for example extracting a PlaneRow component, adding error boundaries, or standardizing date formatting.
```

## Step 4, Demo script
Copy the prompt below into **Copilot Chat**. Paste one block at a time.
```
Draft a 2 minute demo script to explain the app, call out weak spots, and set up an Edits and an Agent Mode pass.
```
