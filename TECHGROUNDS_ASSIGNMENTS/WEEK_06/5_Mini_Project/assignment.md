# [5/ Mini_Project]

Now that you’ve encountered the basic puzzle pieces, it’s time to build something. Depending on how comfortable you are with Python, you can choose one of the following games to build:

- Number guessing (Beginner)
- Rock paper scissors (Intermediate)
- Tic-Tac-Toe (Hard)

## Key-terms

[Schrijf hier een lijst met belangrijke termen met eventueel een korte uitleg.]

## Assignment

 Number Guessing:

- Generate a random number between 1 and 100 (or any other range).
- The player guesses a number. For every wrong answer the player receives a clue.
- When the player guesses the right number, display a score.

 Rock Paper Scissors:

- The player plays against a computer opponent typing either a letter (rps) or an entire word (rock paper scissors) to play their move.
- Create a function that checks whether the move is valid or not.
- Create another function to create a computer move.
- Create another function to check who wins the round.
- Finally, create a function that keeps track of the score.
- The game should be played in a predetermined number of rounds.

 Tic-Tac-Toe:

- Generate a 3x3 board on the command line.
- This is a 2-player game, where one player inputs “X” and the other player inputs “O”.
- Bonus: create a single-player version that you can play against the computer.

### Used sources

[Plaats hier de bronnen die je hebt gebruikt.]

### Encountered problems

[Geef een korte beschrijving van de problemen waar je tegenaan bent gelopen met je gevonden oplossing.]

### Result

 Number Guessing:

- Generate a random number between 1 and 100 (or any other range).
- The player guesses a number. For every wrong answer the player receives a clue.
- When the player guesses the right number, display a score.

  Result Number Guessing:

  This script defines three functions:

- `generate_random_number()` generates a random number between 1 and 100.

- `give_clue(guess, secret_number)` gives a clue to the player based on their guess compared to the secret number.

- `play_game()` is the main function where the game logic resides. It generates a random number, prompts the player to guess, gives clues for incorrect guesses, and finally displays the score when the player guesses the right number.
  
  When you run this script, the player can guess numbers until they guess the correct one. For each wrong guess, they receive a clue. When they guess the correct number, their score is displayed.
  
  ```
  import random
  
  def generate_random_number():
    return random.randint(1, 100)
  
  def give_clue(guess, secret_number):
    if guess < secret_number:
        print("Too low! Try a higher number.")
    else:
        print("Too high! Try a lower number.")
  
  def play_game():
    secret_number = generate_random_number()
    attempts = 0
    while True:
        guess = int(input("Guess the number (between 1 and 100): "))
        attempts += 1
        if guess == secret_number:
            print("Congratulations! You guessed the number", secret_number, "correctly!")
            print("Your score is:", 100 - (attempts - 1) * 10)  # Score calculation
            break
        else:
            give_clue(guess, secret_number)
  
  if __name__ == "__main__":
    play_game()
  ```

 Rock Paper Scissors:

- The player plays against a computer opponent typing either a letter (rps) or an entire word (rock paper scissors) to play their move.
- Create a function that checks whether the move is valid or not.
- Create another function to create a computer move.
- Create another function to check who wins the round.
- Finally, create a function that keeps track of the score.
- The game should be played in a predetermined number of rounds.

  Result Rock/Paper/Scissors:

  This script defines several functions:

- `is_valid_move(move)`: checks whether the player's move is valid or not.

- `generate_computer_move()`: randomly generates a move for the computer.

- `determine_winner(player_move, computer_move)`: determines the winner of a round based on the player's and computer's moves.

- `play_game(rounds)`: orchestrates the game, keeping track of scores and playing the specified number of rounds.
  
  When you run this script, it prompts the player to enter their move (rock, paper, or scissors) for the specified number of rounds. After each round, it displays the computer's move and the result of the round (whether the player wins, loses, or it's a tie). Finally, it prints the final score.

```
import random

# Function to check if the move is valid
def is_valid_move(move):
    valid_moves = ['rock', 'paper', 'scissors']
    return move.lower() in valid_moves

# Function to generate a computer move
def generate_computer_move():
    return random.choice(['rock', 'paper', 'scissors'])

# Function to determine the winner of a round
def determine_winner(player_move, computer_move):
    if player_move == computer_move:
        return "It's a tie!"
    elif (player_move == 'rock' and computer_move == 'scissors') or \
         (player_move == 'paper' and computer_move == 'rock') or \
         (player_move == 'scissors' and computer_move == 'paper'):
        return "You win!"
    else:
        return "Computer wins!"

# Function to keep track of the score
def play_game(rounds):
    player_score = 0
    computer_score = 0

    for _ in range(rounds):
        player_move = input("Enter your move (rock, paper, scissors): ")
        while not is_valid_move(player_move):
            print("Invalid move! Please enter a valid move.")
            player_move = input("Enter your move (rock, paper, scissors): ")

        computer_move = generate_computer_move()
        print("Computer's move:", computer_move)

        result = determine_winner(player_move, computer_move)
        print(result)

        if result == "You win!":
            player_score += 1
        elif result == "Computer wins!":
            computer_score += 1

    print("\nFinal Score:")
    print("Player:", player_score)
    print("Computer:", computer_score)

if __name__ == "__main__":
    rounds = int(input("Enter the number of rounds you want to play: "))
    play_game(rounds)
```

 Tic-Tac-Toe:

- Generate a 3x3 board on the command line.
- This is a 2-player game, where one player inputs “X” and the other player inputs “O”.
- Bonus: create a single-player version that you can play against the computer.

  Result Tic-Tac-Toe:

  This script allows two players to play Tic-Tac-Toe in the command line. Players take turns entering row and column numbers to place their marks ('X' or 'O') on the board. The game continues until one player wins or the board is filled, resulting in a tie.

```
# Function to print the Tic-Tac-Toe board
def print_board(board):
    for row in board:
        print(" | ".join(row))
        print("-" * 9)

# Function to check if a player has won
def check_winner(board, player):
    for row in board:
        if all(cell == player for cell in row):
            return True
    for col in range(3):
        if all(board[row][col] == player for row in range(3)):
            return True
    if all(board[i][i] == player for i in range(3)) or \
       all(board[i][2-i] == player for i in range(3)):
        return True
    return False

# Function to check if the game is a tie
def check_tie(board):
    for row in board:
        for cell in row:
            if cell == ' ':
                return False
    return True

# Function to play Tic-Tac-Toe
def play_game():
    board = [[' ' for _ in range(3)] for _ in range(3)]
    current_player = 'X'
    while True:
        print_board(board)
        row = int(input(f"Player {current_player}, enter row (0, 1, or 2): "))
        col = int(input(f"Player {current_player}, enter column (0, 1, or 2): "))
        if board[row][col] == ' ':
            board[row][col] = current_player
            if check_winner(board, current_player):
                print_board(board)
                print(f"Player {current_player} wins!")
                break
            elif check_tie(board):
                print_board(board)
                print("It's a tie!")
                break
            current_player = 'O' if current_player == 'X' else 'X'
        else:
            print("That position is already taken. Try again.")

if __name__ == "__main__":
    play_game()
```