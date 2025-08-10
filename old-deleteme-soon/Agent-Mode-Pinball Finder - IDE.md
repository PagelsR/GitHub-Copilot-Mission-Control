# 🕹️ GitHub Copilot Agent Mode: Build a Python Pinball Finder App

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

## About the Pinball Finder API
The Public Pinball API is a RESTful web service provided by Pinball Map that allows developers to access data about pinball machines, locations, regions, and events. The API is open and does not require authentication for most endpoints, making it easy to integrate pinball-related data into your applications.

Key Features:
- Retrieve lists of pinball locations, machines, and regions.
- Search for locations by coordinates, city, or region.
- Access information about events, operators, and machine details.
- Submit suggestions or corrections to the database

For more information, check out the [Pinball Map API documentation](https://pinballmap.com/api/v1/docs/1.0.html).


## 🚀 Agent Mode in IDE: Python Pinball Finder App

### Ask about the Pinball Finder API

```plaintext
What is the Public Pinball API and how can I use it? https://pinballmap.com/api/v1/
```

```plaintext
What other data can I pull from this API?
```

### Demo 1: Create a Pinball Finder app from IDE.

#### Prompt using HTML:
```plaintext

### **Prompt:**
```plaintext
Create an HTML file named PinballFinder-Demo.html that:
- Uses Leaflet.js to render a full-screen map.
- Allow the user to input a zip code with a submit button.
- On submission, fetch all locations and their machines for that zip code from the API.
- Finds the nearest pinball machines based on user location.
- Use the Open Pinball Map API to fetch machine data and display it on a map.
```

#### Prompt using Python:
```plaintext
Let's build a project from scratch that will connect to the public Pinball Map API (docs: https://pinballmap.com/api/v1/docs/1.0.html).

Core Requirements
- Language: Python
- Source Control: Use Git. Create a gitignore file. Initialize the project.
- Package Management: Use Poetry. Initialize the project (poetry init) and manage dependencies.
- Project Structure: Create a best practices Python project structure
- Project Architecture: Monolithic but modular design to ensure clear separation of concerns.
- API Client: Implement logic to interact with the Pinball Map API. Start with fetching locations by zip code (likely using the /locations/by_zip_code.json endpoint).
- GUI: Create a simple GUI. Our team uses pyside6.
- First Feature:
  - Allow the user to input a zip code into the GUI.
  - On submission, fetch all locations and their machines for that zip code from the API.
  - Show locations.
    - Determine the top 3 most frequently appearing machine names across all locations found in that zip code. (An API endpoint exists for this.)
    - Combine and display these top 3 machine names, for each location, in the GUI as a sample of what's available in the area.
```


#### Prompt using Python (Enhanced):
```plaintext
Act as a senior Python developer and project architect using Agent Mode. Build a new Python project from scratch that connects to the public Pinball Map API ([docs](https://pinballmap.com/api/v1/docs/1.0.html)).

**Core Requirements:**
- **Language:** Python 3.11+
- **Source Control:** Initialize a Git repository and create a .gitignore file tailored for Python and Poetry.
- **Package Management:** Use Poetry for dependency management (`poetry init`). All dependencies must be managed via Poetry.
- **Project Structure:** Scaffold a best-practices Python project layout (src/ layout, tests/ folder, README.md, etc.).
- **Architecture:** Monolithic but modular, with clear separation of concerns (API client, GUI, business logic, utilities).
- **API Client:** Implement a reusable client for the Pinball Map API. Start with fetching locations by zip code using `/locations/by_zip_code.json`.
- **GUI:** Use PySide6 to build a simple, responsive GUI.
- **First Feature:**
  - User can input a zip code in the GUI.
  - On submission, fetch all locations and their machines for that zip code.
  - Display a list of locations in the GUI.
  - For each location, show the top 3 most frequently appearing machine names in that zip code (use the relevant API endpoint).
  - Display these machine names for each location as a sample of what’s available in the area.

**Agent Mode Instructions:**
- Provide step-by-step guidance and code for each phase: project scaffolding, API integration, GUI setup, and feature implementation.
- Suggest best practices for error handling, modularity, and code readability.
- Recommend and add any useful developer tools (e.g., linters, formatters, pytest).
- Output code snippets and terminal commands as needed, with clear file paths and explanations.
- Ask clarifying questions if any requirements are ambiguous.

**Goal:** Deliver a clean, maintainable, and user-friendly Python application that demonstrates best practices and leverages modern tooling.
```

If you want Copilot Agent Mode to produce:
- ✅ **More polished, thorough solutions**
- ✅ **Proactive best-practice suggestions**
- ✅ **Collaborative Q\&A to nail down unclear areas**

👉🏽 Then use the **Enhanced prompt**.


