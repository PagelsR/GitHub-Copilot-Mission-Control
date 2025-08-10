# Codebase Explain, Frontend

## Mission
Use Copilot Chat to understand the React app structure, the data flow to the API, and where to improve.

## Why this matters
You make better changes when you know component boundaries, props, state, and fetch points.

## Copilot mode
Copilot Chat in the VS Code side panel.

## Prerequisites
- React app opened in VS Code
- The backend API running locally
- Copilot Chat enabled

## Steps
1) Map the UI
Prompt in Chat
> Explain this React codebase. Identify the app entry, routing, key components, shared UI, and API calls. List each component and its props.

2) Trace the data flow
Prompt in Chat
> Show where we fetch plane data, how it is transformed, and where it is displayed. Identify duplication and missing loading or error states.

3) Surface opportunities
Prompt in Chat
> Propose three improvements we can demonstrate with Copilot Edits, for example extracting a PlaneList item component, adding error boundaries, or standardizing date formatting.

4) Produce a short demo script
Prompt in Chat
> Draft a two minute demo script to explain the app, call out weak spots, and set up an Edits pass and an Agent Mode pass.
