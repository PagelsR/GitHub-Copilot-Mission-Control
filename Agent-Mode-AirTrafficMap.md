
# ✈️ GitHub Copilot Agent Mode: Leaflet.js Map for Airplane Tracking

This project guides GitHub Copilot Agent Mode to build Leaflet.js-based airplane tracking maps in stages. Paste each step into Copilot Chat, review the output, then proceed to the next.

---

## Getting Started

Before using GitHub Copilot Agent Mode:

### Step 1: Create a Project Folder
```plaintext
mkdir leaflet-airplanes-demo && cd leaflet-airplanes-demo
```

### Step 2: Open the Folder in VS Code
```plaintext
code .
```

### Step 3: Enable Agent Mode
- Open the **Copilot Chat** sidebar.
- Make sure **Agent Mode** is toggled ON.
- You’re now ready to start pasting the prompts below.

---

✅ You're all set to run this demo with GitHub Copilot Agent Mode. Paste each block above one at a time and enjoy the ride!

---

## 🧩 Step 1: Create Leaflet Map with OpenSky API
```plaintext
Create an HTML file named Leaflet-Airplanes-Demo.html that:

- Uses Leaflet.js to render a full-screen map.
- Fetches live airplane data from: https://opensky-network.org/api/states/all.
- Plots each airplane using latitude and longitude as Leaflet circleMarkers.
- Do NOT include any integrity or crossorigin attributes in the Leaflet.js or CSS links.

🛑 Stop after completing this step so I can review the output before continuing.
```

- Click **Keep** button to retain the generated code.

> [!TIP]
> Do not click **Done**, since we need to continue with the next steps.

- Open the HTML file in a browser to see the map with airplane markers.

It looks like we have quite a few markers here, which might make it a bit overwhelming to navigate. In the next step, let's apply a filter to narrow down our display and make things more manageable!"

---

## 🧩 Step 2: Filter for United Kingdom Flights
```plaintext
In Leaflet-Airplanes-Demo.html, filter the airplane markers so that only flights with:

  origin_country === "United Kingdom"

...are displayed on the map.

🛑 Stop after completing this so I can test tooltips and zoom behavior.
```

- Click **Keep** button to retain the generated code.

> [!TIP]
> Do not click **Done**, since we need to continue with the next steps.

- Refresh the HTML file in a browser to see the map with airplane markers.

Great job narrowing down the markers! Now we can focus on adding some data about each flight to make the display more informative. In the next step, let's enhance the user experience by adding some tooltips to provide quick details at a glance!

---

## 🧩 Step 3: Add Tooltips on Hover
```plaintext
Update the Leaflet-Airplanes-Demo.html file:

- Show a tooltip when hovering over an airplane marker.
- The tooltip should include:
  - Velocity (m/s)
  - Altitude (m)
  - Callsign
  - Heading (degrees)
- Tooltips must only appear when the map zoom level is greater than 5.

🛑 Stop after completing this so I can test tooltips and zoom behavior.
```
- Click **Keep** button to retain the generated code.

> [!TIP]
> Do not click **Done**, since we need to continue with the next steps.

- Refresh the HTML file in a browser, zoom in, the hoover over a marker to see the tooltip.

Fantastic work adding the tooltips! They make it so much easier to get quick details about each flight. In the next step, let's focus on refining the visuals or adding interactivity to make the display even more engaging by adding some color to the markers based on the flight status!

---

## 🧩 Step 4: Style Markers by Flight Status
```plaintext
In Leaflet-Airplanes-Demo.html, update the circleMarker color logic:

- Use red if the airplane is on the ground (on_ground: true).
- Use blue if the airplane is in flight (on_ground: false).
- Make sure markers are always visible, regardless of zoom level.

🛑 Pause here so I can check the updated marker styles.

```

- Click **Keep** button to retain the generated code.

- Click **Done** to complete this step.

- Refresh the HTML file in a browser, zoom in, and look for grounded aircraft in red.

Great work adding those advanced filtering options! Now, for the next step, let's create a new bubble map to visually represent the data in a dynamic and engaging way!

- Close the current HTML file.

---

## 🧩 Step 5: Visualize Airplane Counts by Country

#### First: Create AirplaneCountByCountry.json

Create a new file called airplane-count-by-country.json with the following content:

```plaintext
airplane-count-by-country.json
```

Add the following JSON data to the file:

```json
[
  { "name": "United States", "lat": 37.0902, "lon": -95.7129, "count": 1500 },
  { "name": "China", "lat": 35.8617, "lon": 104.1954, "count": 800 },
  { "name": "Russia", "lat": 61.524, "lon": 105.3188, "count": 300 },
  { "name": "Germany", "lat": 51.1657, "lon": 10.4515, "count": 200 },
  { "name": "United Kingdom", "lat": 55.3781, "lon": -3.436, "count": 100 }
]
```

✈️ This gives us real data to visualize airplane counts on the map!

I’ll guide Agent Mode step-by-step here — first we’ll create the HTML, then I’ll ask it to walk me through Python setup, running a local server, and opening the map. Watch how smoothly we can build this together!

##### Then: Create Leaflet-Airplane-Bubble.html

```plaintext
Create a new HTML file named Leaflet-Airplane-Bubble.html that:

- Uses Leaflet.js to render a full-screen map.
- Load data from the `airplane-count-by-country.json` file. Each object has:
  - name, lat, lon, and count.
- Display a bubble on the map at each lat/lon with:
  - Size and color based on count:
    - 0–100 = blue
    - 101–500 = yellow
    - 501–1000 = green
    - >1000 = red
- Show the airplane count in a tooltip on hover.
- Do NOT include any integrity or crossorigin attributes in the Leaflet.js or CSS links.

Before starting, tell me what’s about to happen:
1. You will create the HTML file.
2. Then you will guide me to install Python 3 if needed.
3. Then you will guide me to start a local server (python -m http.server 5500).
4. Then you will tell me to open the page at http://localhost:5500/Leaflet-Airplane-Bubble.html.

After each step, prompt me to click "Continue" before proceeding.

```

- Click **Keep** button to retain the generated code.

> [!TIP]
> Do not click **Done**, since we need to continue with the next steps.

Awesome — now that Copilot built our HTML file, let’s move on to setting up our environment. I’ll click Continue to guide it to the next step.

Paste the following prompts one at a time to guide Agent Mode through the remaining steps:

```plaintext
Now guide me through installing Python 3 if I don't already have it.
```

Perfect, now that we have Python ready, let's move to running our local server. I'll click Continue and ask Copilot to walk me through it.

```plaintext
Now guide me through starting a local server using python -m http.server 5500.
```

Nice — server’s running locally now! Next, I'll click Continue and have Copilot walk me through opening the map in the browser.

```plaintext
Now guide me to open the page at http://localhost:5500/Leaflet-Airplane-Bubble.html and check that the map works.
```

And there it is! Our map’s up and running, with real airplane data plotted — all guided smoothly by Copilot Agent Mode!

Fantastic job on the bubble map! It really brings the data to life. Next, let's fine-tune the map's styling to ensure it’s both visually appealing and easy to interpret.

> [!NOTE]
> What Is AirplaneCountByCountry.json?
> It's a JSON file with an array of objects, each representing a country's airplane count.
> Latitude and longitude for each country’s bubble placement are provided in the JSON.
> Leaflet.js doesn't know where to place bubbles on the map unless you give it coordinates.
> The OpenSky API gives you origin_country names — but not coordinates.

Great work bringing the airplane counts to life!
Your bubble map is now showing real-world data based on each country's airplane activity — and it looks fantastic!

Next, let’s make the map even sharper by updating the tile style, adding country boundaries, and making the bubbles dynamically adjust as you zoom in and out.

This will give our map a more polished and interactive feel!

---

## 🧩 Step 6: Add Custom Map Tiles and Country Boundaries

Now that your bubble map is working, let’s take it to the next level by upgrading the map’s background, adding country outlines, and making the bubbles dynamically scale when you zoom.

In this step, we’ll polish the bubble map by adding a new basemap, drawing country boundaries, and making the bubbles smoothly adjust when zooming.

### First: Create countries.geojson

Create a new file called `countries.geojson` with this sample content:

```plaintext
countries.geojson
```

Add the following JSON data to the file:

```json
{
  "type": "FeatureCollection",
  "features": [
    {
      "type": "Feature",
      "properties": { "name": "United Kingdom" },
      "geometry": {
        "type": "Polygon",
        "coordinates": [[
          [-5.0, 50.0], [-5.0, 58.0], [1.5, 58.0], [1.5, 50.0], [-5.0, 50.0]
        ]]
      }
    },
    {
      "type": "Feature",
      "properties": { "name": "United States" },
      "geometry": {
        "type": "Polygon",
        "coordinates": [[
          [-125.0, 24.0], [-125.0, 49.0], [-66.0, 49.0], [-66.0, 24.0], [-125.0, 24.0]
        ]]
      }
    },
    {
      "type": "Feature",
      "properties": { "name": "Germany" },
      "geometry": {
        "type": "Polygon",
        "coordinates": [[
          [5.5, 47.0], [5.5, 55.0], [15.5, 55.0], [15.5, 47.0], [5.5, 47.0]
        ]]
      }
    },
    {
      "type": "Feature",
      "properties": { "name": "France" },
      "geometry": {
        "type": "Polygon",
        "coordinates": [[
          [-5.0, 42.0], [-5.0, 51.0], [8.0, 51.0], [8.0, 42.0], [-5.0, 42.0]
        ]]
      }
    },
    {
      "type": "Feature",
      "properties": { "name": "Australia" },
      "geometry": {
        "type": "Polygon",
        "coordinates": [[
          [113.0, -44.0], [113.0, -10.0], [154.0, -10.0], [154.0, -44.0], [113.0, -44.0]
        ]]
      }
    }
  ]
}
```

> ✈️ *This creates simple country outlines matching the countries from your airplane count data!*

### Then: Update Leaflet-Airplane-Bubble.html

```plaintext
Enhance your `Leaflet-Airplane-Bubble.html` file to:

- **Replace** the default map tiles with a clean style, like:
  - CartoDB Positron:  
    `https://{s}.basemaps.cartocdn.com/light_all/{z}/{x}/{y}{r}.png`
- **Include attribution** for the tiles (required by the tile provider).
- **Load** and display the `countries.geojson` file.
- **Style the country boundaries**:
  - Border color: dark gray
  - Fill: transparent
  - Line weight: 1

### Update Bubble Behavior

- Make the **bubble size dynamically adjust** based on the map zoom level.
- Ensure **bubbles animate smoothly** when zooming in or out.
- Keep **bubbles always on top** of the country boundaries.

🛑 **Pause after completing this!**

```

I’ll review the tile style, country borders, and bubble zoom animations before we move forward.

> [!TIP]
> Smooth bubble resizing and better basemaps make your visualization feel professional and fun to explore!

---

## Pro Tips During Demo

> [!TIP]
> “Agent Mode works best with precise, atomic tasks.  
> Instead of feeding it everything at once, I guide it like a coworker—one clear ask at a time.”

## Notes
- Leaflet.js = free, no API key needed
- OpenSky has generous rate limits for testing
- This entire demo can run locally

