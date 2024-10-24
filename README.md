# Game of Life Project

## Overview

**The Game of Life** is a 2D evolutionary game where you start with a grid of dead cells. You can select specific cells to be alive, and the game evolves according to a set of rules to determine the state of each cell.

## Rules

The classic rules for the Game of Life are as follows:
1. If a cell is alive and has 2 or 3 living neighbors, it stays alive.
2. If a cell is dead and has exactly 3 living neighbors, it becomes alive.
3. Otherwise, the cell dies.

## Project Structure

The project is structured to demonstrate various design patterns through refactoring:

- **life1original**: The initial implementation.
- **life2state**: Refactored using the State pattern.
- **life3singleton**: Refactored using the Singleton pattern.
- **life4command**: Further refactoring with the Command pattern.
- **life5observer**: Implementation using the Observer pattern.
- **life6visitor**: Final refactoring with the Visitor pattern.

## Design Patterns

### State Pattern
- Cells are represented by a `Cell` class instead of a Boolean primitive.
- A `CellState` interface with two concrete states: `AliveState` and `DeadState`.

### Singleton Pattern
- `AliveState` and `DeadState` are implemented as singletons to avoid creating multiple instances.

## Additional Features

- Cells can determine their number of alive neighbors using an internal list of neighboring cells.
- The logic for computing alive neighbors has been moved from the main game application to the `Cell` class.

## Running the Project

1. Load `DuDraw.jar` as an external library on your build path.
2. Use the mouse to toggle cells between alive and dead states.
3. Advance the evolution one step at a time using the spacebar.
