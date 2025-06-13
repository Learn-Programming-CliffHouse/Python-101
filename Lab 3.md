# Lab X3: User Input & Classes

## Learning Objectives

- Learn how to get keyboard input from the user.
- Make buttons that respond to user input.
- Add collision detection to your game.

## Setup
1. Create a new branch using GitHub Desktop and name it `lab-3`.
   - Open GitHub Desktop
   - Click on the "Current Branch" dropdown
   - Click on "New Branch"
   - Name the branch `lab-3`
   - Click "Create Branch"
2. Make sure your virtual environment is activated. You can do this by running:
   ```powershell
   .\venv\Scripts\Activate
   ```

## Challenge 1: Get keyboard input
The white square you animated last time currently just moves on its own in a pretty boring pattern. Let's make it more interactive by allowing the user to control its movement with the arrow keys.

First we should define some more information about the screen and the square. I expect you'll need to make some changes to the code you wrote in the last lab. Here are the requirements:
- The square should be white and 50 x 50 pixels tall.
- The screen should be 800 pixels wide and 600 pixels tall.
- The square should start at the center of the screen
- The square should move at a rate of 1 square width per second.

Now that we have the square and screen set up, let's make it so that the square can be moved using the arrow keys. The square should move in the direction of the arrow key pressed and keep moving in that direction until another arrow key is pressed. If the square reaches the edge of the screen, it should teleport back to the center of the screen.

## Challenge 2: Making a Snake Class
Your code is probably getting a bit messy at this point so let's organize it a bit by creating a `Snake` class. 

This class should have the following:
### Variables
- `x`: The x-coordinate of the snake's head.
- `y`: The y-coordinate of the snake's head.
- `width`: The width of the snake
- `height`: The height of the snake
- `color`: The color of the snake
- `direction`: This should be a list that contains the xy direction the snake is moving in, e.g. `[1, 0]` for right, `[-1, 0]` for left, `[0, 1]` for down, and `[0, -1]` for up.
- `screen_width`: The width of the screen.
- `screen_height`: The height of the screen.

### Methods
- `__init__(self, x, y, width, height, color)`: This method should initialize the snake's position, size, color, and direction.
- `move(self)`: This method should update the snake's position based on its direction and handle border collision logic.
- `draw(self, screen)`: This method should draw the snake on the screen.
- `change_direction(self, direction)`: This method should change the snake's direction based on the input direction. It should not allow the snake to move in the opposite direction (e.g. if the snake is moving right, it should not be able to change direction to left).

Update your main loop to create an instance of the `Snake` class and use its methods to move and draw the snake on the screen. The snake should still be controlled by the arrow keys.

# Submitting Assignment
Once you have completed the challenges, make sure to:
1. Save your work.
2. Commit your changes in GitHub Desktop.
   - Click on "Changes" in the left sidebar.
   - Write a commit message like "Completed Lab 2: Draw Something to the Screen".
   - Click "Commit to lab-3".
3. Push your changes to GitHub.
   - Click on "Push origin" in the top bar.
4. Create a pull request in GitHub
    - Go to your repository on GitHub.
    - Click on "Pull requests" in the top menu.
    - Click on "New pull request".
    - Select `lab-3` as the branch you want to merge into `main`.
    - Click "Create pull request".
    - Add a title and description, then click "Create pull request".
5. Let the instructor know that you have completed the lab by sending a message.

# Rubric

Total Points: 10

- Left thorough comments explaining what the code is doing - 2 points (1/2 credit for leaving comments in only a few places)
- Completed Challenge 1 - 4 points
- Completed Challenge 2 - 4 points
