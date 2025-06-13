# Lab 6: Refactoring & Enhancements

## Learning Objectives

- Learn about object inheritance and how to use it to create a base class for game objects.
- Refactor existing code to improve organization and readability.
- Learn how to use enums to manage game states.
- Implement a simple menu system for the game.

## Setup
1. Create a new branch using GitHub Desktop and name it `lab-6`.
   - Open GitHub Desktop
   - Click on the "Current Branch" dropdown
   - Click on "New Branch"
   - Name the branch `lab-6`
   - Click "Create Branch"
2. Make sure your virtual environment is activated. You can do this by running:
   ```powershell
   .\venv\Scripts\Activate
   ```

## Challenge 1: Object Inheritance
Up until this point you've been making stand-alone classes for each game object. I bet you've also notice a lot of places where the code is repeated between these classes.
We can use object inheritance to create a base class for all game objects. This will allow us to define common properties and methods in one place, and then extend them in specific classes.
1. Create a base class called `GameObject` that has the following properties:

### Variables
- `x`: The x-coordinate of the object.
- `y`: The y-coordinate of the object.
- `width`: The width of the object.
- `height`: The height of the object.
- `color`: The color of the object.

### Methods
- `draw()`: A method that draws the object on the screen using the `pygame.draw.rect()` function. You might not even need to implement this method in the base class, but it should be defined so that subclasses can override it.
- `update()`: A method that updates the object's position or state. This can be empty in the base class, but should be overridden in subclasses if needed.

## Challenge 2: Refactor Existing Classes
1. Refactor the `Snake` and `Apple` classes to inherit from the `GameObject` class. Here's a good tutorial on [Python inheritance](https://www.w3schools.com/python/python_inheritance.asp).

The apple class will probably leave its update method empty, but the snake class will need to override the update method to handle movement and collision detection.

2. Update the main game loop so that all game objects are stored in a list called `game_objects`. This list should contain instances of the `Snake` and `Apple` classes. The game loop should iterate over this list to update and draw each object.

## Challenge 3: Enumerations for Game States
Python's `enum` module allows us to define a set of named values. This is useful for managing game states in a more readable way. Here is a great [tutorial on Python enums](https://www.w3schools.com/python/python_enumerations.asp).
1. Create an `enum` called `GameState` with the following states:
   - `PAUSE`: The main menu of the game.
   - `PLAYING`: The game is currently being played.
   - `GAME_OVER`: The game is over and the player can restart or exit.
2. In the game loop, there should be section that checks the current game state and updates the game accordingly. For example, if the game state is `PAUSE`, it should display the main menu, and if it's `PLAYING`, it should update the game objects and draw them on the screen.

## Challenge 4: Doc Strings
All programming languages have many different style guides that developer teams will follow to make it look like their code was all written in the same style. Python has a few different style guides, but the most popular one is [PEP 8](https://www.python.org/dev/peps/pep-0008/). One of the things that PEP 8 recommends is to use docstrings to document your code. [Follow this documentation guide](https://peps.python.org/pep-0257/#what-is-a-docstring) to add docstrings to all of your functions and classes
Add comments to all methods in your classes. Each method should have a comment that describes what it does, its parameters, and its return value (if any). This will help you and others understand the code better in the future.

## Challenge 5: Python Types
Python is a dynamically typed language. That means that it doesn't care what you assign to a variable, it will just let you do it. This can lead to bugs if you're not careful, so it's a good idea to use type hints to indicate what type of data a variable should hold.
1. Add type hints to all your functions and methods. For example, if a function takes an integer as an argument, you can write it like this:
   ```python
   def my_function(x: int) -> None:
       pass
   ```
   This indicates that `x` should be an integer and the function does not return anything.

Another example is if a function returns a string, you can write it like this:
   ```python
   def get_name() -> str:
       return "John Doe"
   ```
2. Use type hints to indicate the types of variables in your classes. For example, if a class has an `x` variable that should be an integer, you can write it like this:
   ```python
   class MyClass:
       def __init__(self, x: int):
           self.x: int = x
   ```

# Submitting Assignment
Once you have completed the challenges, make sure to:
1. Save your work.
2. Commit your changes in GitHub Desktop.
   - Click on "Changes" in the left sidebar.
   - Write a commit message like "Completed Lab 2: Draw Something to the Screen".
   - Click "Commit to lab-6".
3. Push your changes to GitHub.
   - Click on "Push origin" in the top bar.
4. Create a pull request in GitHub
    - Go to your repository on GitHub.
    - Click on "Pull requests" in the top menu.
    - Click on "New pull request".
    - Select `lab-6` as the branch you want to merge into `main`.
    - Click "Create pull request".
    - Add a title and description, then click "Create pull request".
5. Let the instructor know that you have completed the lab by sending a message.

# Rubric

Total Points: 10

- Completed Challenge 1 - 2 points
- Completed Challenge 2 - 3 points
- Completed Challenge 3 - 3 points
- Completed Challenge 4 - 2 point
