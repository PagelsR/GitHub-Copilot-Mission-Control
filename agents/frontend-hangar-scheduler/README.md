# Frontend Agent Mode, Hangar Bay Scheduler

**Goal**  
Create a reservation UI for hangar bays with daily and weekly views, filters, and a modal.

**Time** 15 to 25 minutes

## Prerequisites
- Node.js and npm

## Step 0, Guardrail
Copy into Agent Mode.
```
If you create or modify React components with hooks, ensure all necessary imports are present.
```

## Step 1, Create app
Copy into Agent Mode.
```
Scaffold a React app using Vite in the current folder. Add a README with scripts and a copilot-instructions.md with common pitfalls.
Stop after setup.
```

## Step 2, Mock reservations
Copy into Agent Mode.
```
Create mock reservations across 10 hangar bays using 90 minute slots with ~70% filled. 
Render a grid, bays as columns and time slots as rows.
```

## Step 3, Improve UX
Copy into Agent Mode.
```
Modernize the daily view using a responsive grid. Add an Add Reservation button on empty slots.
```

## Step 4, Core usability
Copy into Agent Mode.
```
Color empty slots green. Add a filter for available times. Allow marking a reserved slot available again.
```

## Step 5, Weekly view and toggle
Copy into Agent Mode.
```
Add a weekly view and a UI toggle between daily and weekly. Prepare room for a future search bar.
```

## Step 6, Modal with delete
Copy into Agent Mode.
```
Create a modal to view, edit, and add reservations. Include Save, Cancel, and Delete. Delete only in edit mode.
```

## Step 7, Pilot search
Copy into Agent Mode.
```
Add a search bar that filters by pilot name with partial, case insensitive matching.
```

## Step 8, Double booking guard
Copy into Agent Mode.
```
When adding a reservation, prevent the same bay and time from being double booked. Disable taken slots with an explanation.
```

## Step 9, Toasts
Copy into Agent Mode.
```
Add toast notifications for create, update, and delete. Auto dismiss quickly.
```
