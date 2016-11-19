##Minesweeper
Minesweeper is a popular puzzle game distributed with Windows OS. The objective of the game is simple: reveal the blocks without detonating the mines. Number on each block indicates the number of mines in the 8 blocks surrounding it. The numbers are used to determine the safe blocks. You win the game when you've revealed all the safe blocks on board.

##About this clone
This is a clone of minesweeper made for educational purposes. It's written in JS. The game has been built part by part. Each part works with others to make the whole thing work. Understanding how each part works and the way they communicate can help you figure out how it works.

##Parts
Each part does a specific job and communicates with other parts to keep the system running. Parts communicate by directly calling each other and passing data to others through arguments and/or global variables.

List of parts:

- renderBoard
- generateMap
- blockClickListener
- blockRightClickListener
- generateMines
- makeMapVisible
- revealBlock
- invisbleBlockCount
- inMap
- numberBlocks
- getRandomInt

##renderBoard
It draws the board on the screen. It provides an interface for the user to play the game. It's called whenever the board is updated. It's because the changes are buffered and rendering works absolutely, not relatively.

##generateMap
A global variable 'map' is created which holds info about the board.
##generateMines
Random locations are picked and saved on the global variable, 'map'.
##blockClickListener
It stands there, waiting for the user to click a block. It responds accordingly.
##blockRightClickListener
Same as blockClickListener but it listens for right clicks on blocks. Its only job is to flag down blocks.
##makeMapVisible
It makes the entire map visible. It's called when the user clicks on a mine and the game ends.
##revealBlock
It reveals a specific block along with nearby blank blocks (not numbered). It's recursive which means it calls itself, passing the blank blocks in the surrounding in each call.
##inMap
It determines if a given location is within the borders of the map.
##invisibleBlockCount
It counts the blocks in the map which are still not revealed.
##numberBlocks
It goes through every single block on board and numbers them. Number equals the mine count in the surrounding (8 max).
##getRandomInt
Generate a random int, simple as that!