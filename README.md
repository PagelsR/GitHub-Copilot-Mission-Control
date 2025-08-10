# Copilot Mission Control 🚀
*Your central command for mastering GitHub Copilot, Agents, Edits, Chat, MCP, and more.*

![Copilot Mission Control Logo](assets/mission-control-logo.png)

This repo contains organized demos grouped by Copilot mode and focus area. 
The current release includes backend-focused demos, with frontend and MCP content coming soon.

---

## 📂 Folder Structure

```
copilot-mission-control/
│
├── README.md
├── .gitignore
├── docs/
│   ├── overview.md
│   ├── tips-and-tricks.md
│   └── faq.md
│
├── assets/
│   └── mission-control-logo.png
│
├── chat/
│   └── codebase-explain-backend/
│       ├── README.md
│       └── prompts/
│           └── explain-codebase.md
│
├── edits/
│   └── backend-safe-refactors/
│       ├── README.md
│       └── prompts/
│           └── refactor-validations.md
│
├── integrations/
│   └── ci-cd/
│       └── backend-test-and-observability/
│           ├── README.md
│           └── snippets/
│               ├── sample-ci-notes.md
│               └── curl-health.txt
│
├── agents/
│   └── backend-e2e-automation/
│       ├── README.md
│       └── prompts/
│           └── status-update-mission.md
│
├── backend/
│   ├── WrightBrothersApi/
│   └── WrightBrothersApi.Tests/
│
└── frontend/
    └── README.md
```

---

## 🛰 About
Copilot Mission Control is designed to make it easy to demo and learn GitHub Copilot capabilities in a structured way. 
Each demo explains why it matters, which Copilot mode to use, and gives detailed steps for reproducibility.

---

## 📋 Current Demo Categories

### Chat
- **[Codebase Explain, Backend](chat/codebase-explain-backend/)**  
  Use Copilot Chat to explore the Wright Brothers API, understand its structure, and plan follow-up demos.

### Edits
- **[Backend, Safe Refactors](edits/backend-safe-refactors/)**  
  Apply small, safe changes with Copilot Edits while maintaining behavior and readability.

### Integrations
- **[Backend Tests and Observability](integrations/ci-cd/backend-test-and-observability/)**  
  Enhance backend health checks, structured logs, and test coverage with Copilot.

### Agents
- **[Backend E2E Automation](agents/backend-e2e-automation/)**  
  Use Copilot Agent Mode to deliver an end-to-end backend feature with coordinated code, tests, and documentation.

---

---

## 🛠 How to Use
1. Clone this repo  
2. Open in VS Code with GitHub Copilot Chat, Edits, and Agent Mode enabled  
3. Pick a demo and follow its README  
4. Use the prompts exactly as given, or adapt them to your own project

---

## 📡 Mission Status
- **Backend Demos**: ✅ Ready
- **Frontend Demos**: 🔄 In progress
- **MCP Demos**: 🔄 In progress

---

## Frontend Demos

### Chat
- **[Codebase Explain, Frontend](chat/codebase-explain-frontend/)**  
  Use Copilot Chat to map the React app, data flow, and improvement targets.

### Edits
- **[Frontend, Component Refactors](edits/frontend-component-refactors/)**  
  Extract smaller components, improve naming, and add type safety.

### Integrations
- **[Frontend API and State](integrations/frontend-api-and-state/)**  
  Wire the UI to the backend API, add loading and error states, and test it.

### Agents
- **[Frontend Flight Tracker with Leaflet.js](agents/frontend-flight-tracker/)**  
  Visualize planes on a live map with filtering and auto refresh.
- **[Frontend Hangar Bay Scheduler](agents/frontend-hangar-scheduler/)**  
  Reservation UI for hangar bays with daily/weekly views.
- **[Frontend Airport Density Heatmap](agents/frontend-airport-heatmap/)**  
  Leaflet heatmap of airport density with hub markers.

---

## MCP Demos
- **[GitHub Security and PR Review](mcp/github-security-review/)**  
- **[Playwright E2E with MCP](mcp/playwright-e2e/)**
