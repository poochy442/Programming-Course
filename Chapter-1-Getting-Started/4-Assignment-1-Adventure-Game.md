# Assignment 1: Adventure Game

In this assignment, we will create a text-based adventure game using JavaScript.
The game will prompt the player with choices, and the story will progress based on the player's input.

Let's get started!

## Step 1: Setting Up

First, let's set up the basic structure of our game.
Create a new JavaScript file called `adventure-game.js` and open it in your preferred text editor.

```javascript
// adventure-game.js

// Welcome message
console.log("Welcome to the Adventure Game!");
console.log("Let's begin...");

// Game logic goes here
```

In the above code, we have a simple welcome message.
Next, we'll implement the game logic.

## Step 2: Game Logic

To start the game, we'll display a prompt to the player and ask them to make a choice.
Based on their input, we'll determine the next step in the story.

```javascript
// adventure-game.js

// Welcome message
console.log("Welcome to the Adventure Game!");
console.log("Let's begin...");

// Game logic
const readline = require("readline");

const rl = readline.createInterface({
  input: process.stdin,
  output: process.stdout,
});

function startGame() {
  rl.question(
    "You find yourself in a dark room.
What do you do? (type 'explore' or 'escape'): ",
    (answer) => {
      // Process player's choice
      if (answer === "explore") {
        exploreRoom();
      } else if (answer === "escape") {
        escapeRoom();
      } else {
        console.log("Invalid choice. Please try again.");
        startGame();
      }
    }
  );
}

function exploreRoom() {
  console.log("You decide to explore the room...");
  // Continue the story based on the player's choice
}

function escapeRoom() {
  console.log("You try to escape from the room...");
  // Continue the story based on the player's choice
}

// Start the game
startGame();
```

In this code, we're using the `readline` module to read input from the command line.
You will learn how this syntax works soon, but for now just copy what is given here.
The parts you should be changing is the string that is the first parameter to `question` as well as the function where we have access to the answer.

The `startGame` function displays a prompt to the player and checks their choice.
If the choice is valid, it calls the appropriate function (`exploreRoom` or `escapeRoom`).
If the choice is invalid, it displays an error message and restarts the game.

## Step 3: Continuing the Story

Now, let's continue the story based on the player's choices.
Inside the `exploreRoom` and `escapeRoom` functions, we'll display different messages and provide further choices to the player.

```javascript
// adventure-game.js

// ...

function exploreRoom() {
  console.log("You decide to explore the room...");
  console.log("You notice a key on the table and a door on the left.");

  rl.question(
    "What do you do next? (type 'take key' or 'open door'): ",
    (answer) => {
      if (answer === "take key") {
        console.log("You take the key and put it in your pocket.");
        // Continue the story based on the player's choice
      } else if (answer === "open door") {
        console.log("The door is locked. You need a key.");
        // Continue the story based on the player's choice
      } else {
        console.log("Invalid choice. Please try again.");
        exploreRoom();
      }
    }
  );
}

function escapeRoom() {
  console.log("You try to escape from the room...");
  console.log("You find that there is no way out.");

  rl.question("What do you do next? (type 'explore' or 'wait'): ", (answer) => {
    if (answer === "explore") {
      exploreRoom();
    } else if (answer === "wait") {
      console.log("You wait for some time, hoping for help to arrive.");
      // Continue the story based on the player's choice
    } else {
      console.log("Invalid choice. Please try again.");
      escapeRoom();
    }
  });
}

// ...
```

In the above code, we've added additional prompts and choices to the `exploreRoom` and `escapeRoom` functions.
The story progresses differently based on the player's input.

## Step 4: Finalizing the Game

To complete the game, you can continue adding more choices, branching paths, and outcomes based on the player's input.
You can also introduce new functions and variables to handle different scenarios and track the player's progress.

Remember to handle edge cases and validate the player's input to ensure a smooth gameplay experience.

## Summary

Congratulations! You have completed Assignment 1: Adventure Game.
You have built a text-based adventure game using JavaScript that takes user input from the command line and progresses the story based on their choices.

Feel free to expand upon this game and add your own creative elements.
Adventure games offer endless possibilities for storytelling and player interaction.
Have fun exploring and developing your game further!

In the [next chapter](./Chapter-2-Intermediate-Concepts/Arrays-and-Loops.md), we will explore intermediate concepts such as arrays and loops, which will enhance the functionality and interactivity of your programs.

Keep coding and have a thrilling adventure!
