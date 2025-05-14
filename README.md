# 🗳️ Live Poll Battle

A real-time web application where users can create or join a poll room and vote live. The results are updated instantly across all users in the room using WebSockets. Designed to test full-stack fundamentals and real-time communication.

---

## 📌 Objective

Build a simple poll application that enables users to:

- Create or join a poll room.
- Vote live between two options.
- See votes update in real-time.
- Automatically end polling after 60 seconds.

---

## 🚀 Tech Stack

- **Frontend**: ReactJS
- **Backend**: Node.js, Express, Socket.IO (WebSockets)

---

## 🛠️ Features Implemented

### ✅ Frontend (ReactJS)

- 🔹 Allows user to enter their **name** (unique, no password required).
- 🔹 User can:
  - **Create a new poll room** with a question and two options.
  - **Join an existing poll room** using a unique room code.
- 🔹 Displays the poll question and two voting options.
- 🔹 One vote per user — prevents re-voting.
- 🔹 **Live vote count** updates for all users using WebSockets.
- 🔹 **60-second countdown timer** starts when the first voter joins.
- 🔹 Voting is automatically disabled when the timer ends.
- 🔹 **LocalStorage** is used to persist user vote across refreshes.

### ✅ Backend (Node.js + WebSockets)

- 🔹 Handles **poll room creation and storage** (in-memory).
- 🔹 Accepts and broadcasts votes using **Socket.IO**.
- 🔹 Maintains poll state (votes, participants, timer) in memory.
- 🔹 Supports **multiple independent poll rooms** simultaneously.
- 🔹 Automatically synchronizes vote state and timer with all connected clients.

---

### Vote State Sharing and Room Management

The application manages vote state and room participation using an in-memory approach on the backend (`server/index.js`). When a user creates a room, a unique 6-character `roomId` is generated and stored in the `rooms` object along with the question, options, connected users, current votes, a voting timer, and a flag for voted users (tracked using a `Set`). When a user joins a room, their WebSocket connection is associated with the corresponding room, and the server starts a countdown timer (60 seconds) if it hasn't already started.

Each vote is sent over WebSocket and handled by updating the room's vote count and broadcasting the new vote tallies to all connected clients in real-time. Users are prevented from voting more than once through the `voted` set and client-side local storage (ensuring persistence across page refreshes). Once the timer reaches zero, the server broadcasts a `VOTING_ENDED` event to disable further voting in the room. This approach ensures all users in the same room receive synchronized, real-time updates without requiring a database or external state management.

---

## 📦 Installation & Setup

Follow these steps to run the application locally:

### 1. Clone the Repository

```bash
git clone https://github.com/BhaveshZode/Live-Poll-Battle
cd Live-Poll-Battle
````

### 2. Start the Server

```bash
cd server
npm install
node index.js
```

### 3. Start the Client

Open a new terminal tab/window:

```bash
cd client
npm install
npm start
```

* Client will run at: [http://localhost:3000](http://localhost:3000)
* Server will run at: [http://localhost:5000](http://localhost:5000)

---

## 👨‍💻 Author

**Bhavesh Zode**
GitHub: [https://github.com/BhaveshZode](https://github.com/BhaveshZode)

---

## 📃 License

This project is for educational purposes and not currently licensed.

---

```



