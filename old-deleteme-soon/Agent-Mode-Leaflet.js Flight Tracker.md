# 🕹️ GitHub Copilot Agent Mode: Build a Python Flight Tracker App

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

## Flight Tracker Demo — Leaflet.js Frontend App

```markdown
## Flight Data Leaflet Demo with Country Dropdown
Steps:
1. Create a new file named `flight_leaflet_demo.html`.

2. Include a full-screen Leaflet.js map centered initially on the United States (`[37.8, -96], zoom 5`).

3. In the `<head>`, add a `<style>` block to double the tooltip font size:
   html
   <style>
     .leaflet-tooltip {
       font-size: 2em;
     }
   </style>

4. Add a `<select>` dropdown with a few predefined countries (e.g. "United States", "Germany", "Australia", "United Kingdom", "Ireland").

5. Define a simple country lookup containing each country’s center lat/lon and zoom level:
  - United States → center of USA, zoom 5
  - United Kingdom → center of UK, zoom 7
  - Ireland → center of Ireland, zoom 7
  - Germany → center of Germany, zoom 6
  - Australia → center of Australia, zoom 5

6. When the user selects a country:

   - Fetch live flight data from:

     ```
     https://opensky-network.org/api/states/all
     ```
   - Filter aircraft to only those whose `origin_country` matches the selected country.
   - Zoom and center the map on the geographic area of the selected country.
   - Limit the number of aircraft to 50.

7. Plot aircraft as circular markers at `[latitude, longitude]`.

8. Color each marker:

   * Red if `on_ground === true`.
   * Blue if `on_ground === false`.

9. Make sure markers remain clearly visible at all zoom levels by using a fixed pixel `radius` (e.g. `radius: 8`).

10. Bind a tooltip to each marker showing:

   - Callsign
   - Velocity (m/s)
   - Altitude (m)
   - Heading (degrees)

11. Gracefully skip any aircraft that lack lat/lon data.

12. 🛑 Stop after completing this so I can review the output before continuing.

Agent Mode Instructions:

- Run `python -m http.server`
- Print the URL so I can click to view the demo.

```

## MCP Talking Points

### Steps to Demo:

1. **Load your flight demo HTML.**

2. **Explain the country dropdown and MCP:**

   * Point at the dropdown.
   * Say:

     > “When you select a country, this is triggering an MCP-style fetch — pulling live flight data at that moment.”

3. **Show the code snippet where data is fetched:**

   * Highlight the `fetch()` call.
   * Explain:

     > “And here in our flight tracker app, this `fetch()` call is our MCP moment — Copilot is reaching out to get live flight data just when we need it. It’s pulling real-time context directly into our app!”

     > “With MCP, Copilot only grabs flight data as you need it — dynamic and current.”

4. ✅ **Key Points:**

   * Emphasize the live nature of data.
   * Highlight that this would also scale to other data sources — all thanks to the MCP design.


---

## ✨ Bonus Round 1 — Flight Demo Enhancements

```markdown
Please **update the existing `flight_leaflet_demo.html` file** with the following features:
1. **Show Plane Count Stats:**  
   - Add a small fixed overlay div in the top-right corner that displays the total number of planes currently displayed.
2. **Highlight Selected Plane:**  
   - When a plane marker is clicked:
     - Change its style (e.g. a larger circle or different color) to make it stand out.
     - Store its reference so clicking a new plane will reset the previously highlighted one.
3. **Clickable Plane Detail Panel:**  
   - Add a fixed panel at the bottom or side of the page.
   - When a plane is clicked, show its full details inside this panel:
     - Callsign, origin country, altitude, velocity, heading.
   - Make sure the panel updates as different planes are selected.
4. **Add Auto-Refresh Toggle:**  
   - Include a checkbox or button labeled “Auto-Refresh every 30s.”
   - When enabled, re-fetch the flight data every 30 seconds and update the markers, plane count, and panel accordingly.
   - Preserve the currently selected plane if it still exists after refresh.

Agent Mode Instructions:
- Modify the existing `flight_leaflet_demo.html` file.
- Do not start over — just implement these enhancements on top of what is already there.
- 🛑 Stop after completing so I can review the output.
```

## ✨ Bonus Round 2 — Flight Demo Enhancements

```markdown
Please **update the existing `flight_leaflet_demo.html` file** with the following features:
1. **Add Auto-Refresh Toggle:**  
   - Include a checkbox or button labeled “Auto-Refresh every 30s.”
   - When enabled, re-fetch the flight data every 30 seconds and update the markers, plane count, and panel accordingly.
   - Preserve the currently selected plane if it still exists after refresh.

Agent Mode Instructions:
- Modify the existing `flight_leaflet_demo.html` file.
- Do not start over — just implement these enhancements on top of what is already there.
- 🛑 Stop after completing so I can review the output.
```


---

## Summary

✅ Clearly formatted like the Python demo prompt.

✅ Includes an easy “Bonus Round” section that adds flair and interactivity to your demo.

✅ Designed for Agent Mode to auto-generate code you can preview quickly.

---
