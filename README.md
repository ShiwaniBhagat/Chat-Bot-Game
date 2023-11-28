# Chat-Bot-Game
import time

def introduction():
    print("Welcome to the Chat Bot Game!")
    time.sleep(1)
    print("I'll ask you a series of questions, and you'll try to answer them.")
    time.sleep(1)
    print("Let's get started!\n")

def ask_question(question, answer):
    user_response = input(question + " ").lower()
    return user_response == answer.lower()

def play_game():
    score = 0

    # Questions and answers
    questions = [
        ("What is the capital of France?", "Paris"),
        ("Which planet is known as the Red Planet?", "Mars"),
        ("What is the largest mammal in the world?", "Blue Whale"),
    ]

    for question, answer in questions:
        if ask_question(question, answer):
            print("Correct!\n")
            score += 1
        else:
            print(f"Wrong! The correct answer is {answer}.\n")

        time.sleep(1)

    print("Game Over! Your final score is:", score)

if __name__ == "__main__":
    introduction()
    play_game()
