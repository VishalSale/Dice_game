# Dice Game

## Overview

This Dice Game is a fun, two-player game where players take turns rolling a dice to accumulate points. The objective is to be the first player to reach a predefined score (e.g., 20 points). The game is implemented using HTML, CSS, and JavaScript and is available for everyone to play at [Dice Game](https://vishalsale.github.io/Dice_game/).

## Project Structure

```
dice-game/
│
├── index.html       # HTML structure of the game
├── style.css        # CSS styles for the game
├── script.js        # JavaScript logic for the game
└── images/
    ├── dice-1.png   # Image of dice showing 1
    ├── dice-2.png   # Image of dice showing 2
    ├── dice-3.png   # Image of dice showing 3
    ├── dice-4.png   # Image of dice showing 4
    ├── dice-5.png   # Image of dice showing 5
    └── dice-6.png   # Image of dice showing 6
```

## How to Play

1. **Start the Game**: Open the game in your web browser. The game starts with Player 1. Both players' scores are set to 0.
2. **Roll the Dice**: Player 1 clicks the "Roll dice" button to roll the dice.
   - If the dice shows a number between 2 and 6, that number is added to the player's current score.
   - If the dice shows a 1, the player's turn ends, their current score is reset to 0, and it becomes the next player's turn.
3. **Hold**: The player can choose to "Hold" their current score by clicking the "Hold" button.
   - The current score is added to the player's total score.
   - It becomes the next player's turn.
4. **Winning the Game**: The first player to reach or exceed 20 points in their total score wins the game.
   - The game ends, and the winner is highlighted.
5. **New Game**: Click the "New game" button to reset and start a new game.

## JavaScript Logic

The JavaScript code in `script.js` handles the core game logic, including initializing the game, switching players, rolling the dice, and holding the score. Key components include:

### Variables

- `playing`: Boolean indicating if the game is currently active.
- `scores`: Array storing the total scores of both players.
- `activePlayer`: Index of the current active player (0 or 1).
- `currentScore`: Current score of the active player.

### Functions

- `init()`: Initializes the game by resetting all scores and setting Player 1 as active.
- `switchPlayer()`: Switches the active player and resets the current score.
- `btnRoll.addEventListener('click', ...)`: Handles the dice roll event.
- `btnHold.addEventListener('click', ...)`: Handles the hold event.
- `btnNew.addEventListener('click', ...)`: Resets the game when the "New game" button is clicked.

### Example Workflow

1. **Game Initialization**: The `init()` function sets the starting conditions of the game.
2. **Rolling the Dice**: Clicking the "Roll dice" button triggers a dice roll. If the result is 1, the active player switches; otherwise, the score is added to the current score.
3. **Holding the Score**: Clicking the "Hold" button adds the current score to the total score and switches the active player.
4. **Winning**: If a player's total score reaches or exceeds 20, the game declares them the winner and ends.

## Styling

The CSS styles in `style.css` define the visual appearance of the game, including layout, colors, and fonts. The `.player--active` and `.player--winner` classes are used to highlight the active player and the winning player, respectively.

## Images

Dice images (`dice-1.png` to `dice-6.png`) visually represent the result of a dice roll and are stored in the `images/` directory.

## How to Run

1. Clone the repository or download the project files.
2. Open `index.html` in a web browser to start the game.

You can also play the game directly online at [Dice Game](https://vishalsale.github.io/Dice_game/).

Enjoy the game!
