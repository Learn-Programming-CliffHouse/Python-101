# Lab 5: Game States

## Learning Objectives

- Understand the concept of game states
- Implement a game over state
- Allow the player to restart the game
- Practice file I/O for saving and loading game state

## Setup
1. Create a new branch using GitHub Desktop and name it `lab-5`.
   - Open GitHub Desktop
   - Click on the "Current Branch" dropdown
   - Click on "New Branch"
   - Name the branch `lab-5`
   - Click "Create Branch"
2. Make sure your virtual environment is activated. You can do this by running:
   ```powershell
   .\venv\Scripts\Activate
   ```

## Challenge 1: Impliment a pause state
1. When I press the escape key, the game should pause and display a pause menu.
2. The pause menu should have options to resume the game, restart the game, and save the game.
3. Impliment the resume option to continue the game from where it was paused. The other options should be placeholders for now, as we will implement them in later challenges.

## Challenge 2: Implement Game Over State
1. Create a game over state that is triggered when the snake collides with itself or the walls.
2. This is essentially the same as the pause state, but it should display your score, a game over message, and an option to restart the game.

## Challenge 3: Restart Game
1. Implement the restart option to reset the game state and start a new game. This should reset the snake's body length, position, the apple's position, and the score.
2. It might make sense to create a method in your `Snake` class that resets the snake's position and length.

## Challenge 4: Implement a Save and Load Game State
This is a pretty tricky task. We need some way to save the current game state to a file and load it back later. This will allow players to save their progress and continue later. We will be using a JSON file to store the game state. JSON is a human readable data storage format that is easy to read and write in Python. Python has a built in json library that lets you easily dump python variables to a file and load them back later. Check out the documentation for the [json module](https://docs.python.org/3/library/json.html) for more information. A possibly more usefule link is the [json module tutorial](https://www.w3schools.com/python/python_json.asp) which has some examples of how to use the json module in Python.

### Things we want to save:
- Snake's position and length
- Apple position
- Current score

### Steps to Implement Save and Load:
1. Create a save method in the snake class that returns a s json string representing the snake's current state.
2. Create a load method that initializes the snake's state from a json string.
3. Create a save method in the apple class that returns a json string representing the apple's current state.
4. Create a load method that initializes the apple's state from a json string.
5. In the main game loop, implement a function called `save_game` that saves the current game state to a file when the player chooses to save.
6. Implement a function called `load_game` that loads the game state from a file when the player chooses to load.
7. Have the pause/game over menu call the respective functions when you press those buttons.


# Submitting Assignment
Once you have completed the challenges, make sure to:
1. Save your work.
2. Commit your changes in GitHub Desktop.
   - Click on "Changes" in the left sidebar.
   - Write a commit message like "Completed Lab 2: Draw Something to the Screen".
   - Click "Commit to lab-5".
3. Push your changes to GitHub.
   - Click on "Push origin" in the top bar.
4. Create a pull request in GitHub
    - Go to your repository on GitHub.
    - Click on "Pull requests" in the top menu.
    - Click on "New pull request".
    - Select `lab-5` as the branch you want to merge into `main`.
    - Click "Create pull request".
    - Add a title and description, then click "Create pull request".
5. Let the instructor know that you have completed the lab by sending a message.

# Rubric

Total Points: 10

- Complete challenge 1 - 1 point
- Complete challenge 2 - 2 points
- Complete challenge 3 - 3 points
- Complete challenge 4 - 4 points