# ✈️ GitHub Copilot Agent Mode: Wright Brothers Guided Demos

⏱️ **Estimated Duration: 20 minutes**

---

Welcome to the GitHub Copilot Agent Mode guided demos for the Wright Brothers app! This collection of demos showcases real-world automation across APIs, UIs, and data workflows.

This markdown file walks through a series of GitHub Copilot demos using **Agent Mode only**. Each section builds on the previous one, helping you showcase progressively advanced capabilities in a live demo or hands-on lab.

---

## Demo 1: Plane API Endpoints

### Scenario

We want to enhance an existing `PlanesController.cs` to support more backend operations such as querying by year, updating, and deleting planes.

> **Use Copilot Agent Mode**

**Prompt:**

```
Add new endpoints to PlanesController.cs that allow querying planes by year, updating existing planes, and deleting planes. Make sure to follow existing controller structure.
```

---

## Demo 2: Debugging a Backend Bug

### Scenario

We found a bug in the API where requesting a specific flight by ID returns the wrong result.

> **Use Copilot Agent Mode**

**Prompt:**

```
There's a bug in the FlightsController. When I go to /flights/2, the app returns the wrong flight — it shows the flight with ID 3 instead of 2.

Please investigate and fix the bug so that the correct flight is returned when requesting by ID. Make any updates necessary to resolve this.
```

---

### GitHub Issue Template: Demo Using Copilot Coding Agent on GitHub.com 

When using GitHub Copilot to create issues, you can leverage the following template to report bugs or request enhancements.

**Title:**
```
Bug: Incorrect flight returned from `/flights/:id` endpoint
```

```
**Steps to Reproduce:**

1. Run the backend project locally
2. Navigate to `http://localhost:1903/flights/2`
3. Observe that it incorrectly returns flight with ID `3` instead of `2`

**💡 Expected Behavior:**
It should return the flight with ID `2`

**Request**
Please investigate and fix this bug. Make all necessary code updates so the correct flight is returned when requesting by ID.
```

---

## Demo 3: Code Coverage in the Browser

### Scenario

Let’s generate a visual code coverage report for backend unit tests.

> **Use Copilot Agent Mode**

**Prompt:**

```
Show me code coverage report for my backend project unit tests and display in the browser.
```

---

## Demo 4: Writing Unit Tests for GetById

### Scenario

You already have a method `GetById` in `PlanesController.cs`, but no tests.

> **Use Copilot Agent Mode**

**Prompt:**

```
Generate unit tests for the GetById method in PlanesController.cs, including edge cases. Append the tests to the PlanesControllerTests.cs file using the existing test structure and naming conventions.
```

---

## 📋 Demo 5: Complete Unit Test Coverage

### Scenario

We now want to ensure all methods in `PlanesController` are covered by unit tests.

> **Use Copilot Agent Mode**

**Prompt:**

```
Add all the missing unit tests with edge cases for the PlanesController class and append them to the PlanesControllerTests.cs file.
```

---

## Demo 6: Generate Tests for a New Controller

### Scenario

You now want to build tests for the `FlightsController`, similar to your `PlanesControllerTests`.

> **Use Copilot Agent Mode**

**Prompt:**

```
Create a new test class for the FlightsController.cs based on the style of PlanesControllerTests.cs. Include unit tests for key endpoints with common and edge case scenarios.
```

---

## Demo 7: Code Coverage HTML Enhancements

### Scenario

You’re already using ReportGenerator and want to refresh and beautify the HTML output.

> **Use Copilot Agent Mode**

**Prompt:**

```
Use the existing ReportGenerator tool to recreate the code coverage HTML report. Also, make the HTML coverage report more visually appealing.
```

---

## Demo 8: Improve Home Page Layout

### Getting Started

Before using GitHub Copilot Agent Mode run the frontend and backend projects locally.

### Step 1: Change to the Frontend Folder
```plaintext
cd to wright-brothers-frontend
npm install
npm run frontend
```

### Step 2: Run the Frontend Project
In the terminal, run the following commands:
```
npm run frontendandbackend
```

### Step 3: Open the Frontend in the Browser
Navigate to `http://localhost:5173` in your browser to view the frontend.

### Scenario

You want to enhance the homepage banner readability and switch from a list to a responsive grid layout for planes.

> **Use Copilot Agent Mode**

**Prompt:**

```
I'd like to improve the homepage layout to make it more readable and modern.

Please:
- Update the banner subtitle to be easier to read
- Center the title and subtitle inside the banner
- Change the plane list to a responsive grid layout that works well on all screen sizes
```

---

## Demo 9: Add Plane Button Component

### Scenario

You want to add a consistent button that takes users to the form to add a new plane.

> **Use Copilot Agent Mode**

**Prompt:**

```
Create a new button component and route the button to the "/add-plane" page

Design:
- Create new component named "AddPlaneButton.tsx" in the src/components folder.
- Create a button that is in the same style as #file:PlaneList.tsx
- Button text is "Add Plane"
- Add a plus icon left of the text
- Update the HomePage.tsx file by adding the following:
  - a new import statement near the top of the file to import the AddPlaneButton component.
  - Add the AddPlaneButton component below the Banner component inside the PageContent component.
- Use "@heroicons/react/24/solid" for the plus icon
```

---

## Demo 10: Add Plane Form Modal

### Scenario

Let’s create a full modal form to add a new plane, using the Plane model, proper form validation, and redirection.

> **Use Copilot Agent Mode**

**Prompt:**

```
In AddPlanePage.tsx, build a POST form to http://localhost:1903/planes using the Plane model from Plane.cs.

- Use Formik for form handling
- Use Yup for validation
- Include all fields from Plane.cs (do not skip any)
- Apply Tailwind styling to match PlaneList.tsx
- Each input must have a label and ID
- Redirect to home on success
- The form should be accessible at the route /add-plane
- Make this form modal

API URL: https://bookish-halibut-5r59rvx4j5hpvjp-1903.app.github.dev/planes/
```

---

### GitHub Issue Template: Feature Request — Add Plane Form Modal 

When using GitHub Copilot to create issues, you can leverage the following template to report bugs or request enhancements.


**Title:**
```
Feature: Add modal form for creating a new Plane
```

```
**Steps to Reproduce:**

1. Create a new page at `/add-plane` in `AddPlanePage.tsx`
2. Build a POST form that submits to:
   `https://bookish-halibut-5r59rvx4j5hpvjp-1903.app.github.dev/planes/`
3. Use the existing `Plane` model (from `Plane.cs`)
4. Form should:

   * Use **Formik** for form handling
   * Use **Yup** for validation
   * Include **all fields from Plane.cs** (don’t skip any)
   * Use **Tailwind CSS** for styling to match `PlaneList.tsx`
   * Include proper labels and IDs
   * Redirect to home page on success
   * Be accessible at `/add-plane`
   * Appear as a **modal**, not a full page

**Copilot Task:**
Please build the full modal form based on the specs above.
```

---

## Demo 11: View / Edit / Delete Planes

### Scenario

You want users to be able to view, edit, and delete plane details in a modal-based UI.

> **Use Copilot Agent Mode**

**Prompt:**

```
Add a new feature to the frontend application that allows users to view details, edit details, and delete a plane from the application using a modal form.
```

---

## Demo 12: Build and Test Pipeline Automation

### Scenario

Time to automate everything! Let’s create a GitHub Actions workflow to build and test both the backend and frontend.

> **Use Copilot Agent Mode**

**Prompt:**

```
Create a single GitHub Actions build pipeline that builds both the backend and frontend applications. Use the appropriate framework for each project. Create pipelines in the .github/workflows folder.

Backend Steps:
- Install dependencies
- Run unit tests
- Collect code coverage and upload as an artifact
- Build the backend project

Frontend Steps:
- Install dependencies
- Install Playwright and its dependencies
- Run linter for code quality
- Run Playwright tests
- Build frontend for production
```

### GitHub Issue Template: Feature Request — Build and Test Pipeline Automation

When using GitHub Copilot to create issues, you can leverage the following template to report bugs or request enhancements.

**Title:**
```
Feature: Create GitHub Actions CI/CD pipeline for backend and frontend
```

```
**Steps to Reproduce:**

1. Backend and frontend projects exist in the same repo.
2. The backend is a typical .NET project with unit tests.
3. The frontend uses a modern JavaScript stack with Playwright tests.

**Expected Behavior:**
A GitHub Actions workflow file should be created in `.github/workflows/` that:

* Runs on every `push` and `pull_request`
* Builds and tests both backend and frontend

**Pipeline Requirements:**

**Backend Steps:**

* Install dependencies
* Run unit tests
* Collect code coverage
* Upload coverage as an artifact
* Build backend app

**Frontend Steps:**

* Install dependencies
* Install Playwright and dependencies
* Run linter
* Run Playwright tests
* Build frontend for production

**Copilot Task:**
Generate a single GitHub Actions YAML file that automates the steps above for both backend and frontend builds and tests.
```

