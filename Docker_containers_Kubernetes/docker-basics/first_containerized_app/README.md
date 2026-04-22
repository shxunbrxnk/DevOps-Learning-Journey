## Simple Dockerized Node.js App

This project is a simple Node.js application that I containerized using Docker as part of my DevOps learning journey.

---

## What this app does

This is a basic web application built with Express.

- Displays a course goal in the browser
- Allows the user to update the goal via a form
- Stores the goal temporarily in memory

When you open the app in your browser, you will see:
- A heading showing the current goal
- A form where you can enter a new goal

---

## How the code works

The application uses:

- Express → to create the web server  
- Body-parser → to handle form data  

### Key functionality:

- A default goal is set:
  ```js
  let userGoal = 'Learn Docker!';
