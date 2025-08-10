# GitHub Copilot Agent Mode: Live ISS Tracker

⏱️ **Estimated Duration: 15–25 minutes**

Track the International Space Station (ISS) in real time on a Leaflet.js map using GitHub Copilot Agent Mode and the free Open Notify API. 

No live server or cloud deployment required — it all runs locally!

---

## Getting Started

Before using GitHub Copilot Agent Mode:

### Step 1: Create a Project Folder
```plaintext
mkdir iss-tracker-demo && cd iss-tracker-demo
```

### Step 2: Open the Folder in VS Code
```plaintext
code .
```

### Step 3: Enable Agent Mode
- Open the **Copilot Chat** sidebar.
- Toggle **Agent Mode** ON.
- You’re now ready to start pasting the prompts below.

✅ You’re ready to launch this demo with Copilot Agent Mode. Paste one prompt at a time, and let Copilot do the work.

## 🧩 Step 1: Create Basic ISS Map Page
```plaintext
Create an HTML file named ISS-Tracker.html that:

- Loads Leaflet.js and displays a full-screen world map.
- Places a marker labeled “ISS” at coordinates fetched from:
  http://api.open-notify.org/iss-now.json
- The API returns:
  {
    "iss_position": {
      "latitude": "47.6062",
      "longitude": "-122.3321"
    },
    "timestamp": 1687290545,
    "message": "success"
  }
- Position the marker at the ISS coordinates.
- Do NOT include integrity or crossorigin attributes in the Leaflet.js or CSS links.
```

🛑 Stop here so I can confirm the map loads and the ISS marker appears.

- Click **Keep** when the HTML is generated.
- Open the page in your browser — you should see an ISS marker somewhere over Earth.

Great start! Let’s make it dynamic.

## 🧩 Step 2: Add Live Auto-Update Every 5 Seconds
```plaintext
Update ISS-Tracker.html so that:

- The ISS marker updates its position every 5 seconds.
- Fetch the new coordinates from the same API:
  http://api.open-notify.org/iss-now.json
- Smoothly move the marker to its new location.
- Update the map’s center to follow the ISS.
```

- Click **Keep** and refresh the browser.
- Watch the ISS slowly move across the globe!

Looking good! Let’s give it some more visual polish and context.

## 🧩 Step 3: Add Custom Icon and Info Tooltip
```plaintext
Update ISS-Tracker.html to:

- Replace the default marker with a small custom satellite icon.
- Add a tooltip that appears on hover showing:
  - “International Space Station”
  - Timestamp (formatted as local time)
  - Latitude and Longitude
```

- Click **Keep**, refresh the browser, and hover over the marker.

Now that looks like an ISS tracker!

## 🧩 Step 4: Switch to a Better Basemap and Add Attribution
```plaintext
Update the map to use the CartoDB Positron tile layer:
`https://{s}.basemaps.cartocdn.com/light_all/{z}/{x}/{y}{r}.png`

- Add the required attribution for CartoDB and Open Notify.
- Set the zoom level to 2 for a global view.
- Disable scroll wheel zoom for better control.
```

- Click **Keep** and verify the map background and attribution look clean.

Awesome! You’ve got a professional-looking ISS tracker — and you built it locally, with zero setup.

## ✅ Demo Complete!

You now have a real-time ISS tracker powered by a public API, built entirely with GitHub Copilot Agent Mode.

> [!TIP]
> This demo uses only client-side code, a single HTML file, and a free no-auth API — ideal for quick demos and teaching how Agent Mode works with APIs and maps.

---

## 🚀 Bonus Challenge (Optional)

```plaintext
Ask Copilot to:
- Show the next ISS pass time over your current location.
- Add a trail line that shows the last 5 positions.
- Style the trail to fade out over time.
```
