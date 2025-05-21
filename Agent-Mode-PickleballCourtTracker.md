# 🎾 GitHub Copilot Agent Mode: Pickleball Court Tracker

⏱️ **Estimated Duration: 20 minutes**

A step-by-step demo for using GitHub Copilot Agent Mode to build an interactive reservation system for pickleball courts.

This project guides Copilot Agent Mode through atomic tasks, letting you build a complete reservation app by pasting one prompt at a time. No live server or cloud deployment required — it all runs locally!

---

## Getting Started

Before using GitHub Copilot Agent Mode:

### Step 1: Create a Project Folder
```plaintext
mkdir pickleball-reservations-demo && cd pickleball-reservations-demo
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

> [!IMPORTANT]
> 💡 When Copilot creates or updates a React component:
> - Always check that `React`, `useState`, `useEffect`, or any other hooks are properly imported.
> - Missing imports can silently break your app, resulting in a blank screen.
> - Even if using Vite or a modern React setup that hides some imports, being explicit during demos helps prevent confusion and errors.

---

## 🧭 Step 0: Starter Message for Agent Mode
```plaintext
Before we begin, please remember to always import the necessary React functions.

If you create or modify any components using JSX or React hooks (like useState or useEffect), make sure to include:

import React, { useState, useEffect } from 'react';

Even if you're using Vite or modern React, missing imports may cause blank screens or unexpected behavior. Let's get started building the Pickleball Reservation Tracker now!
```

✅ Paste that into the first prompt window before you start giving Copilot steps. It helps set the tone and prevent silent errors later in the demo.

✅ You're all set to run this demo with GitHub Copilot Agent Mode. Paste each block above one at a time and enjoy the ride!

---

## 🧩 Step 1: Create Single Page React app

Let’s set up the folder structure, create a Copilot instructions file, and initialize our project.

```plaintext
- Create a new project folder called `pickleball-reservations-demo`
- Inside that folder, create a file named `copilot-instructions.md` and save in folder called .github.
- This file should include Copilot Agent Mode guidance, including:
  - A starter message to paste into Copilot Agent Mode
  - Best practices (like using atomic prompts and avoiding missing imports)
  - Common issues like blank screens caused by missing React imports
- Then, initialize a basic React app in this folder using your preferred setup method

🛑 Stop after completing this step so I can review the project setup.
```

> [!TIP]
> 💡 The `copilot-instructions.md` file helps prevent common errors and makes it easier to share this demo with others.


- Follow the prompts to run npm commands
- Click **Keep** button to retain the generated code.

> [!TIP]
> Do not click **Done**, since we need to continue with the next steps.

- Open the app in a browser to see the new functionality.

The page looks a bit sad with no data, so let's add some data in the next step.

---

## 🧩 Step 2: Add some data
```plaintext
- Create mock reservation data for the pickleball schedule using about 20 unique first names.
- Randomly assign reservations to 10 courts, using 90-minute time blocks throughout the day.
- Ensure that only about 70% of the possible time slots are filled (leave the rest empty for realism).
- The data structure should support Player Name, Court Number, Start Time, and End Time.
- Also, update the main app component to display this data in the calendar/grid view.


Ensure that only about 70% of the possible time slots are filled (leave the rest empty for realism).
The data structure should support Player Name, Court Number, Start Time, and End Time.
Also, update the main app component to display this data in the calendar/grid view.

🛑 Stop after completing this so I can test tooltips and zoom behavior.
```

- Click **Keep** button to retain the generated code.

> [!TIP]
> Do not click **Done**, since we need to continue with the next steps.

- Refresh your browser to see the data.

Great job giving your page some data so that you can really start working with it!

---

## 🧩 Step 3: Improve the look and feel

Let’s enhance the daily view to look more like a modern calendar layout with the ability to add new reservations.

```plaintext
- Enhance the daily view to look more like a modern calendar layout.
- Use a card or grid layout to show reservations per court and time.
- Make the calendar view responsive so that it adjusts nicely across screen sizes instead of shrinking the font.

🛑 Stop after completing this so I can test tooltips and zoom behavior.
```
- Click **Keep** button to retain the generated code.

> [!TIP]
> Do not click **Done**, since we need to continue with the next steps.

- Refresh the page and test out the new functionality.

---

## 🧩 Step 4: Let's make it easier to use
```plaintext
- On each court, show the available slots in Green so that they are easily identifiable
- Add the ability to make a reservation directly from an available slot
- Add a way to filter by Available times
- Add a way to make a reserved court available by clicking on a red icon

🛑 Pause here so I can check the updated functionality.

```

- Click **Keep** button to retain the generated code.

- Click **Done** to complete this step.

- Refresh the page, and test the new features.

Great work adding usability features! 

---

## 🧩 Step 5: Visualize the full week

Let’s add a weekly calendar view so users can get a full snapshot of reservations across all days.

```plaintext
Implement a Weekly view functionality that shows each day of the week in a calendar view

🛑 Pause here so I can review the layout.
```

---

## Step 6: Add Reservation Details Modal with Delete Functionality

Now we’ll add a modal to view, edit, or delete a reservation when a user clicks on a reserved slot.

```plaintext
- Add a modal component that can be used to view, edit, or create a reservation.
- When a user clicks on an existing reservation, open the modal pre-filled with that reservation's details.
- When a user clicks on the “Add Reservation” button, open the same modal in empty/create mode.
- Include inputs for Player Name, Time, and Court.
- Add Save, Cancel, and Delete buttons.
- The Delete button should only appear in edit mode and should remove the reservation.
- Make sure the modal has a clean layout and works on desktop and mobile.

🛑 Stop after this step so I can review the modal interaction and test the full create/edit/delete flow.
```

---

We’re enhancing the UX by adding a toggle so users can switch between daily and weekly views on demand.

## Step 7: Add Toggle for Weekly View

We’re enhancing the UX by adding a toggle so users can switch between daily and weekly views on demand.

```plaintext
- Add a toggle or button group to switch between Daily and Weekly views.
- Place the toggle near the top of the calendar.
- Reserve space to the right of the toggle for a search input (will be added in next step).
- Use flex layout or a simple horizontal container to align the view toggle and future search input on the same row.
🛑 Pause here so I can review how the toggle and layout behavior.
```

---

##  Step 8: Add Player Search and Filter

To help users quickly find reservations, we’ll implement a player search bar with partial name matching.

```plaintext
- Add a search bar to filter reservations by player name (supporting partial, case-insensitive matches).
- Place the search bar between the Weekly View and Add Reservation button in the top bar, using a flex layout so all three controls are aligned and responsive.
- As the user types, filter the visible reservations to only show matches.
- As the user types, filter the visible reservations in both daily and weekly views to only show matches.
🛑 Stop after this step so I can test the filtering behavior.
```

---

## Step 9: Prevent Double-Booking

Let’s ensure reservation accuracy by preventing double-booking of the same court and time.

```plaintext
- When adding a new reservation, check for existing reservations at the same time on the same court.
- If a time slot is already taken, disable it in the reservation form.
- Optionally, show a tooltip or message explaining why a slot is disabled.
🛑 Pause here so I can test double-booking prevention.
```

---

## 🧩 Step 10: Add User Feedback

To enhance the user experience, we’ll add toast notifications for actions like booking success or cancellation.

```plaintext
- Add toast notifications or alert messages for common user actions:
  - Show a success message when a reservation is successfully made.
  - Display a confirmation when a reservation is cancelled.
  - Show error messages if something goes wrong, like trying to double-book.
- Ensure the toasts are visible but non-intrusive and disappear after a few seconds.
🛑 Pause here so I can verify the feedback notifications work as expected.
```

---

## 🧩 Step 11: Add Court Availability Summary

Let’s provide a quick overview of court availability for the day in the Daily view.

```plaintext
- Add a sidebar widget to the right of the main calendar view.
- This widget should include:
  - A list of courts with the most available time slots *today*.
  - The next available time slot for each court.
- Sort courts so the ones with the most availability appear first.
- Make sure it updates dynamically when new reservations are added or removed.
- Use simple text or a clean list layout to keep it readable.

🛑 Pause here so I can review the availability summary and verify it's working correctly.
```

---

## 🚀 Congratulations!

And there it is! Our app is up and running, with some mock data and the ability to add and delete reservations — all guided smoothly by Copilot Agent Mode!

---

## Pro Tips During Demo

> [!TIP]
> “Agent Mode works best with precise, atomic tasks.  
> Instead of feeding it everything at once, I guide it like a coworker—one clear ask at a time.”

## Notes
- Leaflet.js = free, no API key needed
- OpenSky has generous rate limits for testing
- This entire demo can run locally

