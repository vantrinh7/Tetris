# Tetris

Tetris is a tile-matching puzzle video game orginially designed by Alexey Pajitnov and released in 1984. This program construct a simple version of Tetris. 

In the game, puzzle pieces with the shape of I, L, J, T, S, Z, O fall down from the top of the window to the bottom of the window. While the pieces are falling, user needs to decide where to put them so as to fill as many horizontal lines as possible. Each full horizontal line is cleared from the window and counted towards the total score.

User can make the pieces:
- Move to the left: Left arrow key
- Move to the right: Right arrow key
- Increase falling speed: Down arrow key
- Rotate clockwise: X key
- Rotate counter clockwise: Z key

<br>

  ![start](misc/start.png)       ![play](misc/play.png)     ![clear](misc/clear.png)

<br>

The Tetris board is actually a two-dimensional array of boolean values. At the beginning of the game, these values are initialized to *false*. In the space where a Tetris piece is present, the values are set to *true*. By incrementing or decrementing array indices, the piece can move left, right or down. The use of a timer and an action listener creates the effect of the piece automatically "falling down" by gravity.

Each Tetris piece is a three-dimensional array containing 4 two-dimensional arrays that represent 4 possible rotations of that piece. By incrementing or decrementing array indices, the piece can move clockwise or counter clockwise. 

When a line is full - meaning that the row is filled with true values - the program increases the score, changes true values to false and loop through the board to copy everything down one row. These actions create the effect that a row is cleared and blocks above the removed row fall down to the ground.
