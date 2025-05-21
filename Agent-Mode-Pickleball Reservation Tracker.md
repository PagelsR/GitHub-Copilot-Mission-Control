
# 🎾 GitHub Copilot Agent Mode: Pickleball Reservation Tracker

⏱️ **Estimated Duration: 15–20 minutes**

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

✅ You're all set to run this demo with GitHub Copilot Agent Mode. Paste each block above one at a time and enjoy the ride!

---

## 🧩 Step 1: Create Single Page React app
```plaintext
- Create a single page application using React. 
- The app will allow me to keep track of pickleball court reservations in a facility with 10 courts. I want to be able to see things on a daily and weekly basis.

🛑 Stop after completing this step so I can review the output before continuing.
```

- Follow the prompts to run npm commands
- Click **Keep** button to retain the generated code.

> [!TIP]
> Do not click **Done**, since we need to continue with the next steps.

- Open the app in a browser to see the new functionality.

The page looks a bit sad with no data, so let's add some data in the next step.

---

## 🧩 Step 2: Add some data
```plaintext
Create mock data to be able to populate the schedule, broken down into 90 minute reservations.

🛑 Stop after completing this so I can test tooltips and zoom behavior.
```

- Click **Keep** button to retain the generated code.

> [!TIP]
> Do not click **Done**, since we need to continue with the next steps.

- Refresh your browser to see the data.

Great job giving your page some data so that you can really start working with it!

---

## 🧩 Step 3: Improve the look and feel
```plaintext
- Let's enhance the daily view to give it a more visually appealing view, like a calendar view.
- Add a way to add a new reservation, including the Court, time, and player name

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

```plaintext
Implement a Weekly view functionality that shows each day of the week in a calendar view
```

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

