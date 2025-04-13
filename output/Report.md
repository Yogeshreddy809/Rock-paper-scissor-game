# Rock-Paper-Scissors Game Report

## Implementation Details

The Rock-Paper-scissors game was implemented in Python with the following features:

1. **User Input Handling**
   - Accepts user input for rock, paper, or scissors
   - Validates input to ensure it's one of the valid options
   - Provides a way to quit the game

2. **Computer Selection**
   - Uses Python's `random` module to generate random choices
   - Equally likely to choose rock, paper, or scissors

3. **Game Logic**
   - Implements standard rock-paper-scissors rules:
     - Rock beats scissors
     - Scissors beat paper
     - Paper beats rock
   - Handles tie scenarios

4. **Score Tracking**
   - Maintains scores for both user and computer
   - Displays current score before each round
   - Shows final score when game ends

5. **User Interface**
   - Provides clear instructions at the start
   - Shows both player and computer choices
   - Clearly displays the result of each round
   - Offers option to play again after each round

## How to Run the Game

1. Ensure you have Python installed (Python 3.6 or higher recommended)
2. Clone the repository
3. Run the game with: `python game.py`

## Future Enhancements

1. Graphical user interface (GUI) using Tkinter or Pygame
2. Multiplayer functionality over network
3. Additional game modes (best of 3, tournament style)
4. Statistics tracking (win rates for each choice)
