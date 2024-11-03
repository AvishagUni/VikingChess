# Viking Chess (Hnefatafl) Game

This project implements the game **Hnefatafl**, a traditional Viking chess variant. The project, developed as part of an **Object-Oriented Programming course**, emphasizes the application of OOP principles, including inheritance, encapsulation, and polymorphism.

---

## 📋 Project Overview

**Hnefatafl** is played on an 11x11 grid with 24 attackers and 13 defenders (including a king). The goal is asymmetric:
- **Defenders** aim to get the king to one of the board's corner squares.
- **Attackers** aim to capture the king before he escapes.

---

## 🧩 Game Rules

1. **Objective**:
   - **Defenders' Goal**: Move the king to a corner square to win.
   - **Attackers' Goal**: Surround and capture the king before he reaches the corner.

2. **Movement**:
   - All pieces move like a rook in chess—any number of empty squares in a straight line (vertically or horizontally).
   - Pieces cannot jump over others or move diagonally.

3. **Capturing**:
   - Capture occurs when an opposing piece is surrounded on both sides by two pieces of the player.
   - The king can be captured if surrounded on all four sides or three sides when at the board's edge.

---

## 🛠 Design and Class Structure

The project uses the following OOP principles and structures:

### Core Classes

1. **ConcretePiece** - Abstract base class implementing the `Piece` interface for all game pieces.
2. **Pawn** - Represents a standard piece, either attacker or defender.
3. **King** - Represents the king piece, with unique capture rules.
4. **Position** - Represents a position on the board.
5. **ConcretePlayer** - Implements the `Player` interface, representing a player as either attacker or defender.
6. **GameLogic** - Implements `PlayableLogic`, handling game rules, piece movement, and win conditions.

### Interfaces

- **Piece**: Defines behaviors for game pieces.
- **Player**: Defines behaviors for players.
- **PlayableLogic**: Outlines game logic functions.

### Key Methods

- `move(Position a, Position b)`: Moves a piece and checks if the move is valid.
- `getPieceAtPosition(Position position)`: Returns the piece at a given board position.
- `isGameFinished()`: Checks if the game has reached a win condition.
- `undoLastMove()`: Reverts the last move for replayability.

---

## 🔄 Additional Features

1. **Undo Feature**: Allows players to step back through moves, useful for replaying previous turns.
2. **Statistics (Bonus)**:
   - Track moves, captures, and distances moved by each piece.
   - Display game summary on game completion.

---

## 🧑‍💻 Usage

### Requirements

- **Java**: Ensure you have Java installed to run the game.

### Running the Game

1. **Compile the Project**: Compile all `.java` files using:
   ```bash
   javac *.java
