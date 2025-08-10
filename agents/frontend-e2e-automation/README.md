# Frontend E2E Automation

**Goal**  
Use Copilot Agent Mode to add a plane status badge and a status filter with tests and docs.

**Time** 12 to 20 minutes

## Prerequisites
```bash
git checkout -b demo/agent-frontend-e2e
npm install
npm run dev
```

## Step 1, Define the mission
Copy into Agent Mode.
```
Mission, add a status badge to <PlaneRow /> and a filter control in PlaneList for status values. 
Steps, implement the badge with consistent colors, add a filter that narrows the list without refetching, 
write a React Testing Library test for the filter, and update the README with a short usage section. When complete, open a PR.
```

## Step 2, Review the plan and changes
If scope drifts, say **Keep scope narrow**.

## Step 3, Run and verify
```bash
npm test
npm run dev
```

## Step 4, PR
Copy into Agent Mode.
```
Open a PR with a clear title, bullet summary, and test evidence. Keep the diff focused.
```
