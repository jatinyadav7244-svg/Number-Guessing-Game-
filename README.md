 import random

def number_guessing_game():
    print("Welcome to the Number Guessing Game!")
    secret = random.randint(1, 100)
    attempts = 0

    while True:
        try:
            guess = int(input("Enter your guess (1–100): "))
            attempts += 1

            if guess < secret:
                print("Too low. Try again.")
            elif guess > secret:
                print("Too high. Try again.")
            else:
                print(f"Correct! You guessed the number in {attempts} attempts.")
                break

        except ValueError:
            print("Invalid input. Enter a number only.")

number_guessing_game()
