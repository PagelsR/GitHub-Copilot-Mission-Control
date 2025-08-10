# MCP, GitHub Security and PR Review

**Goal**  
Use the MCP GitHub server to let Copilot retrieve repo facts, list security alerts, and summarize PRs.

**Time** 10 to 15 minutes

## Prerequisites
- Node.js installed
- A GitHub repo you can query
- VS Code with Copilot

## Step 1, Start the GitHub MCP server
```bash
npx mcp-server-github
```

## Step 2, Ask targeted questions
Copy the prompt below into **Copilot Chat**. Paste one block at a time.
```
List the top 10 secret scanning alerts in this repo with file and line numbers.
```
Copy the prompt below into **Copilot Chat**. Paste one block at a time.
```
Summarize open PRs that have unresolved security alerts. Group by severity. Provide links.
```
Copy the prompt below into **Copilot Chat**. Paste one block at a time.
```
Show recent Dependabot alerts grouped by package. Suggest the top three upgrades to merge first and why.
```
