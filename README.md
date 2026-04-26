## README.md

# Tic-Tac-Toe (JS)

A clean, efficient version of the classic **Tic-Tac-Toe**. This project explores game theory and decision-making trees by implementing an AI opponent that uses the Minimax algorithm to ensure it never loses.

URL - https://tic-tac-j3yyhw2mj-henitj19-8765s-projects.vercel.app/

## 🚀 Features
* **Minimax AI:** A recursive algorithm that evaluates every possible move to play the optimal game.
* **Modular Logic:** Separation of concerns between the game engine (logic), the UI (display), and the AI (decision-making).
* **Win/Draw Detection:** Dynamic checking for three-in-a-row patterns or board saturation.
* **Responsive Grid:** A CSS Grid-based layout that scales across desktop and mobile devices.
* **Score Tracking:** Local session persistence for player and AI win counts.

## 🛠️ Technical Stack
* **JavaScript (ES6):** Core engine and recursive AI logic.
* **HTML5:** Semantic markup for the $3 \times 3$ grid.
* **CSS3:** Modern styling with Flexbox and Grid for layout and centering.

## 🕹️ How to Play
1. **Clone the repository:**
   ```bash
   git clone https://github.com/HenitJain/Tic-Tac-Toe.git
   ```
2. **Launch:**
   * Open `index.html` in your browser.
3. **Gameplay:**
   * Click any empty square to place your marker (**X**).
   * The AI will automatically respond with its move (**O**).
   * Try to get three in a row before the AI blocks you.

## 📂 Project Structure
* `index.html`: The main game board and UI.
* `script.js`: Handlers for user clicks and board resets.
* `minimax.js`: The recursive function that determines the AI's moves.
* `README.md`: Documentation.

## ⚙️ Key Logic: Minimax Algorithm
The AI uses a decision tree to evaluate the "value" of every possible future state. It assigns a score to terminal states:
* **Win:** $+10$
* **Loss:** $-10$
* **Draw:** $0$



The algorithm then works backward: if it is the AI's turn, it chooses the move with the **maximum** score; if it is the player's turn, it assumes the player will choose the move that **minimizes** the AI's score.

$$f(n) = \begin{cases} \text{score}(n) & \text{if } n \text{ is terminal} \\ \max_{s \in \text{successors}} f(s) & \text{if AI turn} \\ \min_{s \in \text{successors}} f(s) & \text{if Player turn} \end{cases}$$
