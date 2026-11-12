#include <iostream>
#include <cstdlib>
#include <ctime>
using namespace std;

int main()
{
    int user, computer;

    srand(time(0));

    cout << "----- ROCK PAPER SCISSORS GAME -----";

    cout << "\n1. Rock";
    cout << "\n2. Paper";
    cout << "\n3. Scissors";

    cout << "\nEnter your choice (1-3): ";
    cin >> user;

    if (user < 1 || user > 3)
    {
        cout << "Invalid Choice!";
        return 0;
    }

    computer = rand() % 3 + 1;

    cout << "\nYour Choice: ";

    if (user == 1)
        cout << "Rock";
    else if (user == 2)
        cout << "Paper";
    else
        cout << "Scissors";

    cout << "\nComputer's Choice: ";

    if (computer == 1)
        cout << "Rock";
    else if (computer == 2)
        cout << "Paper";
    else
        cout << "Scissors";

    if (user == computer)
    {
        cout << "\nIt's a Draw!";
    }
    else if ((user == 1 && computer == 3) ||
             (user == 2 && computer == 1) ||
             (user == 3 && computer == 2))
    {
        cout << "\nCongratulations! You Win!";
    }
    else
    {
        cout << "\nComputer Wins!";
    }

    return 0;
}
