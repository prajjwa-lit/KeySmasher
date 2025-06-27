# KeySmasher

KeySmasher is a modern, full-stack, multiplayer typing speed test and racing application. It allows users to practice typing, compete in real-time typing races, track their progress, and view leaderboards. Built with a React + Vite frontend and an Express + MongoDB backend, KeySmasher offers a sleek, responsive UI and robust real-time features powered by Socket.IO.

---

## Table of Contents

- [Features](#features)
- [Tech Stack](#tech-stack)
- [Screenshots](#screenshots)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Running the App](#running-the-app)
- [Project Structure](#project-structure)
- [Usage](#usage)
- [API Overview](#api-overview)
- [Contributing](#contributing)
- [License](#license)

---

## Features

- **Typing Practice:** Solo typing tests with WPM, accuracy, and score calculation.
- **Multiplayer Races:** Join or create rooms to race against friends or random users in real-time.
- **Leaderboard:** Track top performers and your own stats.
- **User Profiles:** View and edit your profile, track your typing history and stats.
- **Customizable Settings:** Adjust test duration, dark mode, and more.
- **Responsive UI:** Works seamlessly on desktop and mobile devices.
- **Real-time Updates:** Powered by Socket.IO for instant race updates.

---

## Tech Stack

**Frontend:**
- React 19 (with Vite)
- TailwindCSS for styling
- React Router for navigation
- React Icons for UI elements

**Backend:**
- Node.js + Express
- MongoDB (via Mongoose)
- Socket.IO for real-time communication
- JWT for authentication
- BcryptJS for password hashing

---

## Screenshots

> _Add screenshots or GIFs here to showcase the UI and features._

---

## Getting Started

### Prerequisites

- Node.js (v18+ recommended)
- npm or yarn
- MongoDB (local or cloud instance)

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/KeySmasher.git
   cd KeySmasher
   ```

2. **Install dependencies for both frontend and backend:**
   ```bash
   cd frontend
   npm install
   cd ../backend
   npm install
   ```

3. **Set up environment variables:**
   - Copy `.env.example` to `.env` in the `backend/` directory and fill in your MongoDB URI and JWT secret.

### Running the App

**Start the backend:**
```bash
cd backend
npm start
```

**Start the frontend:**
```bash
cd frontend
npm run dev
```

- The frontend will typically run on [http://localhost:5173](http://localhost:5173)
- The backend will run on [http://localhost:3000](http://localhost:3000) (or as configured)

---

## Project Structure

```
KeySmasher/
│
├── frontend/         # React + Vite frontend
│   ├── src/
│   │   ├── components/   # UI components (TypingBox, TypingArea, LeaderBoard, etc.)
│   │   ├── pages/        # Main pages (Profile, Settings, RoomPage, etc.)
│   │   ├── context/      # React context for global state
│   │   ├── utils/        # Utility functions (text generation, result calculation)
│   │   └── App.jsx       # Main app entry
│   └── ...               # Config files, public assets, etc.
│
├── backend/          # Express + MongoDB backend
│   ├── controllers/  # Route controllers (user, room, result)
│   ├── models/       # Mongoose models (User, Room, Result)
│   ├── routes/       # API route definitions
│   ├── sockets/      # Socket.IO logic
│   ├── middlewares/  # Express middlewares (auth, error handling)
│   ├── config/       # DB and environment config
│   └── server.js     # Main server entry point
│
└── README.md         # Project documentation
```

---

## Usage

- **Solo Typing Test:** Visit the home page and start typing to test your speed and accuracy.
- **Multiplayer Race:** Create or join a room to compete with others in real-time. The race starts with a countdown and results are shown at the end.
- **Profile & Stats:** View your typing history, stats, and edit your profile.
- **Leaderboard:** See how you rank against other users.

---

## API Overview

The backend exposes RESTful endpoints under `/api/`:

- `POST /api/user/register` - Register a new user
- `POST /api/user/login` - Login and receive JWT
- `GET /api/user/profile` - Get user profile (auth required)
- `POST /api/room/create` - Create a new race room
- `POST /api/room/join` - Join an existing room
- `GET /api/room/:id` - Get room details
- `POST /api/result` - Submit typing result
- `GET /api/result/user/:id` - Get user results

> _See the backend `routes/` and `controllers/` for more details._

---

## Contributing

Contributions are welcome! To contribute:

1. Fork the repository
2. Create a new branch (`git checkout -b feature/your-feature`)
3. Commit your changes
4. Push to your fork and submit a pull request

Please open issues for suggestions or bug reports.

---

## License

This project is licensed under the ISC License.

---

## Acknowledgements

- Inspired by popular typing test platforms like Monkeytype and TypeRacer.
- Built with ❤️ by Prateek Pandey and contributors.
