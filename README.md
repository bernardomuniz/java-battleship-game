# Java Battleship Game
## Author: Bernardo Muniz

### How to use the repository
To clone the repository to your local machine using Git, simply run the following command in your terminal:

`git clone https://github.com/bernardomuniz/java-battleship-game.git`

### About
This repository aims to present the implementation of a Battleship game using Java. During the development of the project, the **algs4** library was used to draw the game boards.

To run the project, make sure you are inside the cloned folder and have Gradle installed on your computer. Then, type the following command in your terminal:

`gradle run` or `./gradlew run`

## Battleship
Battleship is a board game for two players.  
Each player has a fleet of 5 ships of different sizes, as shown in Table 1. These ships must be placed on a 10x10 grid, without overlapping and without going beyond the board’s boundaries.  

The game is played in turns. In each round, a player fires a shot at a grid position on the opponent’s board that has not yet been targeted. The opponent informs whether the shot was a hit or a miss.  
If it was a hit, the opponent also informs whether the ship has been sunk. The turn then passes to the other player.  

The game ends when all of one player’s ships are sunk, and the other is declared the winner.

The table below shows the ships present in the Battleship game, along with their size and identification:

<div align="center">

| Ship              | Size (cells) | Symbol |
|:-----------------:|:------------:|:------:|
| Aircraft Carrier  |      5       |   P    |
| Battleship        |      4       |   E    |
| Cruiser           |      3       |   C    |
| Submarine         |      3       |   S    |
| Destroyer         |      2       |   N    |

</div>

### Placing ships
When starting the game, you can choose between placing your ships automatically or manually.  
- If you choose **automatic placement**, the game generates a board with ships randomly placed and starts immediately.  
- If you choose **manual placement**, you can decide where to position each ship on the board.  

A convention was adopted where, when entering a position to place a ship, you are choosing where the **tip of the ship** will be, and the remaining cells will be filled according to the ship’s size.  

When placing a ship manually, you can choose between two orientations:
- **Horizontal**: places ships to the right.
- **Vertical**: places ships upward.

This convention was used to simplify ship placement.  

To place a ship, you must enter a valid coordinate in the format **"(row) (column)"**, where rows vary from **A–J** and columns from **0–9**.  
A valid position would be, for example: `A 5`.

### Firing shots
After placing the ships, the Battleship game begins. Players take turns firing shots at the opponent’s board — in this case, against the computer.  

Below is an example of gameplay interaction:

<p align="center">
  <img src="/batalhanaval.png" alt="Game Board" width="600">
</p>

The board titled **"Ships"** represents your board, while the board titled **"Targets"** represents the computer’s board, where your shots will be fired in an attempt to sink all ships.  

Similar to ship placement, to fire a shot you must enter a valid coordinate in the format **"(row) (column)"**, where rows vary from **A–J** and columns from **0–9**.

- If either the player or the computer hits an enemy ship, the turn passes to the other player.  
- At the end of the match, you will see game statistics, including the player and the number of victories.  

Feel free to enjoy the Battleship game!
