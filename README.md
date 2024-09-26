# Colosseum Survival: StudentAgent for COMP 424 Final Project

This README outlines the `StudentAgent` class, my contribution to the Colosseum Survival game AI project for COMP 424: Artificial Intelligence. The objective of this project is to create an agent capable of playing Colosseum Survival—a strategic, two-player, grid-based game that focuses on movement, barrier placement, and zone control.

For the full project overview and instructions, refer to the [COMP424 Project GitHub Repository](https://github.com/dmeger/Project-COMP424-2023-Fall) and the [Project Instructions PDF](https://us.edstem.org/api/resources/32098/download/COMP424_Fall2023_FinalProjectInstuctions.pdf).

## Project Context

In Colosseum Survival, players navigate an `M x M` chessboard, placing barriers to divide the board into zones. The game ends when both players are isolated into their own regions. Each agent aims to maximize the number of cells in their zone to secure a win. This agent was developed as part of the final project for COMP 424, adhering to the project's constraints and objectives.

## My Contribution: `StudentAgent`

The `StudentAgent` implements strategic gameplay using search algorithms and heuristics to make decisions on movement and barrier placement. This agent focuses on defensive strategies to maximize its zone area while avoiding entrapment by the adversary.

### Features of `StudentAgent`

1. **Breadth-First Search (BFS) Navigation:** The agent employs BFS to explore the board within a maximum number of allowable steps (`K`). This ensures it selects valid and strategic moves while avoiding barriers and board boundaries.

2. **Heuristic-Based Decision Making:** The agent uses a heuristic function that prioritizes maximizing distance from the opponent, enhancing its chances of survival by avoiding immediate entrapment.

3. **Boundary and Obstacle Checks:** The agent performs boundary and obstacle checks before making moves to ensure all movements remain within the board's valid range and avoid barriers.

### Key Methods

- **`check_boundary(self, pos, board_size):`** Verifies if a position is within the board's boundaries to prevent illegal moves.
- **`bfs_search(self, chess_board, start_pos, max_step):`** Implements BFS to explore potential moves within the maximum step limit (`K`), avoiding obstacles.
- **`heuristic(self, chess_board, new_pos, adv_pos):`** Calculates the optimal direction for placing a barrier based on maximizing the distance from the adversary.
- **`step(self, chess_board, my_pos, adv_pos, max_step):`** Combines BFS navigation and the heuristic function to decide the agent's next move and where to place the barrier.

### Usage

- The `StudentAgent` is designed to be integrated into the Colosseum Survival game environment as defined in the main project repository.
- During the agent's turn, the `step()` method is called to determine its next move and barrier placement direction.

### Constraints and Rules Followed

- **Movement:** The agent can move up to `K` steps in each turn, where `K = ⌊(M + 1) / 2⌋`.
- **Barrier Placement:** At the end of each move, the agent places a barrier in one of the four cardinal directions (up, right, down, left).
- **Turn Timeout:** Adheres to the 2-second limit per move, as specified in the project instructions.
- **Single-Threaded Execution:** The agent runs as a single-threaded process without any external file I/O, meeting the project requirements for the tournament.

## How to Run

1. **Clone the Main Project Repository:** 
   ```bash
   git clone https://github.com/dmeger/Project-COMP424-2023-Fall.git
