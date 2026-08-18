# 🎥 Apna Video Call

Apna Video Call is a full-stack web application that allows users to connect with others through **real-time video meetings** directly from their browser.

Users can create or join meetings using a meeting code, communicate through video and audio, share their screen, send messages in real time, and view their previous meeting activity.

## 🤔 The Problem

Traditional video conferencing platforms can be complex for small projects, learning environments, and simple peer-to-peer communication.

This project was built to understand how a video conferencing platform works under the hood using technologies like **WebRTC, Socket.IO, React, Node.js, Express, and MongoDB**.

## ✅ What Apna Video Call Does

1. Users create an account or log in.
2. Users can enter a meeting code to join a video meeting.
3. The application requests access to the camera and microphone.
4. Participants are connected using **WebRTC**.
5. **Socket.IO** handles real-time signaling between participants.
6. Users can:

   * 🎥 Turn their camera on/off
   * 🎙️ Turn their microphone on/off
   * 🖥️ Share their screen
   * 💬 Send real-time chat messages
   * 👥 See other participants in the meeting
7. Meeting codes are saved to the user's meeting history.
8. Users can view their previous meetings from the history page.

## 🎯 Try It

🔗 **Live Demo:** [Add your deployed application link here]

Open the application, create an account, log in, and enter a meeting code to start a video meeting.

> **Note:** Camera and microphone permissions are required for video meetings.

## 🛠️ How It Works (Under the Hood)

```text
User
  ↓
React Frontend
  ↓
Login / Register
  ↓
Node.js + Express Backend
  ↓
MongoDB
  ↓
Join Meeting
  ↓
Socket.IO Signaling
  ↓
WebRTC Peer-to-Peer Connection
  ↓
Audio + Video Communication
  ↓
Real-Time Chat + Screen Sharing
```

### 🔄 WebRTC Flow

When users join the same meeting:

```text
User 1
   ↓
Socket.IO Signaling
   ↓
Exchange SDP + ICE Candidates
   ↓
WebRTC Peer Connection
   ↕
Audio / Video Streams
   ↕
WebRTC Peer Connection
   ↑
Socket.IO Signaling
   ↑
User 2
```

Socket.IO is used for signaling, while WebRTC handles the actual peer-to-peer audio and video communication.

## 📦 Project Files

| **File / Folder**                            | **What it does**                                  |
| -------------------------------------------- | ------------------------------------------------- |
| `frontend/`                                  | React frontend and user interface                 |
| `backend/`                                   | Node.js and Express backend                       |
| `frontend/src/pages/VideoMeet.jsx`           | Main video meeting functionality                  |
| `frontend/src/pages/authentication.jsx`      | Login and registration interface                  |
| `frontend/src/pages/home.jsx`                | Home page for joining meetings                    |
| `frontend/src/pages/history.jsx`             | Displays previous meeting activity                |
| `frontend/src/contexts/AuthContext.jsx`      | Handles authentication state                      |
| `backend/src/app.js`                         | Creates the Express server and connects MongoDB   |
| `backend/src/controllers/socketManager.js`   | Handles Socket.IO connections, signaling and chat |
| `backend/src/controllers/user.controller.js` | Handles registration, login and meeting history   |
| `backend/src/models/user.model.js`           | MongoDB user schema                               |
| `backend/src/models/meeting.model.js`        | MongoDB meeting history schema                    |
| `backend/src/routes/users.routes.js`         | User authentication and activity API routes       |

## ✨ Features

* 🔐 User Registration
* 🔑 User Login
* 🎥 Real-Time Video Calling
* 🎙️ Microphone Control
* 📹 Camera Control
* 🖥️ Screen Sharing
* 💬 Real-Time Chat
* 👥 Multiple Participants
* 🔗 Meeting Code Based Joining
* 📜 Meeting History
* ⚡ Real-Time Communication with Socket.IO
* 🌐 Peer-to-Peer Communication with WebRTC
* 🗄️ MongoDB Database
* 📱 React-Based User Interface

## 🧰 Skills Used to Build This

* **React.js** — frontend user interface
* **Node.js** — backend runtime
* **Express.js** — REST API and server
* **MongoDB + Mongoose** — database and data modeling
* **Socket.IO** — real-time signaling and chat
* **WebRTC** — peer-to-peer audio/video communication
* **Material UI** — UI components and icons
* **Axios** — API communication
* **bcrypt** — password hashing
* **Crypto** — session token generation
* **Git & GitHub** — version control and code hosting

## 🚀 Run It Yourself

### 1. Clone the Repository

```bash
git clone [https://github.com/YOUR_USERNAME/YOUR_REPOSITORY_NAME](https://github.com/sharanyamaisa2706/).git
cd Zoom-main
```

### 2. Start the Backend

```bash
cd backend
npm install
npm start
```

The backend runs on:

```text
http://localhost:8000
```

For development with Nodemon:

```bash
npm run dev
```

### 3. Start the Frontend

Open a new terminal:

```bash
cd frontend
npm install
npm start
```

The React application will normally open at:

```text
http://localhost:3000
```

## 🗄️ Database

The application uses **MongoDB** to store user information and meeting history.

### User Data

The user collection stores:

```text
name
username
password
token
```

Passwords are hashed using `bcrypt` before being stored.

### Meeting Data

The meeting collection stores:

```text
user_id
meetingCode
date
```

This allows users to see their previous meeting activity.


## ⚠️ Security Note

Before making this repository public, **remove any database credentials or secrets from the source code**.

Use environment variables instead:

```env
MONGO_URI=your_mongodb_connection_string
PORT=8000
```

Also make sure `.env` is included in `.gitignore`.

Never upload:

* MongoDB passwords
* API keys
* Secret tokens
* Production credentials

## 🗺️ What's Next

Some possible improvements for future versions:

* 🔗 Generate shareable meeting links
* 🔐 Add stronger authentication using JWT
* 👤 Add user profile management
* 🗓️ Add scheduled meetings
* 🔒 Password-protected meetings
* 🎥 Meeting recording
* ☁️ Cloud storage for recordings
* 🔇 Host controls for participants
* 🛡️ Improved security and authorization
* 📱 Improve mobile responsiveness
* 🔔 Meeting notifications
* 🌍 Add TURN server support for better WebRTC connectivity
