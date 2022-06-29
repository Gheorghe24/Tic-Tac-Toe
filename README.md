# Hangout-Game

Firstly I declare some variables and constants such as:
- statusDisplay
- gameActive
- currentPlayer
- gameState
- winningMessage, drawMessage, currentPlayerTurn
- winningConditions

Then I created some functions :

handleCellPlayed
-------------------
We update our internal game state to reflect the played move, 
as well as update the user interface to reflect the played move

handlePlayerChange
-------------------
Change the content of currentPlayer and display the player turn  

handleResultValidation
-----------------------
Initialize a variable to store if someone won the round
I check every case when the player clicks on a cell and I am wondering 
if he didn't won the round with "winningConditions"

Then I will check weather there are any values in our game state array 
that are still not populated with a player sign and to display the draw message

If we get to here we know that the no one won the game yet, 
and that there are still moves to be played, so we continue by changing the 
current player (handlePlayerChange).

handleCellClick
------------------
We will save the clicked html element in a variable for easier further use(clickedCell)

Here we will grab the 'data-cell-index' attribute from the clicked cell to 
identify where that cell is in our grid. 
Please note that the getAttribute will return a string value. Since we need an 
actual number we will parse it to an integer(number)

Next up we need to check whether the call has already been played, 
or if the game is paused. If either of those is true we will simply ignore the click.

If everything is in order we will proceed with the game flow

handleRestartGame
------------------
And finally we add our event listeners to the actual game cells, as well as our 
restart button
In this function we set the gameActive to true value, the currentPlayer will be X,
clear the gameState and every cell for a new game.