# Quiz-app
#include <iostream>
using namespace std;

int main() {
    // Quiz questions and answers
    string questions[] = {
        "What is the capital of France?",
        "Which planet is known as the Red Planet?",
        "Who wrote the novel 'Pride and Prejudice'?"
    };

    string options[][4] = {
        {"A. London", "B. Paris", "C. Rome", "D. Madrid"},
        {"A. Venus", "B. Mars", "C. Jupiter", "D. Saturn"},
        {"A. Jane Austen", "B. Charlotte Bronte", "C. Charles Dickens", "D. William Shakespeare"}
    };

    string answers[] = {
        "B",
        "B",
        "A"
    };

    int score = 0;
    int numQuestions = sizeof(questions) / sizeof(questions[0]);

    // Quiz loop
    for (int i = 0; i < numQuestions; i++) {
        // Display question
        cout << "Question " << (i + 1) << ": " << questions[i] << endl;

        // Display options
        for (int j = 0; j < 4; j++) {
            cout << options[i][j] << endl;
        }

        // Get user's answer
        string answer;
        cout << "Enter your answer (A, B, C, or D): ";
        cin >> answer;

        // Check the answer
        if (answer == answers[i]) {
            cout << "Correct!" << endl;
            score++;
        } else {
            cout << "Incorrect!" << endl;
        }

        cout << endl;
    }

    // Display final score
    cout << "Quiz ended. Your score is " << score << "/" << numQuestions << endl;

    return 0;
}
