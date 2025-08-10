# GitHub Copilot Agent Mode: Earthquake Heatmap with USGS API

⏱️ **Estimated Duration: 20–30 minutes**

A fully local, step-by-step GitHub Copilot Agent Mode demo that builds a real-time heatmap of global earthquakes using the [USGS Earthquake API](https://earthquake.usgs.gov/earthquakes/feed/v1.0/geojson.php) and Leaflet.js.

No live server or cloud deployment required — it all runs locally!

---

## Getting Started

Before using GitHub Copilot Agent Mode:

### Step 1: Create a Project Folder
```plaintext
mkdir earthquake-heatmap-demo && cd earthquake-heatmap-demo
```

### Step 2: Open the Folder in VS Code
```plaintext
code .
```

### Step 3: Enable Agent Mode
- Open the **Copilot Chat** sidebar.
- Toggle **Agent Mode** ON.
- You’re now ready to start pasting the prompts below.

✅ You're ready to build this demo with Copilot Agent Mode. Paste each step one at a time and let Copilot do the heavy lifting!

## 🧩 Step 1: Create Basic Map and Fetch Earthquake Data
```plaintext
Create an HTML file named Earthquake-Heatmap.html that:

- Loads Leaflet.js and Leaflet.heat plugin.
- Renders a full-screen interactive map.
- Fetches data from:
  https://earthquake.usgs.gov/earthquakes/feed/v1.0/summary/all_day.geojson
- Extracts latitude, longitude, and magnitude from each feature.
- Uses Leaflet.heat to display a heatmap where each point:
  - Is placed at the earthquake’s coordinates.
  - Uses magnitude as the intensity.
- Do NOT include integrity or crossorigin attributes in the Leaflet or plugin links.

🛑 Stop after this so I can verify map and heatpoints appear correctly.
```

- Click **Keep** to retain the generated code.

- Open the HTML file in your browser and confirm heatmap loads with global earthquake data.

Nice — that’s a solid start! Let’s add more context with tooltips and color overlays next.

## 🧩 Step 2: Add Marker Tooltips for High Magnitude Quakes
```plaintext
Update Earthquake-Heatmap.html so that:

- For any earthquake with magnitude ≥ 5.0:
  - Place a Leaflet circle marker at its location.
  - Attach a tooltip showing:
    - Magnitude
    - Location (place string)
    - Time (formatted as local datetime)
- Keep the heatmap intact as background.
- Circle marker radius should be proportional to magnitude.
```

- Click **Keep** when done.  
- Refresh browser and hover over high-magnitude areas to test.

Great! Now let’s give it a visual upgrade using basemaps and controls.

## 🧩 Step 3: Switch to CartoDB Light Map and Add Legend
```plaintext
Update the Earthquake-Heatmap.html file to:

- Replace the default Leaflet tiles with CartoDB Positron tiles:
  `https://{s}.basemaps.cartocdn.com/light_all/{z}/{x}/{y}{r}.png`
- Add proper attribution for CartoDB and USGS.
- Add a fixed-position legend in the bottom right corner that:
  - Describes the heatmap intensity range.
  - Explains that circle markers indicate strong quakes (≥5.0).
```

- Click **Keep**, refresh browser, and confirm map looks cleaner and includes a helpful legend.

Looking good! One last touch to wrap this up.

---

## 🧩 Step 4: Add Refresh Button to Update Data
```plaintext
Add a "🔄 Refresh Earthquake Data" button to the top-left corner of the page that:

- Refetches the USGS GeoJSON data.
- Clears the heatmap layer and circle markers.
- Rebuilds them with the latest earthquake data.

Style the button with a little padding and a light background.
```

- Click **Keep** once this is implemented.

Now refresh data any time — no page reload needed!

## ✅ Demo Complete!

You’ve built a working real-time earthquake heatmap — from scratch — using just GitHub Copilot Agent Mode.

> [!TIP]
> This demo runs entirely local. The USGS API is public, stable, and doesn’t require an API key — making it perfect for fast, no-hassle Agent Mode experiments.

---

## 🌋 Bonus Challenge (Optional)

```plaintext
Challenge Copilot to:
- Filter to show only earthquakes within the U.S.
- Style quakes above magnitude 6 with red outlines.
- Add popup links to the official USGS event pages.
```
