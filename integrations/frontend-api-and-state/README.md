# Frontend API and State

## Mission
Wire the React app to the backend API with a simple data hook, add loading and error UI, and a basic test.

## Why this matters
Reliable data fetching patterns make the UI feel solid and demo well.

## Copilot modes
Chat to scaffold, Edits to apply consistent patterns.

## Prerequisites
- Backend API running locally
- React app in VS Code
- React Testing Library available, or let Copilot add it

## Steps
1) Create a data hook
Chat prompt
> Create a usePlanes hook that fetches from http://localhost:1903/planes with axios, returns { data, loading, error }, and handles cancellation on unmount.

2) Apply the hook
Edits prompt
> Replace inline fetch logic in PlaneList with usePlanes. Add loading and error states with simple UI.

3) Add a basic test
Chat prompt
> Generate a test using React Testing Library that renders PlaneList, mocks the hook, and verifies loading state and rendering two planes.

4) Confirm manual flow
```bash
npm test
npm run dev
```

5) Optional, accessibility pass
Chat prompt
> Suggest three quick a11y improvements, like roles, labels, and keyboard focus cues. Apply the smallest change across the list and its items.
