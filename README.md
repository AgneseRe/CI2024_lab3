# N-Puzzle solver
The N-Puzzle is a sliding puzzle consisting of n numbered tiles and an empty space that challenges the player to move pieces along certain routes in order to establish a specific end-configuration (usually in ascending numerical order). 8-puzzle consists of 8 tiles in a 3x3 frame, [15-puzzle](https://en.wikipedia.org/wiki/15_puzzle) has 15 tiles in a 4x4 frame etc.

## This program solves n-puzzle using A* algorithm with various heuristics.

## Heuristics:
- `Hamming Distance`: the number of tiles that are not in the correct position. This heuristic is the simplest, but also the slowest. A huge amount of states will be explored in order to reach the goal state;
- `Manhattan Distance / Taxicab Geometry`: the Manhattan distance of a tile is the distance or the number of tiles away it is from its target position. It is calculated as the sum of the absolute differences between its current row and column and its target row and column. For a certain puzzle configuration, the Manhattan distance is the sum of the Manhattan distances of all the tiles, except the blank tile;
- `Linear Conflict + Manhattan Distance / Taxicab Geometry`: two tiles *tile_a* and *tile_b* are in linear conflict if they are both in their correct row or column, but they are reversed relative to their goal positions. They are in the same row or column, their target positions are in the same row or column and the target position of one of the tiles is occupied by the other tile in that row or column. The heuristic value is Manhattan Distance + 2 * number of linear conflicts.

## Results

