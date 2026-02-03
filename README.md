program 2
# Stack ADT using Singly Linked List

class Node:
    def __init__(self, data):
        self.data = data
        self.next = None

class Stack:
    def __init__(self):
        self.top = None

    def push(self, data):
        new_node = Node(data)
        new_node.next = self.top
        self.top = new_node
        print("Element pushed successfully.")

    def pop(self):
        if self.top is None:
            print("Stack is empty. Cannot pop.")
        else:
            popped = self.top.data
            self.top = self.top.next
            print("Popped element is:", popped)

    def display(self):
        if self.top is None:
            print("Stack is empty.")
        else:
            temp = self.top
            print("Stack elements are:")
            while temp:
                print(temp.data)
                temp = temp.next

stack = Stack()

while True:
    print("\n--- Stack ADT using Singly Linked List ---")
    print("1. Push")
    print("2. Pop")
    print("3. Display")
    print("4. Exit")

    choice = int(input("Enter your choice: "))

    if choice == 1:
        element = int(input("Enter element to push: "))
        stack.push(element)
    elif choice == 2:
        stack.pop()
    elif choice == 3:
        stack.display()
    elif choice == 4:
        print("Exiting program.")
        break
    else:
        print("Invalid choice.")--- Stack ADT using Singly Linked List ---
1. Push
2. Pop
3. Display
4. Exit
Enter your choice: 1
Enter element to push: 10
Element pushed successfully.

Enter your choice: 1
Enter element to push: 20
Element pushed successfully.

Enter your choice: 3
Stack elements are:
20
10

Enter your choice: 2
Popped element is: 20
