# Case study: sudoku solver

A simple sudoku solver, written in the Grattlesnake experimental language (https://github.com/ValentinAebi/Rattlesnake/tree/rattlesnake-v0.2-gradient).
This is an example of a gradual ocap program, and a case study for my MSc thesis.

The solver is written according to the ocap discipline and uses two "libraries", that do not follow this discipline: `TableReader`, which reads a grid from a file, 
and `GridFormatter`, which can be parametrized to display the grid with separators between the sectors/blocks.

The rules of the sudoku game can be found at https://en.wikipedia.org/wiki/Sudoku. This solver only handles the classic 9x9 version of the game.

## References

The sudoku grids used in this repo are taken from https://projecteuler.net/project/resources/p096_sudoku.txt.

