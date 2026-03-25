# Bank-Management-System

# Simple Bank Management System (C++)

## 1. Introduction
This project is a basic Bank Management System written in C++. It allows a user to perform simple banking operations like deposit, withdrawal, and balance checking. The program is designed for beginners to understand fundamental programming concepts.

---

## 2. Objectives of the Project
- To learn basic C++ programming
- To understand loops and conditional statements
- To build a menu-driven application
- To simulate simple banking operations
- To improve problem-solving skills

---

## 3. Methodology / System Design
The system follows a simple flow:

1. User enters their name
2. Program initializes balance to 0
3. Menu is displayed:
   - Deposit money
   - Withdraw money
   - Check balance
   - Exit
4. Based on user input:
   - Deposit adds money
   - Withdraw subtracts money (if sufficient balance)
   - Balance displays current amount
5. Loop continues until user exits

---

## 4. Implementation / Source Code

```cpp
// file: simple_bank.cpp

#include <iostream>
using namespace std;

int main() {
    string name;
    float balance = 0;
    int choice;
    float amount;

    cout << "Enter your name: ";
    cin >> name;

    do {
        cout << "\n--- Simple Bank ---\n";
        cout << "1. Deposit\n";
        cout << "2. Withdraw\n";
        cout << "3. Check Balance\n";
        cout << "4. Exit\n";
        cout << "Enter choice: ";
        cin >> choice;

        if (choice == 1) {
            cout << "Enter amount: ";
            cin >> amount;
            balance += amount;
            cout << "Deposited!\n";
        }
        else if (choice == 2) {
            cout << "Enter amount: ";
            cin >> amount;
            if (amount <= balance) {
                balance -= amount;
                cout << "Withdrawn!\n";
            } else {
                cout << "Not enough balance!\n";
            }
        }
        else if (choice == 3) {
            cout << "Name: " << name << endl;
            cout << "Balance: " << balance << endl;
        }

    } while (choice != 4);

    cout << "Thank you!\n";
    return 0;
#5. Conclusion

This project demonstrates a simple banking system using C++. It helps beginners understand how real-world applications work using basic programming constructs. The program can be expanded with more features like multiple users and file storage.
