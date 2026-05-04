# Chess Game ♟️

## What is this?
A basic chess demonstration that sets up a board and provides simple move handling. It’s intended as a learning exercise on representing game state and implementing rules.

## Features
- Board initialization and display.
- Simple move input and basic validation (may be partial).
- Can be extended to include full rules, check/checkmate detection, GUI, or AI.

**Main script:** `Chess Game.py`

### How to run
1. Run: `python "Chess Game.py"`
2. Follow on-screen instructions to enter moves (example notation may vary).

## Summary
This project is ideal for practicing data structures (board representation), rule-based checks and optionally integrating a GUI (Tkinter/Pygame) or implementing a simple AI opponent.
Chess Game User Manual

How to Play:
- Players take turns moving pieces.
- Move format: A2 A4
  (From square → To square)

Rules:
- Pawns move forward only.
- Diagonal move is allowed only when capturing.
- King cannot move into check positions.

Controls:
- Type move to play.
- Type "undo" to undo last move.
- Type "end" to stop game.

Board:
- A to H columns
- 1 to 8 rows
Chess Game Developer Guide

Architecture:
- Board class → manages squares and players
- Piece class → base logic for all pieces
- Player class → stores pieces and captured pieces

Flow:
1. Game starts in startGame()
2. Board is created and populated
3. Players take turns moving pieces
4. move() validates and updates board
5. drawBoard() renders updated state

Rendering:
- Board is stored as dictionary of squares
- Each square contains position and piece
- drawBoard() prints grid in console

Key Logic:
- isSquareValid → validates movement rules
- selfCheck → prevents illegal king moves
- getValidMoves → defines piece movement rules