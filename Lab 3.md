# Lab X3: User Input & Classes

## Learning Objectives

- Learn how to get keyboard input from the user.
- Make buttons that respond to user input.
- Add collision detection to your game.

## Setup
1. Make sure your virtual environment is activated. You can do this by running:
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

## Challenge 2: Makeing a Snake Class
## Challenge 3: Subtitle

```

# Submitting Assignment
Once you have completed the challenges, make sure to:
1. Save your work.
2. Commit your changes in GitHub Desktop.
   - Click on "Changes" in the left sidebar.
   - Write a commit message like "Completed Lab 2: Draw Something to the Screen".
   - Click "Commit to lab-2".
3. Push your changes to GitHub.
   - Click on "Push origin" in the top bar.
4. Create a pull request in GitHub
    - Go to your repository on GitHub.
    - Click on "Pull requests" in the top menu.
    - Click on "New pull request".
    - Select `lab-2` as the branch you want to merge into `main`.
    - Click "Create pull request".
    - Add a title and description, then click "Create pull request".
5. Let the instructor know that you have completed the lab by sending a message.

# Rubric

Total Points: 10

- Criteria 1 - 1 point
- Criteria 2 - 1 point
- Criteria 3 - 1 point
- Criteria 4 - 1 point
- Criteria 5 - 2 points
- Criteria 6 - 2 points
- Criteria 7 - 2 points
