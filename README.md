# Algorithm-ing Sudoku

This project leverages a backtracking algorithm, to generate and solve Sudoku puzzles. This algorithm is a recursive technique, allowing us to efficiently create unique and valid Sudoku grids based on a given difficulty level, and to robustly find solutions for a wide range of puzzles. The codebase is modular, separating the logic for generation, solving, and grid manipulation for clarity and ease of maintenance.

## Usage

To try it out, clone the repository and run the respective scripts:

```bash
git clone https://github.com/SepehrAkbari/sudokuer.git
cd sudokuer
python src/generate.py
python src/solve.py
```

You can also add custom grids by modifying the [grid](src/grid.py) file.

## Approach

Both the Sudoku generation and solving processes are built upon a recursive backtracking algorithm. This method systematically explores potential solutions by attempting to place a valid number in an empty cell. A number's validity is strictly determined by adherence to Sudoku's fundamental constraints: uniqueness within its row, column, and the encompassing 3x3 subgrid. If a placement is valid, the algorithm recursively proceeds to the next empty cell. Should a conflict arise where no valid number can be placed in a cell, the algorithm "backtracks"—reverting the last decision and exploring an alternative path. This systematic try-and-revert mechanism, combined with strategic number selection (e.g., random shuffling for generation to ensure puzzle variety), efficiently navigates the solution space. For puzzle generation, this process first creates a fully solved grid, and then selectively removes numbers to achieve a desired difficulty level, ensuring the puzzle remains solvable. For solving, it guarantees the identification of a unique solution where one exists.

## Contributing

To contribute to this project, you can fork this repository and create pull requests. You can also open an issue if you find a bug or wish to make a suggestion.

## License

This project is licensed under the [GNU General Public License (GPL)](LICENSE).