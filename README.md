//Number Guessing Game
#include <iostream>
#include <cstdlib>
#include <ctime>

using namespace std;

int main() {
    srand(time(0)); 
    int randomNumber = rand() % 100 + 1;
    int guess;
  cout << "I have generated a random number between 1 and 100." << endl;
    cout << "Try to guess it!" << endl;
    // Loop until the user guesses the correct number
    while (true) {
        cout << "Enter your guess: ";
        cin >> guess;
        if (guess > randomNumber) {
            cout << "Too high! Try again." << endl;
        } else if (guess < randomNumber) {
            cout << "Too low! Try again." << endl;
        } else {
            cout << "Congratulations! You guessed the correct number: " << randomNumber << endl;
            break;
        }
    }
    return 0;
}
