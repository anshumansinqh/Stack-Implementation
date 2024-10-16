# Stack Implementation Using Array

**Experiment 18**

## Aim  
To study and implement Stack using an array with menu-driven options.

## Theory  
### Definition  
#### What is a Stack?
- A **Stack** is a linear data structure that follows the **LIFO** (Last In First Out) principle.
  - **Push**: Adds an element to the top of the stack.
  - **Pop**: Removes the element from the top of the stack.
  - **Peek**: Views the top element without removing it.
  - **isEmpty**: Checks if the stack is empty.
  
- Stacks are commonly used in applications like recursive algorithms, expression evaluation, backtracking, and memory management.

- Stack operations are implemented using an array in this program.

### Operations:
1. **Push**: Adds an element to the stack if it's not full.
2. **Pop**: Removes an element from the top of the stack if it's not empty.
3. **Display**: Displays all elements in the stack.

> For example, here’s a simple stack implementation using an array in C++:

```cpp
#include <iostream>
using namespace std;

#define MAX 5 // Maximum size of the stack

class Stack {
    int top;
    int arr[MAX]; // Array to store stack elements
    
public:
    Stack() { top = -1; } // Constructor to initialize the stack
    
    // Function to add an element to the stack
    void push(int x) {
        if (top == MAX - 1) {
            cout << "Stack Overflow!" << endl;
        } else {
            arr[++top] = x;
            cout << x << " pushed into the stack." << endl;
        }
    }
    
    // Function to remove an element from the stack
    void pop() {
        if (top == -1) {
            cout << "Stack Underflow!" << endl;
        } else {
            cout << arr[top--] << " popped from the stack." << endl;
        }
    }
    
    // Function to display the stack
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
```
## Conclusion 
In this experiment we learned about Stack implementation using arrays with menu options for Push, Pop, Display, and Exit.





