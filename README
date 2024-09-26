# Game AI: Student Agent

This README provides an overview of the `StudentAgent` class, which is part of a larger game project. The `StudentAgent` represents an AI agent designed to make strategic decisions in a game environment. This script showcases a basic implementation of AI behavior using search algorithms and heuristics to navigate the game board and avoid adversaries.

## Overview of `StudentAgent`

The `StudentAgent` is a custom AI that employs a breadth-first search (BFS) algorithm to navigate the game board. The agent is designed to make decisions based on the current state of the board, its position, and the adversary's position. It uses simple heuristics to select its next move and place barriers on the board to block adversaries.

### Key Features

- **Breadth-First Search (BFS) Navigation:** The agent uses BFS to explore potential moves on the game board. It identifies the next optimal move within the allowed number of steps, considering the board's boundaries and obstacles.
- **Heuristic-Based Decision Making:** The agent incorporates a heuristic function that evaluates possible moves to maximize its distance from the adversary, promoting defensive gameplay.
- **Boundary and Obstacle Checks:** The agent checks the game board's boundaries and obstacles to ensure valid movements.

## How It Works

1. **Initialization:** The agent is registered and initialized with a set of possible moves (up, right, down, left).

2. **Boundary Checking:** Before making a move, the agent checks whether a position is within the boundaries of the board and not obstructed by a wall.

3. **BFS Search:** During its turn, the agent uses BFS to explore the board within a specified number of steps to find the next potential move. It ensures the chosen move is not blocked by obstacles.

4. **Heuristic Evaluation:** The agent uses a heuristic function to select the move that maximizes its distance from the adversary, choosing the safest path available.

5. **Making a Move:** The `step` method combines the BFS search and heuristic evaluation to determine the next position and the direction to place a barrier, preventing adversary advancement.

## Code Breakdown

- **`check_boundary(self, pos, board_size):`** Checks if a given position is within the game board's boundaries.
- **`bfs_search(self, chess_board, start_pos, max_step):`** Implements a BFS algorithm to find the next optimal move within a specified number of steps.
- **`heuristic(self, chess_board, new_pos, adv_pos):`** Evaluates potential moves and selects the direction that maximizes the distance from the adversary.
- **`step(self, chess_board, my_pos, adv_pos, max_step):`** Combines the BFS search and heuristic to decide the agent's next move and the direction to place a barrier.

## Usage

- **Game Integration:** This agent can be integrated into the game's environment to act as an AI player. It uses the game board's current state to make strategic movements and place barriers.
- **Customizable Parameters:** The agent's behavior can be adjusted by modifying the BFS depth (`max_step`) and the heuristic function to enhance its decision-making strategy.

## Future Improvements

- Enhance the heuristic function to consider more complex game strategies.
- Implement additional search algorithms (e.g., A* search) for more efficient pathfinding.
- Introduce a learning component to adapt the agent's strategy based on gameplay experience.

## Dependencies

- Python (3.x)
- NumPy (for vector calculations)

## Contributing

This file (`student_agent.py`) represents a part of the game AI. Contributions are welcome to further improve the agent's strategy and performance.

## License

This project is licensed under the MIT License.
