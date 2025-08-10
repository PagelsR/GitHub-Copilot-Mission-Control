## Automating with `mcp-playwright` (MCP Playwright) Testing

## Getting Started

✅ **Create a new empty folder** — e.g. `GHAS-Demo`, then **open it in VS Code**.

  ```bash
  mkdir GHAS-Demo && cd GHAS-Demo
  ```

✅ **Enable Agent Mode**:
   - Click the **Extensions** icon in the VS Code sidebar.
   - Search for **Python** (by Microsoft).
   - Click **Install**.

✅ **Open Agent Mode Chat**:
- Open the **Copilot Ask** sidebar.
- Make sure **Agent Mode** is toggled on.
- You’re now ready to start pasting the prompts below.

---

✅ You're all set to run this demo with GitHub Copilot Agent Mode. Paste each block below one at a time and enjoy the ride!

---

### Steps to Demo `@modelcontextprotocol/server-github`:
1. Open Visual Studio Code with `GHAS-Demo` folder.

2. Start the MCP GitHub Server:
   ```bash
   npx mcp-server-github
   ```



## Example MCP Prompts for Reviewing PRs and Security Alerts

### 1. Show Open Security Alerts by Type

```
Show me the top 5 open security alerts in https://github.com/Technical-Bootcamp/pagelsr-ghas-bootcamp, grouped by alert type (e.g., secret scanning, code scanning, Dependabot).
```

### 2. List All Secret Scanning Alerts

```
List me the top 10 secret scanning alerts in https://github.com/Technical-Bootcamp/pagelsr-ghas-bootcamp, ordered by Secret type including the file and line number where each secret was found.
```

### 3. Review Pull Requests with Open Security Alerts

```
Show all open pull requests in https://github.com/Technical-Bootcamp/pagelsr-ghas-bootcamp that have unresolved security alerts. Include the PR title, author, and alert type.
```

### 4. Summary of Code Scanning Alerts in PRs

```
Summarize all code scanning alerts found in open pull requests for https://github.com/Technical-Bootcamp/pagelsr-ghas-bootcamp. Group by alert severity and provide direct links to the affected PRs.
```

### 5. List PRs by Most Recent Security Alert Activity

```
List pull requests in https://github.com/Technical-Bootcamp/pagelsr-ghas-bootcamp, sorted by the most recent security alert activity. For each PR, show the type of alert, date detected, and current status.
```


---

## 🧭 **Demo Flow — What to Say and Do**

✅ **First**, run this prompt in Agent Mode and let Copilot produce the full file — your audience will see it build the entire Playwright test suite!

✅ **Next**, highlight:

> 🎙️ *“Here we asked Copilot to implement a detailed Playwright test suite with real selectors and validation logic — exactly like a human would.”*

✅ **Then**, run the tests (`npx playwright test`) so everyone can see green checks.

✅ **Finally**, introduce the `mcp-playwright` angle:

> 🎙️ *“With this baseline, we can now leverage MCP Playwright to generate variations, add error handling, or test additional edge cases — all driven by Agent Mode.”*

---

