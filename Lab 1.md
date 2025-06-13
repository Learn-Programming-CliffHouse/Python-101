# Lab 1: Project Setup & Python Basics

## Learning Objectives

- Get all necessary tools that you'll need for the rest of the semester installed
- Setup a python virtual environment
- Review python syntax and how to use some of the basic functions
- Push your repository to git for grading

## Setup

This lab is intended to be done with the professor present so that you can be introduced to all of the tools you'll be using for the rest of the semester.

### Git, Github, and Github Desktop

These three things often get confused because of their annoyingly similar names, but they're all pretty straightforward.

Git is a command line tool which is a version control system that allows you to make a local repository that tracks changes to your code.

Github is a cloud-based hosting service for git repositories that allow you to upload your code and access it from anywhere. We'll be using these two things together to track your changes and allow the professor to grade your work.

Github desktop is a GUI for git that makes it easier to use for beginners. It's made by the same people who made Github - hence the name.

- Create a github account if you don't have one already
- Message the professor your github username so I can add you to the class organization

### Software

- Install the latest python version from the [python website](https://www.python.org/downloads/)
- Install VS Code from the [VS Code website](https://code.visualstudio.com/download)
- Install git from the [git website](https://git-scm.com/downloads)
- Install github desktop from the [github desktop website](https://desktop.github.com/)

### Make a new git repository

- In github create a new repository and name it python-101. This is where you'll be putting all of your work for the semester.
- On your local machine clone that repository using github desktop.
- Open that repository in VS code - I believe that github desktop has a button to do this.
- In the repository, create a new file called README.md. This file is a markdown file that will be displayed on the github repository page. In this file write a short introduction about yourself and one fun fact about yourself.
- Create a file called .gitignore. This file is a text file that tells git which files it should NEVER track. Create a file called .gitignore and add the following lines to it:
  - venv/
  - **pycache**/
- Commit your changes.
- Push your changes to github.
- Go to the github repository page and verify that your README.md file is displayed.

### Virtual Environments

When using python, it's important to keep your project's dependencies separate from other projects. This is where virtual environments come in. A virtual environment is a self-contained directory tree that contains a Python installation for a particular version of Python.

- Create a new virtual environment using the following command:
  - `python -m venv venv`
- Activate the virtual environment using the following command:
  - `venv/bin/Activate`

## Lab 1 Code

Create a new branch in github desktop called `lab-1`

Create a new file called `lab1.py`

Complete the following excersizes that are intended to have you get used to the python syntax.

## 🔹 Challenge 1: Print Your Name

**Task:**  
Write a Python script that prints your full name to the console.

**Example Output:**

```
Riya Milan
```

---

## 🔹 Challenge 2: Temperature Converter

**Task:**  
Create a function that convert a temperature from Celsius to Fahrenheit. use the function to convert the temperature 37 degrees Celsius to Fahrenheit. Print the input temperature and the output temperature.

**Formula:** `F = (C × 9/5) + 32`

## 🔹 Challenge 3: FizzBuzz

**Task:**  
Print the numbers from 1 to 20.

- If a number is divisible by 3, print `"Fizz"`
- If a number is divisible by 5, print `"Buzz"`
- If divisible by both 3 and 5, print `"FizzBuzz"`
- Otherwise, print the number

**Expected Output Example:**

```
1
2
Fizz
4
Buzz
Fizz
7
8
Fizz
Buzz
11
Fizz
13
14
FizzBuzz
```

---

## 🔸 Challenge 4: Word Frequency Counter

### 📝 Task:

Write a program that takes a sentence as input and counts how many times each **unique word** appears in it.

### ✅ Requirements:

- Ask the user to enter a sentence.
- Convert the sentence to lowercase so that the word count is case-insensitive.
- Remove any punctuation (e.g., `. , ! ?`) so words are clean.
- Split the sentence into words.
- Count how many times each word appears using only lists and `for` loops (do **not** use a dictionary).
- Print each unique word along with its count.

### 🧠 Bonus:

- Sort the output alphabetically by the word before printing.

---

## 🔸 Challenge 5: Build a Simple Bank Account Class

**Concepts Used:** Classes, attributes, methods, basic arithmetic, `__init__`

### 📝 Task:

Create a class called `BankAccount` that simulates a basic bank account.

---

### ✅ Requirements:

1. The class should be initialized with:

   - The account owner's name
   - An optional starting balance (default to 0)

2. The class should have the following methods:

   - `deposit(amount)` → Adds money to the account
   - `withdraw(amount)` → Subtracts money if sufficient funds are available
   - `display_balance()` → Prints the current balance
   - `__str__()` → Returns a string representation like:  
     `"Account owner: Alice | Balance: $200"`

3. Handle edge cases like:
   - Depositing or withdrawing negative amounts
   - Withdrawing more than the available balance

---

### 🧪 Example:

```python
account = BankAccount("Alice", 100)
account.deposit(50)
account.withdraw(30)
account.display_balance()

print(account)
```

Output:

```
Current balance: $120
Account owner: Alice | Balance: $120
```

# Submitting Assignment

You're done! Congrats! This is going to be one of the longest labs you work on and probably one where you learn the most. To submit, push your lab-1 branch to github and open a PR request. Add the professor as a reviewer and then let them know you are ready for grading.

1. Save your work.
2. Commit your changes in GitHub Desktop.
   - Click on "Changes" in the left sidebar.
   - Write a commit message like "Completed Lab 2: Draw Something to the Screen".
   - Click "Commit to lab-1".
3. Push your changes to GitHub.
   - Click on "Push origin" in the top bar.
4. Create a pull request in GitHub
    - Go to your repository on GitHub.
    - Click on "Pull requests" in the top menu.
    - Click on "New pull request".
    - Select `lab-1` as the branch you want to merge into `main`.
    - Click "Create pull request".
    - Add a title and description, then click "Create pull request".
5. Let the instructor know that you have completed the lab by sending a message.

# Rubric

Total Points: 10

- Correctly submitted the assignment using a lab-1 branch and opening a pull request on github - 1 point
- Created a README.md file with some information about themself - 1 point
- Task 1 - 1 point
- Task 2 - 1 point
- Task 3 - 2 points
- Task 4 - 2 points
- Task 5 - 2 points
