# Number-Guessing
import random

def number_guessing_game():
    print("🎯 Welcome to the Number Guessing Game!")
    lower_bound = 1
    upper_bound = 100
    number_to_guess = random.randint(lower_bound, upper_bound)
    attempts = 0

    while True:
        try:
            guess = int(input(f"Guess a number between {lower_bound} and {upper_bound}: "))
            attempts += 1

            if guess < lower_bound or guess > upper_bound:
                print("⚠️ Your guess is out of bounds. Try again.")
            elif guess < number_to_guess:
                print("🔼 Too low! Try again.")
            elif guess > number_to_guess:
                print("🔽 Too high! Try again.")
            else:
                print(f"✅ Congratulations! You guessed it in {attempts} tries.")
                break
        except ValueError:
            print("❌ Invalid input. Please enter a number.")

# Run the game
number_guessing_game()
