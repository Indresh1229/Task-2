# Task-2
#include <iostream> 
 
using namespace std; 
 
int main() { 
    char operation; 
    double num1, num2, result; 
 
    cout << "Enter operation (+, -, *, /): "; 
    cin >> operation; 
 
    cout << "Enter two numbers: "; 
    cin >> num1 >> num2; 
 
    result = num1; 
    for (int i = 1; i < num2; i++) { 
        switch (operation) { 
            case '+': 
                result += num1; 
                break; 
            case '-': 
                result -= num1; 
                break; 
            case '*': 
                result *= num1; 
                break; 
            case '/': 
                if (num1 != 0) { 
                    result /= num1; 
                } else { 
                    cout << "Error! Division by zero."; 
                    return -1; 
                } 
                break; 
            default: 
                cout << "Error! Invalid operation."; 
                return -1; 
        } 
    } 
 
    cout << "Result: " << result << endl; 
 
    return 0; 
} 
