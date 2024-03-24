# Task-4-Python
import random

def play_rock_paper_scissors():
  """
  Plays a single round of Rock-Paper-Scissors against the computer.
  """
  # User input validation loop
  while True:
    user_choice = input("Choose rock, paper, or scissors (r/p/s): ").lower()
    if user_choice not in ['r', 'p', 's']:
      print("Invalid choice. Please enter 'r' for rock, 'p' for paper, or 's' for scissors.")
      continue
    break

  # Generate computer's choice
  computer_choice = random.choice(['rock', 'paper', 'scissors'])

  # Determine winner
  if user_choice == computer_choice:
    print("It's a tie!")
  elif (user_choice == 'r' and computer_choice == 'scissors') or \
       (user_choice == 'p' and computer_choice == 'rock') or \
       (user_choice == 's' and computer_choice == 'paper'):
    print("You win!")
  else:
    print("You lose!")

  # Display choices
  print(f"You chose: {user_choice.upper()}")
  print(f"Computer chose: {computer_choice.upper()}")

# Play again loop
while True:
  play_rock_paper_scissors()
  play_again = input("Do you want to play again? (y/n): ").lower()
  if play_again != 'y':
    break

print("Thanks for playing!")
