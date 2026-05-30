# ChessMaster - Real-Time Multiplayer Chess Game

🎮 **[Play Live Demo](https://chess-frontend-navy.vercel.app)** | 📂 **[View Code](https://github.com/anisoni12/Multiplayer-chess-game)**

A full-stack real-time chess application with multiple game modes, AI opponent, authentication, and friend invitations. Built with React, TypeScript, Node.js, and Socket.io.

## 🚀 Live Deployment
- **Frontend:** [https://chess-frontend-navy.vercel.app](https://chess-frontend-navy.vercel.app)
- **Backend:** [Render](https://chess-backend-0mm0.onrender.com)
- **WebSocket:** wss://chess-backend-0mm0.onrender.com

## ✨ Features

### Game Modes
- ♟️ **Play Online** - Real-time multiplayer with other players
- 🤖 **Play Computer** - Single-player against AI with 3 difficulty levels (Easy, Hard, Advanced)
- 👫 **Play with Friend** - Invite friends via unique room IDs and shared links
- 👤 **Guest Mode** - Play without registration

### Core Features
- ✅ Real-time multiplayer gameplay with WebSocket synchronization
- ✅ Move validation with Chess.js library
- ✅ Advanced AI opponent with strategic gameplay
- ✅ Multiple time controls (Blitz 3min, Rapid 10min, Classical 15min)
- ✅ Live timer with turn-based countdown (only current player's time decreases)
- ✅ Move history and captured pieces display
- ✅ Game result banners with victory/defeat animations
- ✅ Check and checkmate detection
- ✅ Draw offers and game resignation

### User Experience
- ✅ Professional dark theme UI
- ✅ Persistent left sidebar navigation (chess.com style)
- ✅ Active page indicators in sidebar
- ✅ Responsive design for all devices
- ✅ Sound effects for moves and game events
- ✅ Smooth animations and transitions

### Authentication & User Management
- ✅ Full authentication system (Login/Signup)
- ✅ User profile with email and username
- ✅ Guest mode for instant play
- ✅ Session persistence with localStorage
- ✅ Secure logout functionality
- ✅ User display in all game modes

### Game Features
- ✅ Real-time opponent info display
- ✅ Captured pieces visualization
- ✅ Move history tracking
- ✅ Game statistics (difficulty, moves, pieces)
- ✅ Professional game over modals
- ✅ Play again and back to home options

### Error Handling & Reliability
- ✅ Automatic WebSocket reconnection with exponential backoff
- ✅ Error boundaries for graceful error recovery
- ✅ User-friendly error messages and feedback
- ✅ Toast notifications for important events
- ✅ Connection status indicators
- ✅ Timeout warnings (30 seconds remaining)
- ✅ Invalid move feedback

### Performance Optimization
- ✅ Component memoization to reduce re-renders
- ✅ Shared game logic hook (useGameLogic) to eliminate code duplication
- ✅ Optimized socket message handling
- ✅ Efficient state management

## 🛠 Tech Stack

**Frontend:**
- React 19 with TypeScript
- React Router for navigation
- Socket.io Client for real-time communication
- Chess.js for chess logic and validation
- Tailwind CSS for styling
- Custom hooks for socket management and game logic

**Backend:**
- Node.js with Express.js
- Socket.io for WebSocket communication
- Real-time game state management

## 📁 Project Structure
```
multiplayer-chess-game/
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   │   ├── Sidebar.tsx (memoized)
│   │   │   ├── ChessBoard.tsx
│   │   │   ├── ComputerChessBoard.tsx
│   │   │   ├── GameResultBanner.tsx
│   │   │   ├── GameModeModal.tsx
│   │   │   ├── AnimatedChessBoard.tsx
│   │   │   ├── ErrorBoundary.tsx (NEW)
│   │   │   └── Toast.tsx (NEW)
│   │   ├── contexts/
│   │   │   └── AuthContext.tsx
│   │   ├── screens/
│   │   │   ├── Landing.tsx
│   │   │   ├── Game.tsx (Online mode)
│   │   │   ├── ComputerGame.tsx
│   │   │   ├── PlayWithFriend.tsx
│   │   │   ├── Login.tsx
│   │   │   └── Signup.tsx
│   │   ├── hooks/
│   │   │   ├── useSocket.tsx (with reconnection logic)
│   │   │   ├── useChessSound.tsx
│   │   │   └── useGameLogic.ts (NEW - shared game logic)
│   │   ├── utils/
│   │   │   └── computerAI.ts
│   │   └── App.tsx
│   └── package.json
└── backend/
    ├── server.js
    └── package.json
```

## 🚀 Setup Instructions

### Frontend
```bash
cd frontend
npm install
npm run dev
```

### Backend
```bash
cd backend
npm install
npm start
```

## 🎮 How to Play

### Online Mode
1. Click "Play" on landing page
2. Log in or sign up (or play as guest)
3. Select time control (Blitz, Rapid, or Classical)
4. Wait for opponent to join
5. Play chess in real-time!

### Computer Mode
1. Click "Play Computer" on landing page
2. Select difficulty (Easy, Hard, or Advanced)
3. Play against AI opponent
4. AI makes strategic moves based on difficulty

### Play with Friend
1. Click "Play with Friend" on landing page
2. Copy the game link
3. Share with friend
4. Friend opens link and joins automatically
5. Game starts when both players are connected

### Guest Mode
1. On login screen, click "Play as Guest"
2. Instantly logged in as Guest{number}
3. Access all game modes
4. No registration required!

## 🎯 Game Controls
- **Click piece** - Select a piece to move
- **Click highlighted square** - Move selected piece
- **Resign** - Forfeit the game
- **Offer Draw** - Propose a draw (online mode)
- **Play Again** - Start new game after game over
- **Go Back** - Return to home page

## 🤖 AI Difficulty Levels

### Easy
- Random legal moves
- Basic piece protection
- Simple tactics

### Hard
- Evaluates board position
- Protects valuable pieces
- Looks ahead 2-3 moves
- Captures undefended pieces

### Advanced
- Advanced position evaluation
- Strategic piece placement
- 3-4 move lookahead
- Considers king safety
- Optimal piece coordination

## 🔐 Authentication

### Login
- Email and password authentication
- Session persistence
- Demo mode for testing

### Sign Up
- Username (min 3 characters)
- Email validation
- Password (min 6 characters)
- Automatic account creation

### Guest Mode
- No registration needed
- Random username (Guest1234)
- Full access to all features
- Session saved in localStorage

## 📊 Game Statistics
- Total moves count
- Difficulty level (computer mode)
- Piece count tracking
- Game result and reason
- Time remaining display

## 🎨 UI Features
- Dark professional theme
- Responsive sidebar navigation
- Active page highlighting
- User profile display
- Game result animations
- Smooth transitions and effects
- Professional modals and dialogs

## 🔄 Real-Time Features
- Live opponent info updates
- Instant move synchronization
- Real-time timer countdown
- Live game state management
- Automatic reconnection handling

## 📱 Responsive Design
- Desktop optimized
- Tablet compatible
- Mobile friendly
- Adaptive layouts
- Touch-friendly controls

## 🚀 Future Enhancements
- Game history and replays
- Chess ratings and leaderboards
- Tournament mode
- Chat during games
- Player statistics
- Elo rating system
- Opening book integration
- Endgame tablebase
- Mobile app (React Native)
- Social features

## 📝 License
MIT

---

## 🔗 GitHub Repository
```
https://github.com/anisoni12/multiplayer-chess-game
```

**Use this link in your resume!**

---

## 📧 Contact & Support
For issues, feature requests, or contributions, please open an issue on GitHub.

---

## 🙏 Acknowledgments
- Chess.js for chess logic
- Socket.io for real-time communication
- React and TypeScript communities
- Tailwind CSS for styling
