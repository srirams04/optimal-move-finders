# Efficient Game Solvers Using Data Structures and Algorithms

This repository contains a collection of efficient game solvers developed in C and C++ as part of the [Data Structures and Algorithms course](https://bkomarath.rbgo.in/teaching/data-structures-and-algorithms-i-2023/) at IIT Gandhinagar in 2023. These solvers are designed to analyze game states, explore potential moves, and find optimal solutions or strategies for different games.

The games included in this repository are:

-   Connect 4 Solver
-   Cube 2x2x2 Solver
-   8-Puzzle Solver
-   Triangle Game Solver
-   Sudoku Solver

Each solver aims to find the optimal sequence of moves or the shortest solution path to solve the respective game. The implementations leverage data structures such as **queues, stacks, and hash tables** to efficiently store and manage game states, while algorithms like **breadth-first search (BFS), depth-first search (DFS), and minimax** are used to explore the solution space and prune the search tree.


## Connect 4

Connect 4 is a classic two-player game where each player takes turns dropping colored discs into a vertically suspended grid. The objective is to be the first player to form a horizontal, vertical, or diagonal line of four discs of the same color.

- **Representing the Board State:** The board is represented using a 2D character array, where each element represents a cell on the board, with values 'R' for red, 'B' for blue, and '.' for an empty cell.

- **Implementing Game Rules and Validating Moves:**  The `place_move` function checks if a column is full before placing a disc, and the `has_won` function checks for horizontal, vertical, and diagonal lines of four discs of the same color to determine a winner.

- **Developing an Intelligent AI Player:** The `best_move` function implements a minimax algorithm to evaluate the game tree and choose the best move for the AI player.


## Cube 2x2x2 Solver

The Cube 2x2x2 Solver is a program that solves the 2x2x2 Rubik's Cube puzzle. Given an initial configuration of the cube, the program finds the shortest sequence of moves required to solve the puzzle.

- **Representing the Cube State Efficiently:** The cube's state is represented using a 3D character array, where each element represents a cubelet's color. Cube rotation operations (e.g., clockwise, counterclockwise) are implemented using efficient swapping and shifting techniques.

- **Ensuring Cube Validity:** The `is_valid` function checks if the cube's configuration is solvable by verifying the color permutations and orientations of the cubelets.

- **Finding the Shortest Solution:**  The `solve` function implements a breadth-first search (BFS) algorithm, exploring all possible moves and maintaining a hash table to avoid revisiting states. The solution is reconstructed by backtracking from the solved state.

## 8-Puzzle

The 8-Puzzle is a classic sliding puzzle game that consists of a 3x3 grid with eight numbered tiles and one blank space. The objective is to rearrange the tiles from a given initial configuration to the desired goal configuration by sliding the tiles one at a time into the blank space.

- **Representing the Board State:** The board state is represented using a 1D array of size 9, where each element represents a tile, and the value 9 represents the blank space.

- **Implementing Valid Moves:** The `up`, `down`, `left`, and `right` functions check if the blank space is at the respective edge of the board before attempting a move, preventing invalid moves.

- **Finding the Shortest Solution:**  The `solve` function implements a breadth-first search (BFS) algorithm, exploring all valid moves and maintaining a visited array to avoid revisiting states. 


## Triangle Game

The Triangle Game is a two-player game played on a board with six vertices and fifteen edges. Each player takes turns joining two unconnected vertices with an edge of their color. The objective is to be the first player to form a triangle of their color.

- **Representing the Board State:** The board state is represented using a 1D character array of size 15, where each element represents an edge, and the values 'R' and 'B' indicate the player's colors.

- **Implementing Game Rules and Validating Moves:**  The `best_move` function checks if an edge is available before attempting a move, and the `has_won` function checks for triangles of the same color to determine a winner.

- **Developing an Intelligent AI Player:** The `best_move` function implements a minimax algorithm to evaluate the game tree and choose the best move for the AI player.


## Sudoku Solver

The Sudoku Solver is a program that solves Sudoku puzzles by finding a valid arrangement of numbers that satisfies the rules of the game. Sudoku is a brain teaser that challenges you to fill in a 9x9 grid with numbers. Each row, column, and mini-grid (3x3) must contain all the digits 1-9, with no repetition!

- **Representing the Sudoku Board:** The board is represented using a 2D integer array, where each element represents a cell on the board, with 0 representing an empty cell.

- **Validating the Board Configuration:** The `is_valid` function checks if each row, column, and 3x3 sub-grid does not contain duplicate non-zero values, enforcing the Sudoku rules.

- **Implementing an Efficient Solving Algorithm:** The provided code implements a backtracking algorithm to solve Sudoku puzzles by recursively filling empty cells with valid values and backtracking when a solution is not possible.

