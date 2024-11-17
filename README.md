
# Tic Tac Toe Game README

## Overview
This Python script implements a console-based **Tic Tac Toe** game. The game supports single matches or "best of N" series between two players, where one chooses **X** and the other chooses **O**. Players take turns to mark positions on the board, and the game announces the winner after every match.

---

## How It Works

1. **Game Board Layout**:
   The board is represented as follows:
   ```
    1 | 2 | 3
   -----------
    4 | 5 | 6
   -----------
    7 | 8 | 9
   ```
   Players choose positions by inputting the corresponding number.

2. **Player Selection**:
   Players can choose between **X** or **O**. The game alternates turns automatically.

3. **Game Modes**:
   - **Single Match**: Play a single round.
   - **Best of N**: Play a series of games. N must be an odd number.

4. **Winning Conditions**:
   A player wins by marking three consecutive positions either horizontally, vertically, or diagonally. The game announces the winner after every match.

5. **Tie Handling**:
   If no player wins and all positions are filled, the game declares a draw.

6. **Scoring**:
   The game tracks the number of wins for each player during the series.

7. **Play Again**:
   After a series ends, players can choose to start a new series or exit the game.

---

## Features

- **Dynamic Board Display**:
  The board updates in real-time after each turn.
  
- **Input Validation**:
  Ensures that players:
  - Choose valid positions.
  - Enter correct game modes (e.g., odd numbers for "Best of N").

- **Automatic Turn Switching**:
  Alternates turns between players.

- **Score Tracking**:
  Maintains and displays scores for each player.

- **Replay Option**:
  Players can start a new series without restarting the script.

---

## Usage Instructions

1. **Run the Script**:
   Execute the script using Python:
   ```bash
   python tictactoe.py
   ```

2. **Choose the Game Mode**:
   - Input `1` for a single match.
   - Input an odd number (e.g., `3`, `5`, etc.) for a "Best of N" series.

3. **Pick Your Marker**:
   - Enter `X` or `O` to choose your symbol.

4. **Make Your Moves**:
   - Input numbers `1-9` to mark your positions on the board.

5. **View Results**:
   - The game announces the winner or a draw after every match.

6. **Replay or Exit**:
   - Input `Y` to play another series.
   - Input `N` to exit the game.

---

## Example Gameplay

### Start:
```
Index Sample of TicTacToe
 1 | 2 | 3 
-----------
 4 | 5 | 6 
-----------
 7 | 8 | 9 
Enter the number of game you would like to play: 3
Best of 3
Enter X to choose X and O to choose O: X
```

### Turn-by-Turn Updates:
```
Choose your position b/w 1-9: 1
 X |   |   
-----------
   |   |   
-----------
   |   |   

Choose your position b/w 1-9: 5
 X |   |   
-----------
   | O |   
-----------
   |   |   

...
```

### Game End:
```
Player X wins
{'player_x': 1, 'player_o': 0}
2 games left
```

---

## Code Overview

### Main Functions

1. **`insert_str(string, index, mark)`**:
   Updates the board string by inserting the player's marker (`X` or `O`) at the specified index.

2. **`choose_position()`**:
   - Main function for managing the game flow:
     - Displays the board.
     - Validates inputs.
     - Tracks turns, positions, and scores.
     - Detects win, draw, or loss conditions.
     - Manages replay logic.

---

## Notes

- **Input Handling**:
  - Only integer inputs are allowed for position and game mode selection.
  - Invalid inputs prompt re-entry.

- **Limitations**:
  - The game does not handle AI or automated opponent behavior.
  - It's strictly two-player (manual turn-by-turn).

---

Enjoy playing! 😊
