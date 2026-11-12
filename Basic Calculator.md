#include <iostream>
using namespace std;
int main()
{
    int choice;
    float num1, num2, result;
    do
    {
        cout << "\n----- BASIC CALCULATOR -----";
        cout << "\n1. Addition";
        cout << "\n2. Subtraction";
        cout << "\n3. Multiplication";
        cout << "\n4. Division";
        cout << "\n5. Exit";
        cout << "\nEnter your choice: ";
        cin >> choice;
        if (choice >= 1 && choice <= 4)
        {
            cout << "Enter two numbers: ";
            cin >> num1 >> num2;
        }
        switch (choice)
        {
            case 1:
                result = num1 + num2;
                cout << "Addition = " << result;
                break;
            case 2:
                result = num1 - num2;
                cout << "Subtraction = " << result;
                break;
            case 3:
                result = num1 * num2;
                cout << "Multiplication = " << result;
                break;
            case 4:
                if (num2 != 0)
                {
                    result = num1 / num2;
                    cout << "Division = " << result;
                }
                else
                {
                    cout << "Error! Division by zero is not allowed.";
                }
                break;
            case 5:
                cout << "Exiting Calculator...";
                break;
            default:
                cout << "Invalid choice! Please try again.";
        }
    } while (choice != 5);
    return 0;
}
