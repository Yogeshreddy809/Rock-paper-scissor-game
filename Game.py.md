import random

def determine_winner(user_choice, computer_choice):
    if user_choice == computer_choice:
        return "tie"
    elif (user_choice == "rock" and computer_choice == "scissors") or \
         (user_choice == "scissors" and computer_choice == "paper") or \
         (user_choice == "paper" and computer_choice == "rock"):
        return "user"
    else:
        return "computer"

def play_game():
    user_score = 0
    computer_score = 0
    
    print("Welcome to Rock-Paper-Scissors Game!")
    print("Instructions:")
    print("- Choose rock, paper, or scissors")
    print("- Rock beats scissors")
    print("- Scissors beat paper")
    print("- Paper beats rock")
    print("- Type 'quit' to exit the game\n")
    
    while True:
        print(f"\nCurrent Score - You: {user_score} | Computer: {computer_score}")
        user_choice = input("Enter your choice (rock/paper/scissors): ").lower()
        
        if user_choice == "quit":
            print("\nFinal Score:")
            print(f"You: {user_score} | Computer: {computer_score}")
            print("Thanks for playing! Goodbye!")
            break
            
        if user_choice not in ["rock", "paper", "scissors"]:
            print("Invalid choice. Please try again.")
            continue
            
        computer_choice = random.choice(["rock", "paper", "scissors"])
        print(f"\nYou chose: {user_choice}")
        print(f"Computer chose: {computer_choice}")
        
        result = determine_winner(user_choice, computer_choice)
        
        if result == "tie":
            print("It's a tie!")
        elif result == "user":
            print("You win!")
            user_score += 1
        else:
            print("Computer wins!")
            computer_score += 1
            
        play_again = input("\nPlay again? (yes/no): ").lower()
        if play_again != "yes":
            print("\nFinal Score:")
            print(f"You: {user_score} | Computer: {computer_score}")
            print("Thanks for playing! Goodbye!")
            break

if __name__ == "__main__":
    play_game()
