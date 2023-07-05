# Sudoku-Solver
The given Java code is a Sudoku solver that uses a backtracking algorithm to find a valid solution for a given Sudoku puzzle. Sudoku is a number puzzle where you need to fill a 9x9 grid with digits from 1 to 9, subject to certain constraints:

1. Each row must contain all digits from 1 to 9 without repetition.
2. Each column must contain all digits from 1 to 9 without repetition.
3. Each of the nine 3x3 subgrids (also known as boxes) must contain all digits from 1 to 9 without repetition.

The code defines a class named `Solution`, which contains three main methods:

1. `isSafe`: This method checks if it is safe to place a number `number` at a specific position (`row`, `col`) on the Sudoku board, i.e., if the number satisfies the Sudoku constraints for that particular row, column, and 3x3 subgrid.

2. `helper`: This is the backtracking method that tries to solve the Sudoku puzzle. It iterates through each cell of the board. If a cell is empty (denoted by '.'), it tries placing digits from 1 to 9 at that position, checks if the placement is valid using `isSafe`, and recursively calls itself for the next cell. If a valid solution is found, it returns `true`; otherwise, it backtracks by undoing the last placement and continues exploring other possibilities.

3. `solveSudoku`: This is the main method that initiates the solving process. It calls the `helper` method to solve the Sudoku puzzle.

The code includes a `main` method where a 9x9 Sudoku puzzle is defined as a 2D array of characters. The empty cells are represented by '.'. The solver is called to find a valid solution for the puzzle, and the solution is then printed to the console.

To solve the Sudoku puzzle, the solver explores different possible combinations of numbers using a depth-first search approach, and it backtracks whenever a placement leads to an invalid configuration. The algorithm continues to explore different combinations until a valid solution is found or until all possibilities have been exhausted.

When you run the code, it will print the solved Sudoku board to the console. If there is a valid solution, the 2D array will contain digits from 1 to 9, satisfying all the constraints. If there is no valid solution for the given puzzle, the board will remain unchanged, indicating that the Sudoku puzzle is unsolvable.

Overall, this Sudoku solver effectively demonstrates the power of backtracking algorithms in solving constraint satisfaction problems like Sudoku.![sudoku](https://github.com/kritika-das/Sudoku-Solver/assets/94691076/576eb415-e18a-4ecd-9451-fb700a5df9b9)
