#include <iostream>
using namespace std;

#define MAX 5 

class Stack {
    int top;
    int arr[MAX]; 
    
public:
    Stack() { top = -1; } 
    
    
    void push(int x) {
        if (top == MAX - 1) {
            cout << "Stack Overflow!" << endl;
        } else {
            arr[++top] = x;
            cout << x << " pushed into the stack." << endl;
        }
    }
    
   
    void pop() {
        if (top == -1) {
            cout << "Stack Underflow!" << endl;
        } else {
            cout << arr[top--] << " popped from the stack." << endl;
        }
    }
    
    
    void display() {
        if (top == -1) {
            cout << "Stack is empty." << endl;
        } else {
            cout << "Stack elements: ";
            for (int i = 0; i <= top; i++) {
                cout << arr[i] << " ";
            }
            cout << endl;
        }
    }
};

int main() {
    Stack stack;
    int choice, value;
    
    while (true) {
        cout << "\nMenu:\n1. Push\n2. Pop\n3. Display\n4. Exit\nEnter your choice: ";
        cin >> choice;
        
        switch (choice) {
            case 1:
                cout << "Enter value to push: ";
                cin >> value;
                stack.push(value);
                break;
                
            case 2:
                stack.pop();
                break;
                
            case 3:
                stack.display();
                break;
                
            case 4:
                cout << "Exiting..." << endl;
                exit(0);
                
            default:
                cout << "Invalid choice!" << endl;
        }
    }
    
    return 0;
}
