# 🏗️ Conway's Game of Life
## 📜 Overview
This project implements a simulation of Conway’s Game of Life, a famous cellular automaton that follows simple rules to model complex behaviors. The simulation is implemented in Python, using a torus-shaped grid (donut shape), meaning that the top and bottom edges, as well as the left and right edges, are connected.

## 🎯 Problem Explanation
Conway’s Game of Life operates on a grid of cells, where each cell can be either alive (1) or dead (0). The state of each cell evolves over time based on the number of alive neighbors.

**Rules of the Game**
1. Underpopulation: Any live cell with fewer than two live neighbors dies.
2. Survival: Any live cell with two or three live neighbors remains alive.
3. Overpopulation: Any live cell with more than three live neighbors dies.
4. Reproduction: Any dead cell with exactly three live neighbors becomes alive.

The board continuously updates based on these rules until either:
- A maximum number of iterations is reached, or
- The board stops changing (reaches a stable state).

## 🛠️ Implementation Details
1. Board Generation:
- The grid is a square NumPy array of size s × s.
- Each cell is randomly initialized with probability p (default p = 0.1, meaning 10% of cells start as alive).
2. State Updates:
- The board updates in iterations, using two matrices: One stores the current state. The other stores the next state to prevent mid-update interference.
3. Simulation Execution:
- Function simulate_gameoflife(s, p, n) runs the simulation for up to n iterations.
- Stops early if the board reaches a steady state (no further changes occur).
- Displays the board at each iteration.

📊 Example Output
Iteration 1:
[0 1 0 0 1]
[1 1 1 0 0]
[0 0 1 1 1]
...

Iteration 10:
[0 0 1 0 0]
[1 0 0 1 1]
[1 1 0 0 0]
...
