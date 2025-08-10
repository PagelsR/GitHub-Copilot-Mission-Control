# 🕹️ GitHub Copilot Coding Agent: Build a Python Pinball Finder App

**Estimated Duration: 20 minutes**

A step-by-step demo for using GitHub Copilot Coding Agent to build a Pinball Finder app in Python. This project guides Copilot Coding Agent through atomic tasks, letting you build a complete airplane tracking app by pasting one prompt at a time. No live server or cloud deployment required — it all runs locally!

## About the Pinball Finder API
The Public Pinball API is a RESTful web service provided by Pinball Map that allows developers to access data about pinball machines, locations, regions, and events. The API is open and does not require authentication for most endpoints, making it easy to integrate pinball-related data into your applications.

Key Features:
- Retrieve lists of pinball locations, machines, and regions.
- Search for locations by coordinates, city, or region.
- Access information about events, operators, and machine details.
- Submit suggestions or corrections to the database

For more information, check out the [Pinball Map API documentation](https://pinballmap.com/api/v1/docs/1.0.html).


## 🚀 Coding Agent from GitHub.com: Python Pinball Finder App


## ✅ Step 1 — Setup

### Initialize Python Pinball Finder Project Structure (Poetry + Git)

1. Create a new empty GitHub repository for the `pinball-finder` project in your GitHub account.
1. Initialize this repository with:
  - Add a `.gitignore` file tailored for Python and Poetry.
  - Add a `README.md` file.

1. Add the repository to list **Only selected repositories** in the Copilot settings.

1. Clone the empty repository to your local machine:

```sh
git clone [https://github.com/yourusername/pinball-finder.git](https://github.com/yourusername/pinball-finder.git)
```

1. Open repo using VS Code:
1. Run `poetry init` in the terminal to set up dependency management.

```sh
python -m poetry init
```

1. Scaffold the project directory structure:
   - `src/`
   - `tests/`

1. Push the changes to GitHub:

#### 🔄 Recommendation for Repeating This Demo:

Each time you want to demo this project:

1. Create a new empty GitHub repository under your account.
2. Clone the new empty repository locally.
3. Set up the project structure and dependencies as above.
4. Push your changes to GitHub.
5. Create new issues (using these issue templates) directly on GitHub.com.

---

✅ You're all set to run this demo with Coding Agent. Create each Issue below but do not assign it, enjoy the ride!

---

## ✅ Step 2 — Issue Creation

> Create new issues (using these issue templates) directly on GitHub.com.

### 📂 Issue 1

Title:
```
Implement Pinball Map API Client (Locations by Zip)
```

Steps to Reproduce
```
Steps to Reproduce:

1. Review the Pinball Map API docs: https://pinballmap.com/api/v1/docs/1.0.html
2. Create a new file at `src/pinballmap/client.py`.
3. Implement a `get_locations_by_zip(zip_code: str)` function to fetch and parse the `/locations/by_zip_code.json` endpoint.
4. Return a structured list of locations and machines as Python objects.
5. Write unit tests in `tests/test_client.py` to verify client functionality.
```

#### 🔄 Recommendation for Repeating This Demo:

After pushing the scaffolded repo to GitHub, create this issue on GitHub.com to track the client implementation.

---

### 📂 Issue 2

Title:
```
Create PySide6 GUI for Pinball Finder App
```

Steps to Reproduce
```
Steps to Reproduce:

1. Create a new file at `src/pinballmap/gui.py` for the PySide6 GUI.
2. Add a text input for zip code.
3. Add a submit button that triggers the `get_locations_by_zip()` client function.
4. Display the returned list of locations in the GUI.
5. Ensure signal/slot connections between the input, button, and list view are properly implemented.
```

#### 🔄 Recommendation for Repeating This Demo:

Once the client issue is completed and pushed, create this issue on GitHub.com to begin GUI work.

---

### 📂 Issue 3

Title:
```
Add Top 3 Frequent Machines Feature
```

Steps to Reproduce
```
Steps to Reproduce:

1. Extend the API client to also retrieve the top 3 most frequently appearing machines for each zip code.
2. Modify the GUI to:
   - Show each location with its top 3 machines displayed underneath.
   - Maintain a responsive layout using PySide6 best practices.
3. Write tests to validate the new behavior in `tests/test_client.py`.
```

#### 🔄 Recommendation for Repeating This Demo:

Create this issue on GitHub.com after pushing and verifying the GUI issue is completed.


## Demo walkthrough

### Step 1: Edit Issue 1 - Implement Pinball Map API Client

- Assign Issue 1 to Coding Agent.
- Watch as Coding Agent reads the issue, creates the necessary files, and starts implementing the API client.

> When Copilot mentioned this and you see [WIP] click on it to see the PR.

- Click **View Session** to see the Copilot Agent's progress.
- Review the code changes and tests generated by Coding Agent.
- Merge the PR once you're satisfied with the implementation.
- From Visual Studio Code, pull the changes from the main branch.

### Step 2: Edit Issue 2 - Create PySide6 GUI for Pinball Finder App 
- Assign Issue 2 to Coding Agent.
- Watch as Coding Agent reads the issue, creates the necessary files, and starts implementing the API client.

> When Copilot mentioned this and you see [WIP] click on it to see the PR.

- Click **View Session** to see the Copilot Agent's progress.
- Review the code changes and tests generated by Coding Agent.
- Merge the PR once you're satisfied with the implementation.
- From Visual Studio Code, pull the changes from the main branch.


## Demo Talking Points

### **1. Intro: What Is Copilot Agent?**

* **“GitHub Copilot Agent is an AI teammate that works alongside you right in your GitHub repo.”**
* “Instead of just helping in your editor, Copilot Agent takes Issues assigned to it and actually starts doing the work—setting up code, opening PRs, and providing updates right inside GitHub.”

---

### **2. How Does It Work?**

* “I can write out Issues—just like normal tasks for my team—but now, I assign them to the Copilot Agent.”
* “Copilot Agent reads the Issue, understands the requirements, and works just like a developer would. It will propose changes, create code, and open a pull request for review.”

---




--- 


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


