# **Connect 4 AI Game with Minimax Algorithm**
A Python-based implementation of the classic Connect 4 game with an intelligent AI opponent using the Minimax algorithm with alpha-beta pruning.

## **Features**
1. **Player vs AI Gameplay**: 
   - Human player (Player 1) uses red pieces.
   - AI opponent (Player 2) uses yellow pieces.

2. **Game Logic**:
   - Players alternate turns.
   - Valid moves are restricted to open columns.
   - The game ends when a player connects four pieces horizontally, vertically, or diagonally.

3. **AI Strategy**:
   - The AI uses the Minimax algorithm with alpha-beta pruning for optimized decision-making.
   - AI evaluates the board using a scoring function that prioritizes forming and blocking connections.

4. **Graphics**:
   - Built with **Pygame** to create an interactive and visually appealing user interface.
   - Dynamic visuals showing player moves and game state updates.

5. **Endgame Detection**:
   - Detects winning moves and draws.

---

## **Files**
- `connect4.py`: Main Python file containing all logic and the Pygame visualization.
- Dependencies: `numpy`, `pygame`, and `math`.

---

## **How It Works**
1. **Game Initialization**:
   - The board is represented as a 2D NumPy array initialized with zeros.
   - Player pieces are marked as `1` and AI pieces as `2`.

2. **Gameplay Loop**:
   - The player makes moves by clicking on the desired column.
   - The AI calculates its move using the **Minimax algorithm** to maximize its winning chances while minimizing the player’s advantage.

3. **Winning and Scoring**:
   - The game ends if a player connects four pieces.
   - Scores are calculated for AI moves to find the best column.

4. **Graphics**:
   - The Pygame interface updates dynamically to reflect player moves and shows messages when the game ends.

---

## **Key Code Highlights**
1. **Minimax with Alpha-Beta Pruning**:
   - AI decision-making optimized for performance.
   - Code snippet:
     ```python
     def minimax(board, depth, alpha, beta, maximizingPlayer):
         ...
         if maximizingPlayer:
             value = -math.inf
             for col in valid_locations:
                 ...
                 if value > beta:
                     break
             return column, value
         else:
             ...
     ```

2. **Board Evaluation**:
   - Scoring function to assess potential moves:
     ```python
     def evaluate_window(window, piece):
         score = 0
         if window.count(piece) == 4:
             score += 100
         elif window.count(piece) == 3:
             score += 5
         ...
         return score
     ```

3. **Graphics with Pygame**:
   - Drawing the board and pieces dynamically:
     ```python
     def draw_board(board):
         for c in range(COLUMN_COUNT):
             for r in range(ROW_COUNT):
                 pygame.draw.rect(screen, BLUE, ...)
                 pygame.draw.circle(screen, BLACK, ...)
                 ...
     ```

---

## **Requirements**
1. Python 3.6+
2. Required libraries:
   - `numpy`
   - `pygame`

Install dependencies:
```bash
pip install numpy pygame
```

---

## **How to Run**
1. Clone the repository:
   ```bash
   git clone https://github.com/username/connect4-ai.git
   ```
2. Navigate to the project folder:
   ```bash
   cd connect4-ai
   ```
3. Run the game:
   ```bash
   python connect4.py
   ```

---

## **Known Issues**
1. The AI's performance depends on the search depth; higher depths can slow gameplay.
2. Pygame window might not handle resize events effectively.

---

## **Future Improvements**
1. Enhance the AI with reinforcement learning or Monte Carlo Tree Search.
2. Add multiplayer support over a network.
3. Optimize graphics for mobile platforms.

---

## Contact
If you have any questions or need further assistance, please feel free to contact:

- **Name**: Sarowar Alam
- **Email**: sarowaralam40@gmail.com
- **GitHub**: [https://github.com/SarowarAlam](https://github.com/SarowarAlam)


