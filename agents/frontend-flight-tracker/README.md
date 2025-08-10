# Frontend Agent Mode, Flight Tracker with Leaflet.js

**Goal**  
Build a Leaflet map that visualizes planes from the API with a country filter, tooltips, and auto refresh.

**Time** 12 to 18 minutes

## Prerequisites
- Backend API running at http://localhost:1903/planes
- Python for a local static server, or VS Code Live Server

## Step 1, Base map and dropdown
Copy into Agent Mode.
```
Create flight_leaflet_demo.html that:
- Loads Leaflet with a full screen map centered on [37.8, -96], zoom 5
- Adds a <select> with United States, United Kingdom, Ireland, Germany, Australia
- Adds CSS for larger tooltip font
Stop after creating the file.
```

## Step 2, Fetch and plot
Copy into Agent Mode.
```
In flight_leaflet_demo.html, fetch from http://localhost:1903/planes. 
Assume fields: callsign, originCountry, latitude, longitude, velocity, altitude, heading, onGround. 
Filter by selected country. Limit to 50. Plot markers. 
Blue if onGround=false, red if true. Tooltip shows callsign, velocity, altitude, heading.
```

## Step 3, Stats, selection, auto refresh
Copy into Agent Mode.
```
Add an overlay showing number of planes. On marker click, highlight and show a detail panel. 
Add a toggle to auto refresh every 30 seconds and keep selection if still present.
```

## Run locally
```bash
python -m http.server
# open http://localhost:8000/flight_leaflet_demo.html
```
