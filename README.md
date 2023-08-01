# ChessEngine

![Chess_Still](https://github.com/KriChau95/ChessEngine/assets/140979138/58e5441a-3d3d-4369-a329-08f7d528e2b8)

This is a Chess Engine made using PyGame. It uses the principles of object oriented programming to coordinate the logic and visuals of the game of Chess.
There are 3 main components to the program: 
  1. The Main Chess Driver File 
  2. The Chess Engine File
  3. The SmartMove Finder

# 1. The Main Chess Driver File
This file takes care of the main game loop and the animations. It coordinates :
* the drawing of the pieces on the board after every move
* drawing the possible moves a piece has after it is clicked
*  updating the moveLog, which displays the moves made from start to the current point in the game

# 2. The Chess Engine File
This file stores information about the Chess Game and the current GameState
It contains a GameState class that:
* stores instance variables about the current player to move
* whether or not the current player is in check
* the current position of all of the pieces on the board
* the enPassant and castling possibilities at the current stage of the game
* whether or not the game is in an endgame scenario - checkmate or stalemate
* methods for making moves so that the moves are reflected in the data structure (a 2D list) that represents the board
* several helper methods that determine all possible moves on a chess board based on the moves made so far, and the current state of the board

There is also a Move class defined to combine and package information about a certain move (starting and ending square, type of move - normal/enPassant/castle)
 
# 3. SmartMove Finder File
This file codes the logic of the computer player option in the Chess Game
* It uses nega max alpha-beta pruning to determine the best available move for the computer player
* It contains several different versions of MinMax algorithms, each corresponding to a different capability for the computer player
