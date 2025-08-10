# MCP, Playwright E2E Testing with Copilot Agent Mode

**Goal**  
Use MCP Playwright tools with Copilot Agent Mode to generate and run browser tests against a local app, iterating until they pass.

**Time** 15 to 25 minutes

## Prerequisites
- Node.js 18+
- VS Code with GitHub Copilot and Agent Mode
- A local web app to test, or use a simple demo app

## Step 0, Initialize Playwright
Run in an empty folder you want to use for tests.
```bash
npm init playwright@latest --yes -- --quiet --browser=chromium --browser=firefox --gha
npm install
npx playwright install
```

## Step 1, Start the MCP Playwright tooling
If you have an MCP Playwright server, start it now. Otherwise ask Copilot for the recommended setup.
Copy the prompt below into **Copilot Chat**. Paste one block at a time.
```
Explain how to use MCP with Playwright in VS Code. 
Provide the simplest setup so Copilot Agent Mode can create and run tests locally.
```

## Step 2, Create a focused spec
Copy into Agent Mode.
```
Create a Playwright test named example.spec.ts that:
- Navigates to http://localhost:3000
- Verifies the page title contains "Wright"
- Clicks a menu link labeled "Planes"
- Asserts that a list of planes renders at least two items
Keep selectors readable and resilient.
```

## Step 3, Run tests and fix failures
```bash
npx playwright test
npx playwright show-report
```

If a step fails, ask Copilot to fix the spec:
Copy the prompt below into **Copilot Chat**. Paste one block at a time.
```
The test failed on step X with error Y. Propose a minimal fix and update selectors. 
Keep CSS selectors or text locators simple and stable.
```

## Step 4, Add a second spec with filtering
Copy into Agent Mode.
```
Create a Playwright test named filter.spec.ts that:
- Opens http://localhost:3000/planes
- Types "United" into a Status filter or Country filter input
- Asserts that the visible list is narrowed
- Takes a screenshot named filter.png
```

## Step 5, Parallel run and artifacts
```bash
npx playwright test --reporter=html,line --workers=2
npx playwright show-report
```

## Step 6, CI hint
Copy the prompt below into **Copilot Chat**. Paste one block at a time.
```
Add a short CI snippet for GitHub Actions that installs Node, caches npm, runs Playwright tests, and uploads the Playwright report as an artifact.
```
