# Lab 2: Draw Something to the Screen

## Learning Objectives
By the end of this lab you will have:
- Created a basic pygame window
- Drawn shapes and text to the screen
- Moved shapes around the screen using keyboard input

## Setup
1. Make sure your virtual environment is activated. You can do this by running:
   ```powershell
   .\venv\Scripts\Activate
   ```
2. Install pygame
    ```bash
    pip install pygame
    ```
A note about pip: `pip` is the package installer for Python. You can use it to install packages other people have written from the Python Package Index (PyPI) and other package repositories. Package repositories are places where people can upload their code so that others can use it. [Here's the PyPi page for pygame](https://pypi.org/project/pygame/). The PyPi page will also have instructions on how to install the package, and it will usually have a link to the package's documentation. This is a good place to start if you want to learn more about how to use any package.

3. Create a new branch using github desktop and name it `lab-2`
   - Open GitHub Desktop
   - Click on the "Current Branch" dropdown
   - Click on "New Branch"
   - Name the branch `lab-2`
   - Click "Create Branch"

4. Create a new Python file called `snake_game.py` in your project directory.

## Challenge 1: Create a Basic Pygame Window
In this challenge, you will create a basic pygame window that displays a title and a background color. Below is how you can accomplish this, but I'd like you to try to write the code yourself first. If you get stuck, you can refer to the code below.

```python
import pygame
import sys

# Initialize Pygame
pygame.init()

# Set up the display
width, height = 800, 600
screen = pygame.display.set_mode((width, height))
pygame.display.set_caption("Snake Game")

# Set the background color
background_color = (0, 0, 0)  # Black
screen.fill(background_color)

# Main loop
while True:
    for event in pygame.event.get():
        # Check for quit event. (User closing the window)
        if event.type == pygame.QUIT:
            pygame.quit()
            sys.exit() # Exit the program

    pygame.display.flip()
```

## Challenge 2: Draw Shapes and Text
A blank screen is not very interesting, so let's draw some shapes and text on the screen. You'll need to modify the main loop from your previous challenge and add some drawing code.

For this challenge:
1. Draw a white rectangle in the center of the screen
2. Draw some text that says "Score: 0" in the top left corner

I wont be providing sample code for this challenge and I encourage you to start looking at the documentation.
[Pygame Draw Documentation](https://www.pygame.org/docs/ref/draw.html)
[Example of drawing shapes](https://www.geeksforgeeks.org/python/pygame-drawing-objects-and-shapes/)
[Pygame Font Documentation](https://www.pygame.org/docs/ref/font.html)
[Example of drawing text](https://www.geeksforgeeks.org/python-display-text-to-pygame-window/)

## Challenge 3: Moving the Rectangle
In this challenge, you will make the rectangle move to the right and when it reaches the edge of the screen, it will change direction and move to the left.

There won't be any sample code or documentation for this challenge, you should have everything you need to complete this.

# Submission
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
- Correctly submitted the assignment using a lab-2 branch and opening a pull request on github - 1 point
- Left thorough comments explaining what the code is doing - 2 points (1/2 credit for leaving comments in only a few places)
- Challenge 1 - 2 points
- Challenge 2 - 2 points
- Challenge 3 - 3 points