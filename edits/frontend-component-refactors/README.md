# Frontend, Component Refactors

**Goal**  
Extract smaller components, clarify prop names, and add type safety without changing behavior.

**Time** 8 to 12 minutes

## Prerequisites
```bash
git checkout -b demo/edits-frontend-refactors
npm install
npm run dev
```

## Step 1, Extract PlaneRow
Select the row markup.
Copy the prompt below into **Copilot Chat**. Paste one block at a time.
```
Extract a <PlaneRow /> component with typed props. Keep behavior identical. Update imports and usages.
```

## Step 2, Standardize date formatting
Copy the prompt below into **Copilot Chat**. Paste one block at a time.
```
Add a small date util that formats departure and arrival as local time strings. Replace inline formatting with the util. 
No behavior change besides formatting consistency.
```

## Step 3, Improve names and types
Copy the prompt below into **Copilot Chat**. Paste one block at a time.
```
Rename ambiguous props like data or item to plane or planes. Add explicit types. Update all call sites.
```

## Step 4, Summarize and test
Copy the prompt below into **Copilot Chat**. Paste one block at a time.
```
Summarize the diff and call out any risky areas.
```
```bash
npm test
npm run dev
```
