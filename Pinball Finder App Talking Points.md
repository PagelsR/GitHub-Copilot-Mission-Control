# ✈️ GitHub Copilot Agent Mode: Build a Python Pinball Finder App

**Estimated Duration: 20 minutes**

A step-by-step demo for using GitHub Copilot Agent Mode to build a Pinball Finder app in Python. This project guides Copilot Agent Mode through atomic tasks, letting you build a complete airplane tracking app by pasting one prompt at a time. No live server or cloud deployment required — it all runs locally!

---

## Getting Started

Before using GitHub Copilot Agent Mode:

### Step 1: Create a Project Folder
```plaintext
mkdir pinballfinderapp && cd pinballfinderapp
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



## 🚀 Agent Mode Demo: Python Pinball Finder App

### **Prompt:**
```plaintext
Build a Python app that finds the nearest pinball machines based on user location. Use the Open Pinball Map API to fetch machine data and display it on a map.
```

### **Prompt Details:**
```plaintext
Let's build a project from scratch that will connect to the public Pinball Map API (docs: https://pinballmap.com/api/v1/docs/1.0.html).

Core Requirements
Language: Python
Source Control: Use Git. Create a gitignore file. Initialize the project.
Package Management: Use Poetry. Initialize the project (poetry init) and manage dependencies.
Project Structure: Create a best practices Python project structure
Project Architecture: Monolithic but modular design to ensure clear separation of concerns.
API Client: Implement logic to interact with the Pinball Map API. Start with fetching locations by zip code (likely using the /locations/by_zip_code.json endpoint).
GUI: Create a simple GUI. Our team uses pyside6.
First Feature:
Allow the user to input a zip code into the GUI.
On submission, fetch all locations and their machines for that zip code from the API.
Show locations.
Determine the top 3 most frequently appearing machine names across all locations found in that zip code. (An API endpoint exists for this.)
Combine and display these top 3 machine names, for each location, in the GUI as a sample of what's available in the area.
```


### **1. Intro: What Is Copilot Agent?**

* **“GitHub Copilot Agent is an AI teammate that works alongside you right in your GitHub repo.”**
* “Instead of just helping in your editor, Copilot Agent takes Issues assigned to it and actually starts doing the work—setting up code, opening PRs, and providing updates right inside GitHub.”

---

### **2. How Does It Work?**

* “I can write out Issues—just like normal tasks for my team—but now, I assign them to the Copilot Agent.”
* “Copilot Agent reads the Issue, understands the requirements, and works just like a developer would. It will propose changes, create code, and open a pull request for review.”

---

## Project Goal: Build a Python Pinball Finder App

### **3. Step-by-Step Demo Flow**
Using GitHub Copilot Agent Mode from Visual Studio Code, you can walk through a demo of how Copilot Agent works. Here’s a suggested flow:

* Open Copilot Agent Mode in Visual Studio Code.
* Create a new Python project for the Pinball Finder app.
* Paste this prompt into the Copilot Agent Mode:

  ```
  Build a Python app that finds the nearest pinball machines based on user location. Use the Open Pinball Map API to fetch machine data and display it on a map.
  ```

  OR

```
Let's build a project from scratch that will connect to the public Pinball Map API (docs: https://pinballmap.com/api/v1/docs/1.0.html).

Core Requirements
Language: Python
Source Control: Use Git. Create a gitignore file. Initialize the project.
Package Management: Use Poetry. Initialize the project (poetry init) and manage dependencies.
Project Structure: Create a best practices Python project structure
Project Architecture: Monolithic but modular design to ensure clear separation of concerns.
API Client: Implement logic to interact with the Pinball Map API. Start with fetching locations by zip code (likely using the /locations/by_zip_code.json endpoint).
GUI: Create a simple GUI. Our team uses pyside6.
First Feature:
Allow the user to input a zip code into the GUI.
On submission, fetch all locations and their machines for that zip code from the API.
Show locations.
Determine the top 3 most frequently appearing machine names across all locations found in that zip code. (An API endpoint exists for this.)
Combine and display these top 3 machine names, for each location, in the GUI as a sample of what's available in the area.
```



Using GitHub Issues and PRs, you can walk through a demo of how Copilot Agent works. Here’s a suggested flow:

#### **a. Assign the First Issue**

* “Let’s start by assigning this first Issue—‘Initialize Python project with Poetry and Git’—to the Copilot Agent.”
* “Notice how quickly the Agent picks it up and starts commenting as it works.”

#### **b. Watch the Progress**

* “You can see Copilot Agent updating the Issue with what it’s doing, and opening a PR with its changes.”
* “Everything happens transparently. The code changes are visible, and you can review them just like with any other team member.”

#### **c. Move Through Each Task**

* “Once the Agent finishes and closes this Issue, I’ll assign the next task—building the API client, then the GUI, and so on.”
* “This step-by-step approach lets you guide the Agent through your development process, and you always stay in control.”

---

### **4. Key Features to Highlight**

* **Autonomy:** “Copilot Agent doesn’t just suggest code—it actually does the work and submits it for review.”
* **Transparency:** “All its actions are visible in Issues, PRs, and commit history. Nothing is hidden.”
* **Control:** “You choose which Issues to assign, and you review and merge the PRs. It’s like a junior developer you can supervise and teach.”

---

### **5. Why This Is a Game Changer**

* “This dramatically speeds up basic project setup and repetitive tasks.”
* “It frees up your team to focus on trickier problems and lets the Agent handle the boilerplate.”
* “You’re still in charge of quality—review, request changes, or even close PRs you don’t want.”

---

### **6. Final Thoughts**

* “GitHub Copilot Agent isn’t just about code completion—it’s about actual collaboration and automation.”
* “This workflow lets anyone, from solo devs to teams, work smarter and build faster.”

---

**Pro Tip:** If anyone asks, “Can I assign everything at once?”—let them know it’s best to assign Issues one at a time, so you can monitor, review, and keep the process smooth.


