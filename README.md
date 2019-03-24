This is a working Tic Tac Toe game on IOS.

#  Common Logic for Tic Tac Toe 

The logic of Tic Tac Toe as follows
To make a Tic Tac Toe game, you need to 
layout 9 buttons with image (expectation: see 9 nought buttons)
identify the button that trigger button pressed event(expectation: press on the button will show image)
`activePlayer`  to identify which round for `cross`  or  `nought` 
An array of 9 items to store the `gameState` so that if it is pressed before, do not modify the state using `0` for `untouched`, `1` for `nought`, `2` for `cross`.

Then you need to define the 8 winning patterns and detect the winning pattern in each move using a for loop. The condition would be something like this
```
gameState[combination[0]] != 0 && gameState[combination[0]] == gameState[combination[1]] && gameState[combination[1]] == gameState[combination[2]]
```
The `combination` is one of the 8 winner patterns. This will check for the item at index `0`,  `1` , `2`  in the `combination` is the same.

If someone has won, you need to show the text to display the winner and show play again button. At the same time you need to mark the game as `ended` so that further clicks on the game board will not display anything.

Lastly, add the logic for play again button to restart the game once pressed. You need to reset the game state to initial state and hide the winner label and play again button.
