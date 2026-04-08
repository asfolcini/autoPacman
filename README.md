# Pac-Man Game

An autonomous Pac-Man simulation with intelligent AI behavior.

## Features

- **Intelligent Pac-Man**: 
  - Actively seeks dots with lookahead (2-step path planning)
  - Avoids ghosts when they're nearby (within 2 cells)
  - Prevents back-and-forth oscillation by avoiding immediate direction reversal
  - 10% chance of random movement to prevent deadlocks

- **Smart Ghosts**:
  - Actively chase Pac-Man using pathfinding
  - Never occupy the same cell as another ghost
  - 10% chance of random movement to prevent deadlocks
  - Prioritize movement toward Pac-Man
  - Cartoon-style ghost sprites instead of simple circles

- **Game Mechanics**:
  - Collision detection: Pac-Man loses a life when touching a ghost
  - "Life Lost" flashing red message for 3 seconds after collision
  - Score tracking and lives system
  - Game reset on death or win

## How It Works

1. Open `index.html` in any modern browser
2. Pac-Man moves autonomously without any player input
3. Watch as he navigates the maze, collects dots, and avoids ghosts
4. When caught by a ghost, "Life Lost" appears in red for 3 seconds
5. After 3 seconds, Pac-Man and ghosts reset to starting positions
6. Game resets completely after all lives are lost (5-second delay)

## Technical Details

- Grid-based movement (20×20 cells)
- Each cell is 15×15 pixels
- Pac-Man and ghosts move on a fixed grid
- Game loop runs at 5 FPS for Pac-Man and 2.5 FPS for ghosts
- No player input required - fully autonomous
- Collision detection uses exact cell position matching
- "Life Lost" message displayed with 3-second pause before reset
- Cartoon-style ghost sprites with directional eyes

## Development

The game is implemented in pure JavaScript with HTML5 Canvas. No external libraries are used.

To run:
1. Open index.html in any modern web browser

## Game State

- Initial position: Pac-Man at (1,1) facing right
- 4 ghosts at positions: (10,8), (9,8), (10,9), (11,8)
- 3 lives to start
- Score starts at 0

All game logic is contained in index.html.