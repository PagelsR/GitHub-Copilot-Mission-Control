# 🕹️ GitHub Copilot Agent Mode: Build a Python Pinball Finder App

**Estimated Duration: 10 minutes**

A step-by-step demo for using GitHub Copilot Agent Mode to build a Pinball Finder app in Python and HTML. This project guides Copilot Agent Mode through atomic tasks, letting you build a complete airplane tracking app by pasting one prompt at a time. No live server or cloud deployment required — it all runs locally!

---

## Getting Started

✅ **Create a new empty folder** — e.g. `pinball-demo`, then **open it in VS Code**.  
✅ **Ensure Python is installed** — if not, download and install it from https://www.python.org/downloads/.

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

## Pinball Demo — Python Backend App

```markdown
## Python Backend App
Steps:
1. Create a new Python file named `pinball_zip_lookup.py`.
2. Prompt the user to enter a US zip code.
3. Fetch machines from:

https://pinballmap.com/api/v1/machines.json

with the query parameter:

by\_location\_zip={zip\_code}

4. Parse the JSON and retrieve the list of machines.
5. Print **only the top 5 machines**:
- Show each machine's `name` and its `location_name`.
- If fewer than 5 machines are available, just list what’s returned.
6. Print a friendly message if **no machines** are found.
7. Include error handling for:
- Invalid zip code
- Network errors
8. Generate a `requirements.txt` file with any dependencies (`requests`).
9. Run the file after creating it so I can see the output.
10. 🛑 Stop after completing this so I can review the output before continuing.

**Agent Mode Instructions**:
- Run `pip install -r requirements.txt`
- Run the Python file (`python pinball_zip_lookup.py`)
```

## MCP Talking Points

### Steps to Demo:

1. **Run the Pinball Backend demo as before** — let the zip code lookup produce machines.

2. **Explain MCP:**

   * Tell your audience:

     > “Here, Copilot Agent is using the Model Context Protocol — or MCP — to fetch live data on-demand instead of relying on cached or static data.”

3. **Show the code snippet where data is fetched:**

   * Highlight the `requests.get(...)` call.
   * Explain:

     > “This is where Copilot uses the MCP to reach out and pull data at request-time.”

4. **Run the code for multiple zip codes:**

   * Explain that Agent Mode is pulling live data each time — “fetching context just when it’s needed.”

5. **Key Points:**

   * MCP enables real-time context for the model.
   * No stale data.
   * Perfect for demoing up-to-date API calls!

---

### Updated Bonus Round — Pinball Backend + HTML/CSS Table + CSV Export

```markdown
Please **update the existing `pinball_zip_lookup.py` file** to add these features:
1. Fetch machines for the zip code(s) as before and keep the top 10 machines.
2. Save those top 10 machines into:
   - `pinball_machines.html`
   - `pinball_styles.css`
3. In `pinball_machines.html`:
   - Link to the `pinball_styles.css` file.
   - Include a polished, scrollable table with columns: `Name`, `Active`, `Year`, `Manufacturer`.
   - Populate the table with the top 10 machines.
   - Include a prominent **“Export to CSV”** button at the top.
   - Implement client-side JavaScript so clicking the button downloads `pinball_machines_top10.csv`.
4. In `pinball_styles.css`:
   - Style the table with alternating row colors, a subtle border, padding, and fixed header.
   - Style the “Export to CSV” button so it looks polished and stands out.
   - Make the table scrollable vertically if too many machines (e.g. a fixed height with `overflow-y: auto`).
5. Print a friendly message after creating the HTML file, CSS file, and generating the CSV file.

Agent Mode Instructions:
- Modify the existing Python file — do not create a new one.
- Run the Python file (`python pinball_zip_lookup.py`)
- Print the URL for `pinball_machines.html` so I can click to view the demo.
- 🛑 Stop after completing this so I can review the output.
```

---

## Summary

✅ Clearly formatted like the Python demo prompt.

✅ Includes an easy “Bonus Round” section that adds flair and interactivity to your demo.

✅ Designed for Agent Mode to auto-generate code you can preview quickly.

---
