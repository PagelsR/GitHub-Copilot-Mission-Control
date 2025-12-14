# Prototyping: Live Aircraft Tracker with OpenSky Network

This document contains the complete project brief for building a real-time aircraft tracking web application using the OpenSky Network API.

## Description

A visually polished web application that displays live aircraft movements on a global interactive map. The app fetches real-time aircraft position data from OpenSky Network's free public API (no authentication required) and visualizes thousands of aircraft flying around the world with smooth animations, interactive tooltips, and detailed information panels.

## Key Features

- Real-time aircraft tracking with 10-second updates
- Interactive global map with custom aircraft icons
- Country and aircraft limit filters
- Click any aircraft for detailed information
- Visual trails showing recent flight paths
- Live status monitoring

## Technologies

- React + TypeScript + Vite
- Leaflet mapping library
- OpenSky Network REST API
- OpenStreetMap tiles

---

## Full Project Prompt

Copy and paste the prompt below:

```
# Live Aircraft Tracker - Project Brief

## Goal
Build a visually polished web app that displays live aircraft movements on a global map using the OpenSky Network public API with no API key required.

## Data Source
Use OpenSky Network API:
https://opensky-network.org/api/states/all

## Tech Stack
- Vite
- TypeScript
- React
- Leaflet
- OpenStreetMap tiles
- OpenSky Network REST API (JSON format)

## Constraints
- No authentication or API keys
- Client-side first
- Direct API calls (no proxy needed - CORS-friendly)

## Core Features
1) Live Map
   - Render aircraft markers at real-time positions
   - Rotate icons based on heading
   - Smooth position interpolation between updates
   - Update every 10 seconds (API rate limit)

2) Visual Polish
   - Custom aircraft SVG icon with subtle glow
   - Color-coded aircraft: blue for flying, red for on ground
   - Fading trail showing last 3 positions (match aircraft color)
   - Pulse animation on newly selected aircraft
   - Light mode map theme for visibility

3) Info Panel
   - Click an aircraft to open a side panel
   - Show callsign, ICAO24 ID, country, last update time
   - Show "seconds ago" freshness indicator
   - Display speed in knots and heading in degrees

4) Filter Controls
   - Country dropdown filter showing top 15 countries by aircraft count
   - "All Countries" option to show all aircraft (global view, zoom level 3)
   - Aircraft limit dropdown (100, 200, 300, 400, 500), default is 100
   - Filters update map display in real-time
   - Show count of visible vs total aircraft
   - When a country is selected, automatically zoom and center the map to that country's bounds
   - Define appropriate zoom levels and center coordinates for each top country
   - Smooth animated transitions when changing country selection

5) Status UX
   - Top-left status badge: Live / Stale / Error
   - Show last refresh timestamp
   - Graceful empty-state if feed is unavailable

## Architecture
- Create a VehicleProvider interface in FlightProvider.ts
- Implement OpenSkyProvider that fetches all aircraft (including grounded ones)
- Use flight-themed naming: FlightMap, useFlightData, flight.ts, FlightProvider
- Separate data parsing from UI rendering
- Keep provider swappable for other real-time APIs later
- Implement client-side filtering logic

## Implementation Details

### File Structure
- src/types/flight.ts - Vehicle, VehiclePosition, FlightProviderStatus interfaces
- src/providers/FlightProvider.ts - VehicleProvider interface
- src/providers/OpenSkyProvider.ts - Implements VehicleProvider
- src/components/FlightMap.tsx - Leaflet map with aircraft markers
- src/components/FlightMap.css - Map styling with .flight-map, .flight-icon, .flight-marker-selected
- src/components/FilterControls.tsx - Country and limit dropdowns
- src/components/InfoPanel.tsx - Aircraft details side panel
- src/components/StatusBadge.tsx - Live/Stale/Error indicator
- src/hooks/useFlightData.ts - Custom hook for fetching and managing aircraft data
- src/utils/aircraftIcon.ts - Generate SVG aircraft icons with rotation and color

### Country Zoom Coordinates
Define these country coordinates and zoom levels for smooth flyTo animations:
- United States: [39.8283, -98.5795], zoom 5
- Canada: [56.1304, -106.3468], zoom 4
- United Kingdom: [55.3781, -3.4360], zoom 6
- Germany: [51.1657, 10.4515], zoom 6
- France: [46.2276, 2.2137], zoom 6
- Spain: [40.4637, -3.7492], zoom 6
- Italy: [41.8719, 12.5674], zoom 6
- Turkey: [38.9637, 35.2433], zoom 6
- China: [35.8617, 104.1954], zoom 5
- Japan: [36.2048, 138.2529], zoom 6
- Australia: [-25.2744, 133.7751], zoom 5
- Netherlands: [52.1326, 5.2913], zoom 7
- Russia: [61.5240, 105.3188], zoom 3
- Ireland: [53.4129, -8.2439], zoom 7
- Malta: [35.9375, 14.3754], zoom 10
- India: [20.5937, 78.9629], zoom 5
- Brazil: [-14.2350, -51.9253], zoom 4
- Austria: [47.5162, 14.5501], zoom 7
- Mexico: [23.6345, -102.5528], zoom 5
- United Arab Emirates: [23.4241, 53.8478], zoom 7

### Color Coding
- Flying aircraft: blue (#0ea5e9 fill, #38bdf8 stroke)
- Grounded aircraft: red (#ef4444 fill, #dc2626 stroke)
- Trails match aircraft color
- Include onGround property in Vehicle interface

### Key Implementation Notes
- Parse OpenSky API array format (17+ elements per state)
- Include both flying and grounded aircraft (don't filter out on_ground)
- Use Leaflet's flyTo() for smooth country zoom transitions
- Store last 3 positions for trail visualization
- Update interval: 10 seconds (OpenSky rate limit)
- Convert velocity from m/s to knots for display (multiply by 1.944)

## Implementation Order
1) Scaffold project with Vite + React + TypeScript
2) Create type definitions in flight.ts (Vehicle with onGround property)
3) Implement OpenSkyProvider to fetch and parse aircraft data
4) Build FlightMap component with Leaflet, country coordinates, and zoom logic
5) Create aircraftIcon utility with color-coding (blue/red) and rotation
6) Add FilterControls with country dropdown and limit selector
7) Build InfoPanel and StatusBadge components
8) Implement useFlightData hook with position history tracking
9) Wire everything together in App.tsx with filter state management
10) Style with CSS animations and glassmorphism effects
11) Set default aircraft limit to 100

## Deliverables
- Running app showing live aircraft moving on a global map
- Working country and limit filters with automatic zoom
- Color-coded aircraft (blue flying, red grounded)
- Matching trail colors
- Clean, readable code with flight-themed naming
- Easy extension point for adding other real-time tracking APIs (ships, ISS, etc.)
```

---

## Usage Instructions

1. Copy the entire prompt section above (between the triple backticks)
2. Paste into your AI coding assistant
3. The assistant will scaffold and build the complete application
4. Run `npm install` to install dependencies
5. Run `npm run dev` to start the development server
6. Open browser to view live aircraft tracking

## API Information

**OpenSky Network API**
- Endpoint: `https://opensky-network.org/api/states/all`
- Rate Limit: 10 seconds between requests (anonymous users)
- Authentication: None required
- Format: JSON
- Coverage: Global aircraft positions
- Data includes: position, altitude, velocity, heading, callsign, country

## Potential Enhancements

- Add altitude visualization (color-coded markers)
- Flight path history over longer periods
- Airport overlay with live departures/arrivals
- Search by callsign or ICAO24
- Multiple map themes (satellite, terrain)
- Statistics dashboard (busiest routes, countries, etc.)
- Export flight data to CSV
