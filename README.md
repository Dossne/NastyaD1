# Block Crush MVP

## What kind of game is this?

This project is a **Unity-based block puzzle game** inspired by **Block Crush / Block Blast-style gameplay**.

It is **not** a classic falling-block Tetris game.  
The player does not rotate or drop pieces from the top. Instead, the player places block shapes onto a fixed board, clears full rows and columns, and tries to survive as long as possible.

### Genre
- Casual puzzle game
- Block placement puzzle
- Score-based survival gameplay

### Reference
Main reference:
- **Block Crush**
- **Block Blast-like puzzle gameplay**

Core reference loop:
- a fixed square board;
- several available block pieces;
- drag-and-drop or click-and-place interaction;
- row and column clearing;
- game over when no available piece can be placed.

---

## Controls

The game should work primarily for **mouse input** in the Unity Editor / desktop build, and be easy to adapt for **touch input** later if needed.

### Desktop / Editor
- **Click and drag** a piece
- **Release** it over the board to place it
- If the placement is invalid, the piece returns to its original position
- Press the **Restart** button to begin a new run

### Optional mobile-ready behavior
- **Touch and drag** a piece
- **Release** to place it
- Invalid placement returns the piece back

---

## Core gameplay mechanic

The player is given a set of block pieces and must place them onto a fixed board.

### Main gameplay loop
1. Select one of the available block pieces
2. Drag it onto the board
3. If the placement is valid, lock it into the grid
4. Check whether any full row or full column has been completed
5. Clear all completed rows and columns
6. Award score
7. Continue placing pieces
8. Generate new pieces when the current set is used
9. End the game when no available piece can be placed on the board

### Main rules
- The board is a fixed grid
- Recommended MVP board size: **8x8**
- Pieces do **not** fall from the top
- There is **no gravity**
- Pieces are **not rotated**
- Pieces are **not mirrored**
- Full rows are cleared
- Full columns are cleared
- Multiple lines can be cleared in one move
- The player earns points for successful placement and line clears

### Score logic
At minimum, score should increase for:
- placing a piece;
- clearing rows or columns;
- clearing multiple lines in one move.

Combo logic and best score persistence are optional for the first technical prototype and can be added later.

---

## MVP

The MVP is the **first fully playable Unity prototype**.

It must already include the complete core gameplay loop, even if the visuals are still simple.

### What must already work in the MVP
- Unity project with clean scene setup
- C# gameplay logic
- Visible game board
- Visible available block pieces
- Piece selection and dragging
- Valid placement detection
- Invalid placement rejection
- Piece snapping into the board after successful placement
- Full row clearing
- Full column clearing
- Score tracking
- Automatic generation of the next set of pieces
- Game Over detection when no moves remain
- Restart button
- Basic UI for score and game state
- Stable playable loop from start to game over

### What is acceptable in the MVP
- Simple placeholder visuals
- Simple colored blocks
- Minimal animations or no animations
- Minimal sound or no sound
- Basic UI styling

### What is not required for the MVP
- Advanced VFX
- Heavy visual polish
- Skins
- Boosters
- Level progression
- Narrative
- Meta progression
- Monetization
- Shop
- Online leaderboard
- Save system beyond simple local data, if added later

---

## Done criteria

The task is considered **done** when the Unity MVP is fully playable and stable.

### “Done” means:
- The project opens correctly in Unity
- The main scene runs without critical errors
- The player can place pieces on the board
- Invalid placements are rejected correctly
- Valid placements update the board correctly
- Full rows clear correctly
- Full columns clear correctly
- Score updates correctly
- New pieces appear correctly after the current set is used
- Game Over appears when no moves remain
- Restart works correctly
- The gameplay loop can be played from start to finish without breaking
- The code is split into reasonable C# scripts instead of one giant controller
- The project is understandable and extendable

### Quality expectation
The result should feel like a clean, playable **Unity MVP** of a **Block Crush-style block puzzle game**, with solid core mechanics and a structure that can be expanded later.

---

## Suggested technical structure

A possible project structure for the MVP:

- `GameBoardManager` - manages board state
- `BlockShapeData` - stores block shape definitions
- `PieceSpawner` - generates available pieces
- `PieceDragHandler` - handles dragging and dropping
- `PlacementValidator` - checks whether a piece can be placed
- `LineClearSystem` - detects and clears full rows and columns
- `ScoreManager` - tracks score
- `GameManager` - controls game flow, restart, and game over
- `UIManager` - updates score text, restart button, and game over panel

This does not need to be followed literally, but the logic should remain modular.

---

## Summary

This project is a **Unity C# MVP** of a **Block Crush / block puzzle** game.

Priority order:
1. correct core mechanics;
2. stable gameplay loop;
3. clean project structure;
4. visual polish later.