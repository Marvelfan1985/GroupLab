# GroupLab

## Roles:
#### Designing the Chart: Shahriyar Danish

#### Working on Creating GitHub: Sean Wilkinson and Prabhjot Kaur

#### Creating the Script: Deepak Kumar

## Instructions to our game:

##### 1. When you're here 


## Code for our game


```
#!/usr/bin/env python3

import random
import os
import time

# Clear the console screen
def clear():
    os.system('clear')

# Show the game instructions
def rockpaperscissors_instructions():
    print("Instructions for Rock-Paper-Scissors: ")
    print("Rock crushes Scissors")
    print("Scissors cuts Paper")
    print("Paper covers Rock")

# Play a round of Rock-Paper-Scissors
def rockpaperscissors():
    options = ["rock", "paper", "scissors"]
    while True:
        # Get the player's move
        move = input("Enter your move: ")
        if move not in options:
            print("Invalid move. Try again.")
            continue

        # Generate the computer's move
        print("Computer is  making its move...")
        time.sleep(2)
        computer_option = random.choice(options)
        print("Computer chooses:", computer_option)

        # Determine the winner
        if computer_option == move:
            print("Match ties")
        elif (computer_option == "rock" and move == "scissors" or
              computer_option == "paper" and move == "rock" or
              computer_option == "scissors" and move == "paper"):
            print("Computer wins")
        else:
            print("You win")

        # Ask if the player wants to play again
        play_again = input("Play again? (y/n): ")
        if play_again.lower() != "y":
            break

    print("Thank you for playing the game...")

# Get the player's name
name = input("Please enter your name to start: ")

# The GAME LOOP
while True:

    # The Game Menu
    print("Enter A to Play Rock-Paper-Scissors")
    print("Enter B to quit")
    print("Enter C to read instructions")

    # Try block to handle the player choice 
    try:
        choice = input("Enter your choice: ").lower()
    except ValueError:
        clear()
        print("Invalid choice.")
        continue

    # Play the traditional version of the game
    if choice == "a":
        clear()
        print("Let's play the game  Rock-Paper-Scissors, {}!".format(name))
        rockpaperscissors()

    # Quit the GAME LOOP 	
    elif choice == "b":
        break

    elif choice == "c":
        clear()
        rockpaperscissors_instructions()

    # Other invalid input
    else:
        clear()
        print("Your choice is invalid. Please enter A, B, or C.")

```




## Goal:

###### This is what is written in the GroupLab's instructions

###### "You work for a private software company called Games4You with 3-4 employees in the IT team. Each member in the IT department has different roles. There is one project manager/release coordinator, one developer and one QA tester. Your company wants to develop a simple web app of the famous “Rock, Paper Scissors” game to sell to other companies. The organizations are looking to buy this web app asap to promote team building within their companies. Your goal is to follow the Agile SDLC in order to build a quality game and then release it to those organizations within a timely manner. Follow the agile template below in order to successfully deploy your game to Production."
