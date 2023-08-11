
## Analyze the app's functionality

As a user, I want a feature because of reason.

MVP (Minimum Viable Product)

As a user
- I want to be able to have two players, because that is how Connect 4 is played.
- I want to be able to take turns
- I want to alternate dropping colored disc into 1 of 7 columns
- I want to be able to win if I get 4 in a row
- I want to know who won, who lost, or if it was a tie
- I want to be able to play the game again if it's over

If I have some time I'd like to have these
- I want a success animation
- I want a dropping animation
- Difficulty setting
- I want to choose my color of the disc
- I want to keep track of total wins & losses

## Think about the overall design (look & feel) of the app

- Clean
- Purple and orrange for the discs
- Poppins - font
```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@100&display=swap" rel="stylesheet">
```
```css
font-family: 'Poppins', sans-serif;
```

## Wireframe the UI

A wireframe is a way to represent your application

- High fidelity
    - Working demo
    - Images
    - Buttons might be clickable
    - Hover effects happen
    - Little more than just a drawing
- Low fidelity
    - Just a drawing
    - Layout of the page
    - Where is the header going?
    - Where are my messages to the user going?
    - Where are all my buttons going?
    - Does this feel too crowded? Does this feel too empty?

## Pseudocode

- Define required constants
    - Color constant
- Define required variables used to track the state of the game
    - Game board - 1 big array that holds 7 smaller 6 index arrays
    - Turn - 1 || -1 (Player 1 & 2)
    - Winner - null || 1 || -1 || "T"

- Cache DOM elements
    - Message place
    - Play again button
    - Column buttons/ markers

- Upon loading the app should:
    - Init the state vars
    - Create the 7 nested arrays
    - Turn var should be set to 1 (player 1)
    - Winner var should be set to null
- Render changes to the DOM
    - Render the board, should be completely blank
    - Render the message "Purple's Turn"
    - Do not render the play again button

- Wait for interaction

- Handle a player clicking a column button
    - Update the board array
    - Update the turn var
    - Check for a winner
    - LASTLY, re-render the board with the player's move

- Handle a player clicking the replay button
    - Reset the state vars ( back to default on page load functions)
    - LASTLY, re-render the board

- Check for a winner
    -Check for 4 in a row
    - We will use offsets to count the colors of the disc in the arrays

## Identify the application's state (application-wide data)

- game baord - array of 7 nested arrays
```js
let board
```
- turn var
```js
let turn
```
- winner var
```js
let winner
```

## Set up the project

