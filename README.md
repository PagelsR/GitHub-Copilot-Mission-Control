# GitHub Copilot Mission Control

A collection of GitHub Copilot Agent Mode demos showcasing real-world automation across APIs, UIs, and data workflows.

🚀 Explore hands-on GitHub Copilot Agent Mode demos that automate tasks, control apps, and streamline development workflows.

---

## 🗂️ Agent Mode Demo from Scratch

| Demo | Description | Link |
|------|-------------|------|
| **Air Traffic Map** | Uses OpenSky Network API and Leaflet.js to visualize live airplane positions on a map. | [Agent-Mode-AirTrafficMap.md](Agent-Mode-AirTrafficMap.md) |
| **Earthquake Heatmap** | Pulls real-time earthquake data from the USGS API and displays them on a Leaflet.js heatmap with magnitude-based color coding. | [Agent-Mode-USGS Earthquakes.md](Agent-Mode-USGS%20Earthquakes.md) |
| **ISS Tracker** | Uses the Open Notify API to show the current location of the International Space Station on a map, updating every 5 seconds. | [Agent-Mode-ISS Tracker.md](Agent-Mode-ISS%20Tracker.md) |
| **Task Tracker** | Builds a task tracker app with local persistence using HTML, CSS, and JavaScript. | [Agent-Mode-TaskTracker.md](Agent-Mode-TaskTracker.md) |
| **Pickleball Court Tracker** | Builds an interactive reservation system for pickleball courts. | [Agent-Mode-Pickleball Court Tracker.md](Agent-Mode-PickleballCourtTracker.md) |

---

## 🗂️ Agent Mode Demo using Wright Brothers App

| Demo | Description | Link |
|------|-------------|------|
| **TBD** | Uses the Wright Brothers application to enhance the REST API and Frontend app. | [Agent-Mode-WrightBrothers.md](Agent-Mode-WrightBrothers.md) |



Exactly — great catch! 🎯 Let’s add a clear setup step so the demo doesn’t surprise you mid-flight. ✈️ Here’s the updated demo flow with the **Playwright installation** step added before running the tests:

---

## 🧭 Demo Flow — Playwright Test with Agent Mode

✅ **Before running the tests**, make sure Playwright is installed:

```bash
npm init -y
npm install --save-dev @playwright/test
npx playwright install
```

✅ Then run the tests:

```bash
npx playwright test
```

---

## 🎁 Updated Demo Flow Instructions

Here’s a clean version for your talk track:

1. 🔥 Generate the tests with Agent Mode.
2. 📂 Check the `brand_catalog.spec.ts` file.
3. ⚙️ Run the setup commands:

   ```bash
   npm init -y
   npm install --save-dev @playwright/test
   npx playwright install
   ```
4. 🏃 Run:

   ```bash
   npx playwright test
   ```
5. ✅ Show green checkmarks and talk about **MCP Playwright automation**!

---

🎯 Would you also like me to prepare a **one-page cheat sheet** with all these commands and a brief demo script so you can narrate each step smoothly? Let me know — I’d love to help you make this demo pitch-perfect! 🎸
