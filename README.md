# Quizz
quiz_data = [
    {
        "question": "What is the capital of France?",
        "options": ["A: Paris", "B: London", "C: Rome", "D: Berlin"],
        "answer": "A"
    },
    {
        "question": "What is 2 + 2?",
        "options": ["A: 3", "B: 4", "C: 5", "D: 6"],
        "answer": "B"
    },
    {
        "question": "What is the largest planet in our solar system?",
        "options": ["A: Earth", "B: Mars", "C: Jupiter", "D: Saturn"],
        "answer": "C"
    }
]

def quiz_game(quiz_data):
    score = 0
    total_questions = len(quiz_data)
    
    for i, item in enumerate(quiz_data):
        print(f"Question {i + 1}: {item['question']}")
        for option in item['options']:
            print(option)
        
        answer = input("Your answer (A/B/C/D): ").strip().upper()
        
        if answer == item['answer']:
            print("Correct!")
            score += 1
        else:
            print(f"Incorrect! The correct answer is {item['answer']}.")
        
        print()  # Print a newline for better readability
    
    print(f"Quiz completed! Your score: {score}/{total_questions}")

# Run the quiz game
quiz_game(quiz_data)
