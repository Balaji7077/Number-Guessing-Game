# Number Guessing Game
In this project, we implement a Number Guessing Game where the system selects a random integer within a user-defined range, and the user has to guess the number in the minimum number of attempts. The goal is to minimize the number of guesses by intelligently narrowing down the guessing range.

# Click Here For Demo

  https://balaji7077.github.io/Number-Guessing-Game/

# Problem Analysis

## Game Explanation

The system selects a random integer within a given range (e.g., between 1 and 100). The user will attempt to guess the number, and the system provides feedback after each guess.

# Example 1:

Let's assume the range is from 1 to 100, and the number chosen by the system is 42.

1st Guess: The user guesses 50. The system responds, "Try Again! You guessed too high." 

2nd Guess: The user then guesses 25. The system responds, "Try Again! You guessed too small."

The guessing range now narrows down to 25 to 50.

3rd Guess: The user guesses 37. The system responds, "Try Again! You guessed too small."

The range narrows down further, and the user keeps guessing, following the same approach by halving the range.

Eventually, after several guesses, the user guesses 42 correctly, which is the correct number.

Total Guesses: 7

# Example 2:

Now, let’s say the range is 1 to 50, and the system selects 42.

1st Guess: The user guesses 25, which is too small.

2nd Guess: The user guesses 37, which is too small.

3rd Guess: The user guesses 43, which is too high.

Eventually, the user guesses 42 correctly.

Total Guesses: 6

# Minimum Number of Guesses

The minimum number of guesses required to find the number is based on the range. The formula to calculate the minimum number of guesses is:

#### Minimum number of guesses = log2(Upper bound – Lower bound + 1)

This formula works because the user is narrowing down the range by half with each guess (a technique known as binary search).

# Algorithm Overview

### Steps to Play the Game:

1.Input Range: The user inputs the lower and upper bounds for the range of numbers.

2.System Selects Number: The system randomly selects a number within the provided range.

3.Guessing Loop: The user makes guesses, and the system provides feedback:
If the guess is higher than the selected number, the system will prompt, "Try Again! You guessed too high."
If the guess is lower than the selected number, the system will prompt, "Try Again! You guessed too small."

4.Winning Condition: If the user guesses correctly, the system congratulates them.

5.Failure Condition: If the user doesn’t guess the number within the minimum number of guesses, the system will prompt, "Better Luck Next Time!"


# Implementation of the Algorithm

## Pseudocode:

1.Input the range (Lower Bound, Upper Bound).

2.Generate a random number between the range.

3.Start the guessing loop:

  * Calculate the minimum number of guesses using log2(upper bound - lower bound + 1).
  * Allow the user to make guesses.
  * Provide feedback: Too high, too low, or correct guess.


4.Exit conditions:

  * If the user guesses the number correctly, display a congratulatory message.
  * If the user fails to guess within the minimum guesses, prompt them with "Better Luck Next Time!"

# How to Run the Game

  * Clone the repository:

    git clone https://github.com/Balaji7077/Number-Guessing-Game.git

  * Navigate to the project directory:

    cd number-guessing-game

  * Run the  file:
      By clicking the run command in Vs code.
  * Follow the prompts and guess the number within the specified range!




