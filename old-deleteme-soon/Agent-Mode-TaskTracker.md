# GitHub Copilot Agent Mode: Task Tracker with Local Persistence

⏱️ **Estimated Duration: 25–35 minutes**

Build a fully functional task tracker app — from scratch — using GitHub Copilot Agent Mode. You'll create a polished UI with task creation, editing, deletion, and filtering logic, all backed by browser `localStorage`.

No frameworks. No backend. No setup. Just HTML, CSS, and JavaScript — running entirely local.

---

## Getting Started

Before using GitHub Copilot Agent Mode:

### Step 1: Create a Project Folder
```plaintext
mkdir task-tracker-agent && cd task-tracker-agent
```

### Step 2: Open the Folder in VS Code
```plaintext
code .
```

### Step 3: Enable Agent Mode
- Open the **Copilot Chat** sidebar.
- Make sure **Agent Mode** is toggled ON.
- You're ready to go!

✅ You're all set. Paste each step below into Agent Mode one at a time.

## Step 1: Create the HTML Layout
```plaintext
Create an HTML file named TaskTracker.html that:

- Includes a title “Task Tracker”
- Has an input box to add a new task and a button labeled “Add Task”
- Contains a section below that shows the list of tasks
- Each task should have:
  - The task text
  - A checkbox to mark it complete
  - An “Edit” button
  - A “Delete” button
- Wrap everything in a container and link to an external stylesheet (style.css)
```

🔝 Pause so I can review the structure before styling.

## Step 2: Style the App
```plaintext
Create a file called style.css and link it to TaskTracker.html.

Style the task tracker so that:
- It’s centered with a max width of 600px
- Input and buttons are spaced and styled cleanly
- Tasks are in a clean card-like layout
- Completed tasks appear with strikethrough text and dimmed color
- The app uses a modern sans-serif font and has a light gray background
```

✅ Click Keep to save the CSS, then refresh the browser.

Let's move on to the interactivity!

## Step 3: Add Task Logic with JavaScript
```plaintext
Create a file called script.js and link it to TaskTracker.html.

Implement JavaScript that:
- Adds a task when the “Add Task” button is clicked
- Updates the task list in the DOM
- Allows marking tasks as complete
- Allows deleting tasks
- Adds basic input validation (don’t add empty tasks)
```

✅ Click Keep and test task creation, marking complete, and deletion.

Now let's make it persistent!

## Step 4: Store and Load Tasks with localStorage
```plaintext
Update script.js so that:

- When a task is added/updated/deleted/completed, update localStorage
- On page load, load tasks from localStorage and render them
- Store tasks as an array of objects with:
  - id, text, completed (boolean)

Make sure the state persists after a page reload.
```

✅ Confirm tasks save and reload correctly.

Let's add editing and filters next.

## Step 5: Add Task Editing
```plaintext
Update script.js so that:

- Each task’s “Edit” button turns the text into an input field
- When the user confirms the edit (e.g. presses Enter or clicks Save), update the task text
- The updated task should save to localStorage and re-render
```

✅ Test editing and saving, then reload to confirm persistence.

Looking sharp — let's add filters!

## Step 6: Add Filter Controls
```plaintext
Above the task list, add filter buttons:
- “All”, “Active”, and “Completed”

Update script.js so that:
- Clicking a filter shows only the appropriate tasks
- Selected filter is highlighted
- Filtering doesn’t modify the stored task list
```

✅ Click Keep and confirm the filter logic works.

Now let’s top it off with a nice touch…

## Step 7: (Optional) Add Dark Mode Toggle
```plaintext
Add a dark mode toggle button at the top-right of the app.

Implement logic to:
- Toggle a `dark-mode` class on the body
- Change the CSS to support dark background and light text
- Save the theme preference to localStorage
- Load the preferred theme on startup
```

✅ Click Keep, test it out, and admire your work!

## ✅ Demo Complete!

You’ve built a fully functional task tracker with GitHub Copilot Agent Mode — complete with local persistence, filtering, editing, and optional dark mode.

> [!TIP]
> This is a great showcase of Copilot Agent Mode’s ability to scaffold an app step-by-step, turning basic prompts into a real, usable interface — no setup required.

---

## 💡 Bonus Challenge
```plaintext
Ask Copilot to:
- Add drag-and-drop reordering of tasks
- Add due dates with sorting by deadline
- Export the task list to JSON
```
