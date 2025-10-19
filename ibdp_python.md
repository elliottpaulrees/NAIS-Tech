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
        loop = True

        while loop == True:
    
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
                loop = False
                # Have a function call here to take you to your next function
                
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

Loops are a core part of coding and allow steps to be repeated efficiently, saving countless lines of code. We will examine two fundamental types: Count-Controlled and Condition-Controlled.

### Count-Controlled Loop Analysis

This loop is used when the number of repetitions is known before the loop starts. Analyse the code beloe and see if you can understand how it works.

```python
# Constants for the calculation
INITIAL_BALANCE = 1000.00
ANNUAL_RATE = 0.05 # 5% annual interest
NUM_YEARS = 5

balance = INITIAL_BALANCE

# Output using simple string concatenation
print("Starting balance: $" + str(balance))
print("-" * 30)

# The 'for' loop executes exactly NUM_YEARS (5) times.
for year in range(NUM_YEARS):
    # Calculate interest for the year
    interest = balance * ANNUAL_RATE
    balance += interest
    
    # Concatenating strings and converted numbers for output
    # Note: We round the balance when converting to a string to keep the output clean.
    output = "End of Year " + str(year + 1) + ": Balance = $" + str(round(balance, 2))
    print(output)

print("-" * 30)
print("Final balance after " + str(NUM_YEARS) + " years: $" + str(round(balance, 2)))
```

### Activity 1 - Using count controlled loops.
This is a question of probability. Write a function that rolls a dice an amount of times specified by the user and logs each fall. Calculate the likelihood of each number falling. 

The probability (or, more precisely, the empirical probability or relative frequency) of rolling a specific number is calculated as:

Probability (Number X) = (Count of X) / (Total Number of Rolls)

To express this as a percentage, you simply multiply the result by 100:

Percentage (Number X) = (Count of X / Total Number of Rolls) * 100
 
 
 
### Condition-Controlled Loop Analysis

This loop is used when the number of repetitions is unknown because it depends on an external condition (like a goal being reached or user input).


```python
# Constants for the calculation
INITIAL_BALANCE = 1000.00
ANNUAL_RATE = 0.05
GOAL_AMOUNT = 1500.00 # The loop must continue until this condition is met

balance = INITIAL_BALANCE
years = 0

# Output using simple string concatenation
print("Goal: Achieve a balance of $" + str(GOAL_AMOUNT))
print("-" * 30)

# The 'while' loop continues AS LONG AS the balance is below the goal.
while balance < GOAL_AMOUNT:
    # Increment the loop counter
    years += 1
    
    # Calculate interest
    interest = balance * ANNUAL_RATE
    balance += interest
    
    # Concatenating strings and converted numbers for output
    # The round() function is necessary to keep the monetary output clean.
    output = "Year " + str(years) + ": New balance = $" + str(round(balance, 2))
    print(output)

print("-" * 30)
# Final output condition depends on the loop exit state
print("Goal achieved in " + str(years) + " years! Final balance: $" + str(round(balance, 2)))
```


   
### Activity 2 - Use a condition controlled loop to create a game of Rockm Paper, Scissors!

Build a game of Rock, Paper, Scissors against the computer. The game continues until either the player or the computer wins 3 rounds. Display the score after each round. Each part of the program should be split into functions!




<hr>


# Lesson 4 - Work with 1D Arrays

In programming, an array (often called a list in Python) is a structure used to store a collection of related data items under a single variable name. These structures are crucial for organizing data and processing large amounts of information efficiently using loops.

## The Concept of a 1D Array

A one-dimensional (1D) array is a linear structure, like a single row or column. Each item in the array is located by its index (or position), which starts counting from zero (0).

### Example 1: Creating and Accessing a 1D Array

```python
# 1. Creating a 1D Array (List)
fruit_basket = ['Apple', 'Banana', 'Cherry', 'Date', 'Elderberry', 'Fig']

# 2. Finding the size (length) of the array
basket_size = len(fruit_basket)
print("The basket contains " + str(basket_size) + " items.") # Output: 6

# 3. Accessing items by index
print("The first fruit is: " + fruit_basket[0])  # Output: Apple (Index 0)
print("The third fruit is: " + fruit_basket[2])  # Output: Cherry

# 4. Accessing the last item (using negative indexing)
print("The last fruit is: " + fruit_basket[-1]) # Output: Fig

# 5. Modifying an item
fruit_basket[3] = 'Durian'
print("The item at index 3 is now: " + fruit_basket[3]) # Output: Durian
```



### Example 2: Looping Through a 1D Array

We use the skills learned in the previous lesson (loops) to process every item in the array. This is how we find totals, averages, or maximum values.

#### Looping by Value
This method is used when you only need to look at the value of each element.

```python
shopping_costs = [12.50, 4.99, 8.75, 22.00, 1.50]
total_cost = 0

print("--- Calculating Total Cost ---")
# The 'for' loop iterates directly over the values in the list.
for item_cost in shopping_costs:
    total_cost = total_cost + item_cost
    print("Adding cost: $" + str(item_cost) + " | Current Total: $" + str(round(total_cost, 2)))

print("\nFINAL TOTAL COST: $" + str(round(total_cost, 2)))
```
####  Looping by Index (Necessary for modification or parallel arrays)
This method is used when you need to know the index number (position) of the element you are processing.

```python
student_names = ["Alice", "Bob", "Charlie", "Diana"]

print("--- Listing Students by Number ---")
# We loop using 'range(len(array))' to generate the indices: 0, 1, 2, 3
for index in range(len(student_names)):
    # We use the index to access the value: student_names[index]
    student_number = index + 1
    
    output = "Student " + str(student_number) + " is " + student_names[index]
    print(output)
```


### Activity 2 - Analyzing Temperature Data with 1D Arrays

This activity combines file handling, count-controlled loops, and list manipulation. The file daily_temperatures.txt contains one year of daily temperature readings, one per line. We will use a one-dimensional array (list) to store and process this data.

Task Requirements:

1. File Input to Array: Read all the numerical data from the daily_temperatures.txt file and store it in a single Python list (1D array). Remember to handle the conversion of text strings to numbers!

2. Yearly Statistics: Using loops, iterate through the full array to calculate and display the following for the entire year:

- The Highest recorded daily temperature.

- The Lowest recorded daily temperature.

- The Average daily temperature for the entire year.

3. Monthly Averages List: Create a new, separate list that stores the average temperature for each of the 12 months.

Hint: For simplicity, assume the data is exactly 365 days and that the first 30 days are Month 1, the next 30 days are Month 2, and so on. (You will need to adjust your loop structure to process the data in chunks).



<hr>


# Lesson 5 - Two-Dimensional Arrays (Nested Lists)

A two-dimensional (2D) array, often called a nested list in Python, is a list of lists. It is the perfect structure for representing data that is organized in rows and columns, such much as tables, grids, or matrices.

In a 2D array, data is addressed using two indices:

1. The first index specifies the Row.

2. The second index specifies the Column.


```python
### Example 1: Creating and Accessing a 2D Array
# A 2D array representing student data (rows) and their scores (columns)
student_scores = [
    [85, 78, 92],  # Row 0: Student 1 scores
    [90, 82, 87],  # Row 1: Student 2 scores
    [75, 85, 80]   # Row 2: Student 3 scores
]

# 1. Accessing a specific element (Row 1, Column 2)
# Student 2's History score (87)
score = student_scores[1][2]
print("Student 2's History score is: " + str(score))

# 2. Accessing an entire row (Row 0)
# All scores for Student 1
student_1_scores = student_scores[0]
print("Student 1's scores: " + str(student_1_scores))

# 3. Finding the dimensions
num_rows = len(student_scores)
num_cols = len(student_scores[0]) # Length of the first inner list
print("The array has " + str(num_rows) + " rows and " + str(num_cols) + " columns.")
```

Example 2: Looping Through a 2D Array (Nested Loops)

To process every item in a 2D array, you must use nested loops:

1. Outer Loop: Iterates through the rows.

2. Inner Loop: Iterates through the columns (elements within the current row).

```python
student_scores = [
    [85, 78, 92],
    [90, 82, 87],
    [75, 85, 80]
]

# Outer loop iterates through the rows (i = 0, 1, 2)
for i in range(len(student_scores)):
    print("\n--- Processing Student " + str(i + 1) + " ---")
    
    # Inner loop iterates through the columns (j = 0, 1, 2) of the current row
    for j in range(len(student_scores[i])):
        score = student_scores[i][j]
        output = "Score at Row " + str(i) + ", Column " + str(j) + " is: " + str(score)
        print(output)
```


### Activity: Analyzing Student Grades with 2D Arrays

This activity requires you to read a file containing structured data and use nested lists and loops to perform complex analysis. The file student_grades.txt contains 10 rows, where each row represents a student and contains five comma-separated scores for five different subjects.

#### Task Requirements:

1. File Input to 2D Array:

    - Read the data from student_grades.txt.

    - Create a 2D Array (list of lists) where each inner list contains the five numerical scores for one student.

    - Hint: You will need to process each line, split it by the comma separator, and convert each resulting string into an integer.

2. Calculate Student Subject Grades:

    - Create a function (or a section of code) that loops through the 2D array.

    - For each student's score in each subject, determine and print their letter grade (A, B, C, D, or F) using the following scale:

        - Over 80: A
        - 70-79: B
        - 60-69: C
        - 50-59: D
        - Less than 50: F


3. Calculate Student Average Scores:

    - Using the nested loops, calculate the average score for each student across all five subjects.

    - Store these 10 average scores in a separate 1D list of averages.

    - Print each student's final average score clearly.


<hr>


# Lesson 6 - Searching and Sorting Algorithms

After learning to store data efficiently in 1D and 2D arrays, the next challenge is processing that data in the most effective way. Searching and Sorting are the two most fundamental tasks in computer science, and they allow us to explore how different algorithms can solve the same problem with vastly different speeds.

## Part 1: Understanding Searching Algorithms

Searching is the process of finding a specific item within a data structure. We will analyze two common methods.

### Linear Search (Sequential Search)

The Linear Search algorithm checks every element in the list sequentially (one by one) until the target item is found or the end of the list is reached.

- When to use: When the list is small or unsorted.
- Efficiency: Slow, as in the worst case, the computer must check $N$ items (where $N$ is the size of the list).

Steps:
1.  Start a loop to check every position (index) in the list, from the first position to the last position.
2.  Inside the loop, compare the number at the current position with the `target_value` you are looking for.
3.  IF they are the same number, stop the loop and give back the current position (index).
4.  IF NOT, the loop continues to the next position.
5.  If the loop finishes checking every position and the number was not found, give back the number **-1** (which means the search failed).

### Binary Search

The Binary Search algorithm is significantly faster but has one strict requirement: the list must be sorted before searching can begin. It works by repeatedly dividing the search interval in half.

- When to use: When the list is large and sorted.
- Efficiency: Very fast. It quickly eliminates half the remaining items with each step.


Steps:
1.  Start Pointers: Create a variable called `low` and set its value to the first position of the list (index 0).
2.  Create a second variable called `high` and set its value to the last position (index) of the list.
3.  Search Loop: Start a loop that **continues to run** as long as the `low` number is smaller than or equal to the `high` number.
4.  Find Middle: Inside the loop, calculate the position of the **middle number** between `low` and `high`.
5.  Check Middle: Now, compare the number at the middle position with the `target_value` you want to find.
6.  IF Found: IF the middle number is the same as the `target_value`, stop the search immediately and give back the middle position.
7.  IF Too Small: ELSE IF the middle number is smaller than the `target_value`, throw away the lower half of the list. Change the `low` variable to be one position higher than the middle position.
8.  IF Too Big: ELSE (if the middle number is bigger than the `target_value`), throw away the upper half of the list. Change the `high` variable to be one position lower than the middle position.
9.  End Search: If the loop finishes without finding the number, give back the number **-1** (meaning the search failed).

## Part 2: Understanding Sorting Algorithms
Sorting is the process of arranging a list of items into a specific order (ascending or descending).

### Bubble Sort
The Bubble Sort algorithm is the simplest sorting method to understand. It repeatedly steps through the list, compares adjacent elements, and swaps them if they are in the wrong order. This process "bubbles" the largest elements to the end of the list.

- When to use: Only for teaching purposes. It is never used in real-world applications.
- Efficiency: Extremely slow O(n<sup>2</sup>), especially on large lists.

Steps:
1.  Outer Loop (Passes):Start the main loop that controls how many times you check the list. This loop repeats almost the total length of the list.
2.  Inner Loop (Comparisons): Inside the first loop, start a second, nested loop. This loop checks numbers from the very start of the list up to the end of the **unsorted part**.
3.  Compare: Look at two numbers that are right next to each other: the current number (j) and the number after it (j + 1).
4.  IF Wrong Order: IF the current number (j) is bigger than the next number (j + 1), it means they are in the wrong order.
5.  Swap: Swap the positions of these two numbers.
6.  Repeat: The inner loop repeats until the largest unsorted number has moved ("bubbled up") to its correct place at the end of the unsorted section.
7.  Outer Loop Repeats: The outer loop repeats until the entire list is sorted.

### Selection Sort

The Selection Sort algorithm improves slightly on Bubble Sort by minimizing the number of swaps. In each pass, it finds the smallest element from the unsorted portion of the list and swaps it with the element at the current position.

- Concept: It "selects" the smallest remaining item and moves it to its correct sorted position.
- Efficiency: Also slow ($O(n^2)$), similar to Bubble Sort, but typically performs fewer data moves (swaps).


Steps:
1.  Outer Loop: Start a loop that goes through the list from the first position (index 0) almost to the end. This loop marks the start of the unsorted part.
2.  Find the Smallest: Set a variable called `min_index` equal to the index of the number at the current position (from the outer loop). Assume this is the smallest number for now.
3.  Inner Loop: Start a second, inner loop that checks **all the positions after the current position (i.e., the rest of the unsorted part).
4.  Compare and Update: IF the number at the current inner loop position is smaller than the number at the current `min_index`, then change `min_index` to the inner loop's position.
5.  Smallest Found: After the inner loop finishes, `min_index` now holds the position of the true smallest number in the unsorted part.
6.  Swap: Swap the number at the current position (from the outer loop) with the number at the `min_index` position.
7.  Repeat: The outer loop repeats, and the sorted section of the list grows by one number.


## Part 3: Implementing the Algorithms
For each of the discussed sorting and searching algorithms, create a function which takes in a 1D array and carries out the required algorithm on the list. 
