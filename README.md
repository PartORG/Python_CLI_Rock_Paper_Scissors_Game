# Rock-Paper-Scissors Game CLI

Play a classic game of Rock-Paper-Scissors directly from your terminal with this simple Python script!

[![Python](https://img.shields.io/badge/python-3.6%2B-blue.svg)] [![License](https://img.shields.io/badge/license-MIT-green.svg)] [![GitHub stars](https://img.shields.io/github/stars/PartORG/Python_CLI_Rock_Paper_Scissors_Game?style=social)] [![GitHub forks](https://img.shields.io/github/forks/PartORG/Python_CLI_Rock_Paper_Scissors_Game?style=social)]

## Introduction

This project is a straightforward implementation of the classic Rock-Paper-Scissors game in Python. It provides a simple and fun way to play against the computer directly from your terminal.

The primary workflow involves running the script, making your move, and seeing the result. The main advantages include its simplicity, ease of use, and the ability to play without any additional setup or dependencies.

## Features

- **Simple CLI Interface**: Play the game directly in your terminal.
- **No Dependencies**: No external libraries required.
- **Easy to Use**: Just run the script and follow the on-screen instructions.

## How It Works

The game is implemented as a Python script (`main.py`). The user inputs their move (rock, paper, or scissors), and the script determines the winner based on the classic rules of Rock-Paper-Scissors.

Here's a simplified version of how the script works:

```python
import random

def get_user_choice():
    while True:
        choice = input("Enter your move (rock, paper, scissors): ").lower()
        if choice in ['rock', 'paper', 'scissors']:
            return choice
        else:
            print("Invalid move. Please try again.")

def get_computer_choice():
    return random.choice(['rock', 'paper', 'scissors'])

def determine_winner(user_choice, computer_choice):
    if user_choice == computer_choice:
        return "It's a tie!"
    elif (user_choice == 'rock' and computer_choice == 'scissors') or \
         (user_choice == 'scissors' and computer_choice == 'paper') or \
         (user_choice == 'paper' and computer_choice == 'rock'):
        return "You win!"
    else:
        return "Computer wins!"

def main():
    print("Welcome to Rock-Paper-Scissors!")
    user_choice = get_user_choice()
    computer_choice = get_computer_choice()
    print(f"You chose: {user_choice}")
    print(f"Computer chose: {computer_choice}")
    print(determine_winner(user_choice, computer_choice))

if __name__ == "__main__":
    main()
```

## Technology Stack

| Technology | Purpose |
|------------|---------|
| Python     | The programming language used to implement the game. |

## Requirements

- Python 3.6 or later

## Installation

To play the game, simply run the script:

```sh
python main.py
```

## Usage

1. Run the script:
   ```sh
   python main.py
   ```
2. Enter your move when prompted (rock, paper, or scissors).
3. See the result of the game.

## Project Structure

```
.
├── README.md
└── main.py
```

- `README.md`: This file you're reading!
- `main.py`: The Python script that implements the game.

## Development

No specific development workflow is provided as this is a simple script. Feel free to modify and extend it as needed!

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

Feel free to contribute by submitting issues or pull requests!