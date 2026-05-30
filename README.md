# ChessMaster — Real-Time Multiplayer Chess

A full-stack chess application with real-time multiplayer, AI opponents, friend invitations, and a professional dark-themed UI. Built with React, TypeScript, Node.js, and Socket.io.

🎮 **[Play Now](https://chess-frontend-navy.vercel.app)** · **[View Source](https://github.com/anisoni12/Multiplayer-chess-game)**

---

## Overview

ChessMaster brings together everything you'd expect from a modern chess platform — play against friends via shareable room links, challenge an AI at three difficulty levels, or jump into a live game against a random opponent. No setup required; guest mode gets you playing in seconds.

---

## Features

### Game Modes
- **Play Online** — Real-time matchmaking against other players
- **Play Computer** — Single-player AI with Easy, Hard, and Advanced difficulty
- **Play with Friend** — Generate a unique room link and share it; game starts when both players connect
- **Guest Mode** — Instant play with no registration

### Gameplay
- Move validation powered by Chess.js
- Check, checkmate, and draw detection
- Blitz (3 min), Rapid (10 min), and Classical (15 min) time controls
- Turn-based countdown timer — only the active player's clock runs
- Move history and captured pieces display
- Draw offers and resignation
- Sound effects for moves and game events

### User Experience
- Professional dark theme
- Persistent sidebar navigation (chess.com style) with active page indicators
- Game result banners with victory and defeat animations
- Toast notifications and connection status indicators
- Automatic WebSocket reconnection with exponential backoff
- Timeout warnings at 30 seconds remaining
- Responsive design across desktop, tablet, and mobile

### Authentication
- Email and password login with session persistence
- Guest mode with auto-assigned username (Guest1234)
- Secure logout and user profile display across all game modes

---

## Tech Stack

| Layer | Technologies |
|---|---|
| Frontend | React 19, TypeScript, Tailwind CSS, React Router |
| Game Logic | Chess.js |
| Real-time | Socket.io Client |
| Backend | Node.js, Express.js, Socket.io |
| Deployment | Vercel (frontend), Render (backend) |

---

## Project Structure

```
multiplayer-chess-game/
├── frontend/
│   ├── public/
│   │   └── sounds/            # Move and game event audio
│   └── src/
│       ├── assets/            # Images and static files
│       ├── components/        # ChessBoard, Sidebar, Toast, ErrorBoundary, etc.
│       ├── contexts/          # AuthContext
│       ├── hooks/             # useSocket, useChessSound, useGameLogic
│       ├── screens/           # Landing, Game, ComputerGame, PlayWithFriend, Login, Signup
│       └── utils/             # computerAI.ts
└── backend1/
    └── src/                   # Socket.io game state management
```

---

## Getting Started

**Frontend**
```bash
cd frontend
npm install
npm run dev
```

**Backend**
```bash
cd backend
npm install
npm start
```

Frontend runs on `http://localhost:5173`, backend on `http://localhost:3000`.

---

## How to Play

**Online** — Log in or continue as guest, pick a time control, and wait for an opponent.

**vs Computer** — Choose a difficulty level and play against the AI immediately.

**with Friend** — Click "Play with Friend", copy the generated link, and share it. The game begins as soon as your friend joins.

**Guest** — Hit "Play as Guest" on the login screen for instant access to all modes.

---

## AI Difficulty

| Level | Behavior |
|---|---|
| Easy | Random legal moves with basic piece protection |
| Hard | Board evaluation, 2–3 move lookahead, captures undefended pieces |
| Advanced | Strategic placement, king safety, optimal coordination, 3–4 move lookahead |

---

## Deployment

| Service | URL |
|---|---|
| Frontend | https://chess-frontend-navy.vercel.app |
| Backend | https://chess-backend-0mm0.onrender.com |
| WebSocket | wss://chess-backend-0mm0.onrender.com |

---

## Roadmap

- [ ] Elo rating system and leaderboards
- [ ] Game history and replay viewer
- [ ] In-game chat
- [ ] Tournament mode
- [ ] Opening book integration
- [ ] Mobile app (React Native)

---

## License

MIT — free to use, modify, and distribute.

---

*Built by [Anish Soni](https://github.com/anisoni12)*
