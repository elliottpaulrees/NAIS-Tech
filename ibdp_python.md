---
title: Linear and Functional Programming
layout: page
description: About
bodyClass: page-about
---

# Lesson 0 - Setting up your development environment

## Python Interpreter
An interpreter is a translator which can be used to turn your python code into machine code which the computer can run.

- Download the python intepreter from the following link: https://python.org

## Integrated Development Environment
An IDE, or Integrated Development Environment, is a software application that brings together all the essential tools a programmer needs to write, test, and debug code — all in one place.

- Download Visual Studio Code from the following URL: https://code.visualstudio.com/

## Storing and Sharing Code
GitHub is a web-based platform that helps developers store, manage, and collaborate on code using a system called Git — a version control tool that tracks changes to files over time. It is an industry expectation that you know how to use github, which is where this very website is stored.

- Create a github account at: https://github.com/
- Download Github desktop at: https://github.com/apps/desktop


Use the following URL for support: https://www.geeksforgeeks.org/python/python-cheat-sheet/

<hr>

# Lesson 1 - Input, Output, Variables & Decisions

Build a "Digital ID Card" program that asks for name, year, date of birth, whether they can go offsite and account balance and then prints a formatted summary.

### Activity 1: Add the following functionality to your program should:
- Inform the user what you want them to enter.
- Collect data from the user in the correct data type
- Output the data to the console in a formatted way using the print command.
- Write the data to a .txt file for future processing. You may want to use the following website for support: <a href="https://www.w3schools.com/python/python_file_handling.asp">https://www.w3schools.com/python/python_file_handling.asp</a>

#### Example
```python
# You can create a new string form your collected data to write to the text file. You just need to ensure all data are strings.
NewString = "name: " +str(name) + " " + "Year Level: " +str(level) + " " + "Allowed offsite: " +str(offsite) + " " + "Account balance: " +str(balance) 

f = open("demofile.txt", "a")
f.write(NewString + "\n") #the \n adds a new line at the end of the text file so the next write will be one line down.
f.close()
```

Add a screenshot of your code to formative.

### Activity 2: Validation can be used to ensure the user is entering accurate data.

A type check can be used to check the data type of data entered. If its not what we expect, we can reject the input.

```python
balance = 58.7
if isinstance(balance, float):
    print("Balance is a float.")
```


- Validate the user input using a type check (see seen above in the example)
- Validate the user year level and account balance inputs using a range check (check if data is more than or less then set values).
- Validate the user input using a presence check (if input == "":).
- Validate the user date of birth using a format check (You can check if the / is in the data with if DoB[2]=="/":). 

<hr>

# Lesson 2: Using Procedures, decisions and global variables

Today, we're diving back into the power of programmatic decision-making. We'll move beyond simple menus and explore how to control your program's flow using a full range of comparison operators (<, >, ==, !=) and boolean logic (and, or, not).

### Activity 1
Your task is to analyze the code snippet below. Run it several times with different inputs to reverse-engineer its logic. How does it use these operators to change the program's state and output? Your goal is to understand and explain the precise conditions that trigger each outcome.

```python
# Global variables for the player's state
player_health = 50
player_has_key = False
attempts = 0

def challenge_room():
    global player_health, player_has_key, attempts
    
    print("\nYou are in a challenge room.")
    print(f"Health: {player_health} | Key: {player_has_key} | Attempts: {attempts}")
    
    print("\nA gate blocks your path. It needs a code (1-10).")
    
    try:
        guess = int(input("Enter your guess: "))
        attempts += 1  # This will increase each time they try
        
        # Using multiple comparison and boolean operators
        if guess != 7 and guess < 5:  # Not equal AND less than
            player_health -= 10
            print("A trap triggers! -10 health.")
            
        elif guess > 10 or guess < 1:  # Greater than OR less than
            print("The number must be between 1-10! Waste of an attempt.")
            
        elif guess == 7 and not player_has_key:  # Equal AND NOT
            player_has_key = True
            print("The gate opens! You found the key!")
            
        elif player_has_key and attempts >= 2:  # AND with greater/equal
            print("You already have the key! Just go through the gate.")
            
        else:
            print("Nothing happens. Try again.")
            
    except ValueError:
        print("That's not a valid number!")  # != int


# Start of program
challenge_room()

```

### Activity 2

Continue developing the above program to build your own interactive adventure!

<hr>


# Lesson 3 - Using Loops


### Activity 1
 This is a question of probability. Write a function that rolls a dice an amount of times specified by the user and logs each fall. Calculate the likelihood of each number falling. 

The probability (or, more precisely, the empirical probability or relative frequency) of rolling a specific number is calculated as:

Probability (Number X) = (Count of X) / (Total Number of Rolls)

To express this as a percentage, you simply multiply the result by 100:

Percentage (Number X) = (Count of X / Total Number of Rolls) * 100

### Activity 2

Build a game of Rock, Paper, Scissors against the computer. The game continues until either the player or the computer wins 3 rounds. Display the score after each round. Each part of the program should be split into functions!
