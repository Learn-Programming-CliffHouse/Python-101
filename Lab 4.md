# Lab 4: Food Module

## Learning Objectives

- Further experience with classes
- Update the score when the snake eats the apple
- Understand how to use the random module for positioning
- Practical applications for lists

## Setup
1. Create a new branch using GitHub Desktop and name it `lab-4`.
   - Open GitHub Desktop
   - Click on the "Current Branch" dropdown
   - Click on "New Branch"
   - Name the branch `lab-4`
   - Click "Create Branch"
2. Make sure your virtual environment is activated. You can do this by running:
   ```powershell
   .\venv\Scripts\Activate
   ```

## Challenge 1: Create the Apple Class
1. Create a new file called `Apple.py`.
2. Define the `Apple` class with the following attributes:

### Variables
   - `x`: The x-coordinate of the apple.
   - `y`: The y-coordinate of the apple.
   - `width`: The width of the apple.
   - `height`: The height of the apple.
   - `color`: The color of the apple (e.g., red).

### Methods
   - `__init__(self, x, y, width, height, color)`: This method should initialize the apple's position, size, and color.
   - `draw(self, screen)`: This method should draw the apple on the screen.
   - `respawn(self, snake)`: This method should reposition the apple to a new random location within the screen bounds that isn't occupied by the snake.

## Challenge 2: Have the Snake Eat the Apple
1. In the `snake.py` file, import the `Apple` class.
2. Modify the `update` method of the `Snake` class to check for collision with the apple.
3. If the snake eats the apple, call the `respawn` method of the apple to reposition it.

## Challenge 3: Update the Score
1. In the `game.py` file, create a variable called `score` and initialize it to 0.
2. Incriment the score by 1 each time the snake eats an apple.
3. Display the score on the screen using Pygame's font rendering.

## Challenge 4: Grow the Snake
1. Create a new variable inside the snake class called bodies that is a list. This list will hold the positions of the snake's body segments. Each entry in the list should be a tuple representing the (x, y) coordinates of each segment.
2. When the snake moves, move the head of the snake into the new position and check that the snake's head isn't trying to move into a position that is occupied by its body. If it enters the body that should count as a game over. You will probably need to have the snake's `move` method return a boolean indicating whether the move was successful or not. This can be used by the main loop to determine if the game is over. Now iterate through the bodies list. Each entry in the list should go to the position of the previous entry in the list.
3. Update your `draw` method to draw each segment of the snake's body using the positions stored in the bodies list.
4. When the snake eats an apple, append a new segment to the bodies list at the end of the list. The new segment should be positioned at the last segment's position.


# Submitting Assignment
Once you have completed the challenges, make sure to:
1. Save your work.
2. Commit your changes in GitHub Desktop.
   - Click on "Changes" in the left sidebar.
   - Write a commit message like "Completed Lab 2: Draw Something to the Screen".
   - Click "Commit to lab-4".
3. Push your changes to GitHub.
   - Click on "Push origin" in the top bar.
4. Create a pull request in GitHub
    - Go to your repository on GitHub.
    - Click on "Pull requests" in the top menu.
    - Click on "New pull request".
    - Select `lab-4` as the branch you want to merge into `main`.
    - Click "Create pull request".
    - Add a title and description, then click "Create pull request".
5. Let the instructor know that you have completed the lab by sending a message.

# Rubric

Total Points: 10

- Left thorough comments explaining what the code is doing - 1 point
- Completed Challenge 1 - 2 points
- Completed Challenge 2 - 2 points
- Completed Challenge 3 - 1 points
- Completed Challenge 4 - 4 points

