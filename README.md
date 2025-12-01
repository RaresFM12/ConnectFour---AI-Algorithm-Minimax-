# Connect Four – Minimax AI

This project is a Connect Four game implemented in Python, where you can play either against another human or against an AI opponent powered by the Minimax algorithm.  
The focus of the project is on implementing adversarial search and heuristic evaluation to create a competitive computer player.

---

## 🎮 Features

- *Two game modes*
  - Player vs Player
  - Player vs Computer (AI)
- *AI opponent using Minimax*
  - Simulates future moves and counter-moves
  - Evaluates board states using a heuristic scoring function
  - Chooses the move that maximizes its chances to win
- *Valid move handling & win detection*
  - Checks for horizontal, vertical and diagonal connects
  - Handles invalid moves and full columns gracefully
- *Simple, readable codebase*
  - Clear separation between game logic and AI logic
  - Easy to extend with new heuristics or UI

---

## 🧠 Minimax AI – How it works

The AI uses the *Minimax algorithm*, a classic approach for turn-based, zero-sum games:

- Builds a game tree of possible future board states up to a given search depth.
- Alternates between:
  - *Maximizing player* (the AI): tries to maximize the evaluation score.
  - *Minimizing player* (the human): assumed to play optimally and minimize the score.
- Uses a *heuristic evaluation function* to score non-terminal positions:
  - Rewards positions where the AI has potential 2-in-a-row / 3-in-a-row patterns.
  - Penalizes positions where the opponent has strong threats.
- Returns the move with the best expected outcome under optimal play.

---

## 🏗️ Project structure

```text
ConnectFour---AI-Algorithm-Minimax-/
├── src/
│   ├── ... (game logic and AI implementation)
│   └── ... (board representation, Minimax, evaluation)
├── .idea/          # IDE configuration (PyCharm / IntelliJ)
└── README.md       # Project documentation
