Absolutely! Here's the full **`README.md`** content in **Markdown format**, ready to copy and paste directly into your GitHub repository:

````markdown
# Live Poll Battle 🎯

A real-time, interactive polling app where users can create poll battles, share room codes, and let others vote live. Perfect for quick decisions, friendly competitions, or just some fun group opinion battles.

---

## Installation and Running Guide

Follow the steps below to clone and run the application on your local machine:

### 1. Clone the repository

```bash
git clone https://github.com/BhaveshZode/Live-Poll-Battle
cd Live-Poll-Battle
````

### 2. Set up the server

```bash
cd server
npm install
node index.js
```

### 3. Set up the client

Open a new terminal window/tab:

```bash
cd client
npm install
npm start
```

The client will run on [http://localhost:3000](http://localhost:3000) and the server on [http://localhost:5000](http://localhost:5000) (or as configured).

---

## 🔄 How It Works

1. **Create a Poll Battle:**

   * Enter your **name**, a **poll question**, and **two options**.
   * Click **"Create Room"** to generate a session.

2. **Room Code Generation:**

   * A unique **room code** is created.
   * Share this room code with friends to let them join and vote.

3. **Join as a Voter:**

   * Voters enter their **name** and the shared **room code** to join.
   * Once the **first voter** joins, a **60-second timer** starts.

4. **Live Voting:**

   * Voters can vote only **once**.
   * Votes are reflected in **real-time** across all connected clients.

5. **Voting Ends:**

   * After 60 seconds, voting ends automatically.
   * The option with the most votes is declared the **winner**.

---

# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the `client` directory, you can run:

### `npm start`

Runs the app in development mode.
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.
You may also see any lint errors in the console.

### `npm test`

Launches the test runner in interactive watch mode.
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.
It correctly bundles React in production mode and optimizes the build for best performance.

The build is minified and the filenames include the hashes.
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will copy all configuration files and dependencies into your project, giving you full control.

---

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

Other useful links:

* [Code Splitting](https://facebook.github.io/create-react-app/docs/code-splitting)
* [Analyzing Bundle Size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)
* [Making a PWA](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)
* [Advanced Configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

---

```

