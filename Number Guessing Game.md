#include <iostream>
#include <cstdlib>
#include <ctime>
using namespace std;
int main()
{
    int number, guess;
    int attempts = 0;
    srand(time(0));
    number = rand() % 100 + 1;
    cout << "----- NUMBER GUESSING GAME -----";
    cout << "\nGuess a number between 1 and 100.";
    do
    {
        cout << "\nEnter your guess: ";
        cin >> guess;
        attempts++;
        if (guess > number)
        {
            cout << "Too High! Try Again.";
        }
        else if (guess < number)
        {
            cout << "Too Low! Try Again.";
        }
        else
        {
            cout << "\nCongratulations! You guessed the correct number.";
            cout << "\nNumber of attempts: " << attempts;
        }
    } while (guess != number);
    return 0;
}
