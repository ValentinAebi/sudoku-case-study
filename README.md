# Case study: sudoku solver

A simple sudoku solver, written in the Grattlesnake experimental language (https://github.com/ValentinAebi/Rattlesnake/tree/rattlesnake-v0.2-gradient).
This is an example of a gradual ocap program, and a case study for my MSc thesis.

The solver is written according to the ocap discipline and uses two "libraries", that do not follow this discipline: `TableReader`, which reads a grid from a file, 
and `GridFormatter`, which can be parametrized to display the grid with separators between the sectors/blocks.

The rules of the sudoku game can be found at https://en.wikipedia.org/wiki/Sudoku. This solver only handles the classic 9x9 version of the game.

Note: the behavior of the solver is undefined if the empty grid given to it already violates some rules of the sudoku game (e.g. if it has twice the same digit in the same line).


## Running the program

Either use make: `make grid1` (or just make as it is the default target), `make grid2`, `make help`.

Or copy-paste the commands from the Makefile.


## Resolution algorithm

Empty cells maintain a list of candidates, which are eliminated when assigning them to the cell would contradict the rules of sudoku. When this process gets stuck, the grid is copied and guesses are made in the copies regarding the value of the cell with the least number of candidates. The solver then tries to solve the grids with guessed cell recursively (i.e. it goes back to candidates-based deducutions until it gets stuck or the grid is filled).


## Requirements

- Java >= 21, e.g. [22.0.2](https://www.oracle.com/java/technologies/javase/jdk22-archive-downloads.html)
- Make (optional). Installation instructions: [Ubuntu](https://linuxhint.com/install-make-ubuntu/), [Windows](https://www.technewstoday.com/install-and-use-make-in-windows/).


## References

The sudoku grids used in this repo are taken from https://projecteuler.net/project/resources/p096_sudoku.txt.

