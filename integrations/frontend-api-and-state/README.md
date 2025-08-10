# Frontend API and State

**Goal**  
Wire the UI to the backend API with a clean data hook, add loading and error UI, and a basic test.

**Time** 10 to 15 minutes

## Prerequisites
- Backend API running locally

## Step 1, Create a data hook
Copy the prompt below into **Copilot Chat**. Paste one block at a time.
```
Create a usePlanes hook that fetches from http://localhost:1903/planes with axios, returns { data, loading, error }, 
and cancels the request on unmount.
```

## Step 2, Apply the hook
Copy the prompt below into **Copilot Chat**. Paste one block at a time.
```
Replace inline fetch logic in PlaneList with usePlanes. Add loading and error UI.
```

## Step 3, Add a test
Copy the prompt below into **Copilot Chat**. Paste one block at a time.
```
Generate a React Testing Library test that renders PlaneList, mocks the hook, and verifies loading state and rendering two planes.
```

## Step 4, Run
```bash
npm test
npm run dev
```
