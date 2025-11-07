# Rock, Paper, Scissors: Debugging Practice

Welcome to your staged debugging task! There are three code sections and the main game loop. Section 1 is modelled for you; you will debug Sections 2 and 3 before the full game works.

***

## SECTION 1 – User Input & Validation (Completed Example)

```python
# SECTION 1 – User Input & Validation

def get_user_choice():
    user_choice = input("Choose rock, paper, or scissors: ").lower()
    if user_choice not in ["rock", "paper", "scissors"]:
        print("Invalid choice! Please try again.")
        print("You entered: " + user_choice + " but I need one of the three options.")
        attempts = 1
        print("This was attempt number: " + str(attempts))  # FIX: Convert int to str
        return get_user_choice()
    print("Valid choice! You chose: " + user_choice)
    return user_choice
```

***

## MAIN GAME LOOP

This block is the structure for your game. **Some calls are commented out until you finish those functions.**

```python
# === MAIN GAME LOOP ===

def play_game():
    user_choice = get_user_choice()
    # computer_choice = get_computer_choice()  # Uncomment after you complete Section 2
    # result = determine_winner(user_choice, computer_choice)  # Uncomment after Section 2
    # update_score(result)  # Uncomment after Section 3
    # display_score()       # Uncomment after Section 3

play_game()
```

***

## SECTION 2 – Computer Choice & Winner Logic
**TASK:** Copy this code below Section 1. Debug **all four error types** in this section.

```python
# SECTION 2 – Computer Choice & Winner Logic

import random

def get_computer_choice()  # SYNTAX ERROR: missing colon
computer_choice = random.choice(["rock", "paper", "scissors"])  # INDENTATION ERROR
    return computer_choice

def determine_winner(user_choice, computer_choice):
    print("You chose: " + user_choice)
    print("Computer chose: " + computer_choice)
    rounds_played = 1
    print("Round " + rounds_played + " results:")  # TYPE ERROR: can't concatenate str/int

    if user_choice == computer_choice:
        print("It's a tie!")
        winner = "tie"
    elif user_choice == "rock" and computer_choice == "scissors":
        print("You win!")
        winner = "win"
    elif user_choice == "paper" and computer_choice == "rock":
        print("You win!")
        winner = "win"
    elif user_choice == "scissors" and computer_choice == "paper":
        print("You win!")
        winner = "win"
    else:
        print("You lose!")
        winner = "lose"
    return resuLt  # NAME ERROR: should be 'winner'
```

***

## SECTION 3 – Score Tracking & Final Output
**TASK:** Copy this code below Section 2. Debug **all four error types** in this section.

```python
# SECTION 3 – Score Tracking & Final Output

user_score = 0
computer_score = 0

def update_score(result)  # SYNTAX ERROR: missing colon
global user_score  # INDENTATION ERROR: Not in function
    global computer_score
    if result == "win":
        user_score = user_score + 1
    elif result == "lose":
        computer_score = computer_score + 1
    elif result == "tie":
        pass
    return user_score, computer_score

def display_score():
    total_rounds = user_score + computer_score
    print("=== GAME STATISTICS ===")
    print("Total rounds played: " + total_rounds)  # TYPE ERROR: can't concatenate str/int
    print("Your score: " + str(user_score))
    print("Computer's score: " + str(comp_score))  # NAME ERROR: should be 'computer_score'
    print("=======================")
```

***

## How to Complete the Lesson

1. **Start with Section 1** – Teacher models fixing errors
2. **Work in pairs on Section 2** – Debug and then uncomment those function calls in the main loop
3. **Work independently on Section 3** – Debug and then uncomment the score/display calls

***

## Error Types You'll See

- **SyntaxError**: e.g. missing colons, misplaced brackets
- **IndentationError**: blocks not properly indented in functions
- **TypeError**: e.g. concatenating string with integer without conversion
- **NameError**: variable names spelled/used incorrectly

***

**Run your code, fix all errors, and check with your teacher when it's working end-to-end!**