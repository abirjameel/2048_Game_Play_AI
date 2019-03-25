# 2048 Game Play Artificial Intelligence Algorithm

An instance of the 2048-puzzle game is played on a 4×4 grid, with numbered 
tiles that slide in all four directions when a player moves them. 
Every turn, a new tile will randomly appear in an empty spot on the board,
with a value of either 2 or 4. Per the input direction given by the player,
all tiles on the grid slide as far as possible in that direction, 
until they either (1) collide with another tile, or (2) collide with 
the edge of the grid. If two tiles of the same number collide while 
moving, they will merge into a single tile, valued at the sum of the 
two original tiles that collided. The resulting tile cannot merge with 
another tile again in the same move.  

## Implementation of Algorithm
To solve this 2048-puzzle game i have to use following algorithms as a requirement of this
project.  

##### Minimax Algorithm
The Minimax Algorithm. There are many viable strategies to beat the 2048-puzzle game, but in this project we will be practicing with the minimax algorithm.

##### Alpha-Beta Pruning
 This should speed up the search process by eliminating irrelevant branches. 

##### Heuristic Functions
To limit the maximum height of the game tree. Unlike elementary games like tic-tac-toe, in this game it is highly impracticable to search the entire depth of the theoretical game tree.

##### Heuristic Weights
More than one heuristic function will be used. So, will need to assign weights 
associated with each individual heuristic. Deciding on an appropriate set 
of weights will take careful reasoning, along with careful experimentation.

## Code Skeleton

- **GameManager.py:** 
This is the driver program that loads Computer AI and Player AI, 
and begins a game where they compete with each other. 

- **Grid.py:** 
This module defines the Grid object, along with some useful operations: 
`move()`, `getAvailableCells()`, `insertTile()`, and `clone()`. 
- **BaseAI.py:** 
This is the base class for any AI component. All AIs inherit from this 
module, and implement the `getMove()` function, which takes a Grid object 
as parameter and returns a move (there are different "moves" for different
AIs).
- **ComputerAI.py:** 
This inherits from BaseAI. The `getMove()` function returns a computer action
 that is a tuple (x, y) indicating the place you want to place a tile.
- **PlayerAI.py:** 
This inherits BaseAI. The `getMove()` function, returns a number that indicates the player’s action. 
In particular, 0 stands for "Up", 1 stands for "Down", 2 stands for "Left",
 and 3 stands for "Right".
- **BaseDisplayer.py and Displayer.py:**
 These print the grid.
 
 ## How to run 
 Use the following commands to run this program. 
 
 `python3 GameManager_3.py`  
 
 or if you are on windows with python 3.5+ as your default python. 

 `python GameManager_3.py`