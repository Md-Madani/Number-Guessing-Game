import random
import time

def number_guessing_game():
    print("Welcome to the Number Guessing Game!")
    print("I have selected a number between 1 and 10. Try to guess it!")

    # Generate random number between 1 and 10
    number_to_guess = random.randint(1, 10)
    attempts = 0
    max_attempts = 3
    start_time = time.time()

    while attempts < max_attempts:
        try:
            guess = int(input(f"Attempt {attempts + 1}/{max_attempts} - Enter your guess: "))
            attempts += 1

            # Calculate the difference between guess and actual number
            difference = abs(number_to_guess - guess)

            # Provide feedback based on the guess's closeness to the target number
            if guess < number_to_guess:
                if difference > 10:
                    print("Too far low! Try again.")
                elif 5 < difference <= 10:
                    print("You're somewhat close, but still too low!")
                elif difference <= 2:
                    print("Almost there! You're very close!")
                else:
                    print("Getting warmer! But still a bit too low.")
            elif guess > number_to_guess:
                if difference > 10:
                    print("Too far high! Try again.")
                elif 5 < difference <= 10:
                    print("You're somewhat close, but still too high!")
                elif difference <= 2:
                    print("Almost there! You're very close!")
                else:
                    print("Getting warmer! But still a bit too high.")
            else:
                elapsed_time = time.time() - start_time
                print(f"Congratulations! You've guessed the correct number {number_to_guess} in {attempts} attempts and {elapsed_time:.2f} seconds.")
                break

        except ValueError:
            print("Invalid input! Please enter a valid number.")

    if guess != number_to_guess:
        print(f"Sorry, you've used all your attempts. The correct number was {number_to_guess}.")

# Run the game
if __name__ == "__main__":
    number_guessing_game()
