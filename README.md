# Queue-Queue Values in Descending Order Using Python 🧮

This Python program simulates a queue using a list, removes the first two elements (FIFO order), and displays the remaining values in descending order.

## 🎯 Aim

To write a Python program to:
- Accept user inputs into a list (queue)
- Remove the first two elements (simulating dequeue)
- Display the remaining values in **descending order**

## 🧠 Algorithm

1. Create an empty list `q`.
2. Read an integer `n` to determine how many elements will be added.
3. Loop `n` times:
   - Read an input value.
   - Append it to the list `q`.
4. Remove the first element using `pop(0)`.
5. Remove the second element using `pop(0)` again.
6. Sort the list in descending order.
7. Print the updated list.

## 🧪 Program: 
from queue import PriorityQueue<br>
que=PriorityQueue()<br>
n=int(input())<br>
l=[]<br>
for i in range(n):<br>
    l.append(int(input()))<br>
for number in l:<br>
    que.put((-number, number))<br>
while not que.empty():<br>
    print(que.get()[1])
### Output:
<img width="346" height="507" alt="image" src="https://github.com/user-attachments/assets/81dd1869-bf96-487c-ac56-3fdd6515d928" />

## Result:
Thus the output is verified.
# Queue-Remove Two String Values from the Rear End in Python 🧵

This Python program demonstrates how to manage a list of strings and remove the last two elements (i.e., from the rear of the list).

## 🎯 Aim

To write a Python program to:
- Accept `n` string values from the user
- Remove the last two values (rear end of the list)
- Display the updated list

## 🧠 Algorithm

1. Create an empty list `q`.
2. Read an integer `n` from the user (number of strings).
3. Loop `n` times:
   - Read a string input.
   - Append it to the list `q`.
4. Remove the last element using `pop()`.
5. Remove the next last element using `pop()` again.
6. Display the updated list.

##  Program:
from collections import deque<br>
q = deque()<br>
n=int(input())<br>
for i in range(n):<br>
    q.append(input())<br>
for i in range(2):<br>
    q.popleft()<br>
print(q)<br>
q = deque()<br>
n=int(input())<br>
for i in range(n):<br>
    q.append(input())<br>
for i in range(2):<br>
    q.popleft()<br>
print(q)

### Output:
<img width="1088" height="387" alt="image" src="https://github.com/user-attachments/assets/ed99b6eb-bbe2-460f-a9e9-7350f70413b7" />

## Result:
Thus the output is verified.
# Stack Implementation Using `LifoQueue` (Max Size 7) 🔄

This Python program demonstrates a stack implemented using the `LifoQueue` class from the `queue` module. It allows up to 7 elements, checks if the stack is full, and then prints the elements in reverse (LIFO) order.

## 🎯 Aim

To create a Python program that:
- Implements a stack using `LifoQueue` with a maximum size of 7
- Adds user-inputted values to the stack
- Checks whether the stack is full
- Prints the stack elements in reverse order (LIFO)

## 📋 Algorithm

1. Import the `LifoQueue` class from the `queue` module.
2. Create a stack with a maximum size of 7.
3. Read the number of elements (`n`) to be added to the stack.
4. Loop `n` times:
   - Read a value from the user.
   - Use `put()` to push it onto the stack if it's not full.
5. Use `full()` to check if the stack is full and print the result.
6. Use `get()` repeatedly to pop and print elements in reverse order.

## Program
from queue import LifoQueue<br>
stack = LifoQueue(maxsize=5)<br>
n= int(input())<br>
for i in range(n):<br>
    stack.put(input())<br>
print(stack.full())<br>
for i in range(n):<br>
    print(stack.get())<br>
## 🧪 Sample Input and Output
<img width="359" height="416" alt="image" src="https://github.com/user-attachments/assets/a68fc4b7-ca97-4217-bd8a-09868a824755" />

## Result:
Thus the output is verified.
# # Stack-Stack Reversal Program 🔁

This Python program demonstrates how to reverse the values in a stack using basic stack operations like push and pop.

## 🎯 Aim

To write a Python program that reverses the values in a stack using standard stack operations.

## 📋 Algorithm

1. Create an empty stack.
2. Read an integer `n` from the user (number of elements to push).
3. Loop `n` times:
   - Read an integer from the user.
   - Push it onto the stack.
4. Create an empty list called `reverse`.
5. While the stack is not empty:
   - Pop the top element.
   - Append it to `reverse`.
6. Print the reversed list.


### Program:
def insertAtBottom(s, item):<br>
    if not s:<br>
        s.append(item)<br>
        return<br>
    top = s.pop()<br>
    insertAtBottom(s, item)<br>
    s.append(top)<br>

def reverseStack(s):<br>
  if not s:<br>
    return<br>
  item = s.pop()<br>
    reverseStack(s)<br>
 
insertAtBottom(s, item)<br>
    return s<br>
l=[]<br>
n=int(input())<br>
for i in range(n):<br>
    l.append(int(input()))<br>
print(reverseStack(l))

## 🧪 Sample Input and Output
<img width="604" height="289" alt="image" src="https://github.com/user-attachments/assets/cf4cc059-8159-491e-868b-600db5309376" />


## Result
Thus the output is verified.
# 🔄 Types of Queue-Circular Queue in Python

This project demonstrates the implementation of a **Circular Queue** in Python. The queue accepts 3 user values, performs enqueue and dequeue operations, and displays the removed values.

---

## 🎯 Aim

To develop a Python program that implements a Circular Queue:
- Accepts 3 values from the user
- Removes the 3 values from the queue
- Displays the removed values

---

## 🧠 Algorithm

1. **Initialize** a circular queue of fixed size (e.g., 5).
2. **Define the following functions**:
   - `enqueue()`: Inserts an element into the queue.
   - `dequeue()`: Removes an element from the queue.
   - `display()`: Shows the queue contents.
3. Accept 3 values from the user using the `enqueue()` method.
4. Remove 3 values using the `dequeue()` method.
5. Print the removed values.

---

## 💻 Program:
class MyCircularQueue():<br>
    def __init__(self, k):<br>
        self.k = k<br>
        self.queue = [None] * k<br>
        self.head = self.tail = -1<br>
    def enqueue(self, data):<br>
        if ((self.tail + 1) % self.k == self.head):<br>
            print("The circular queue is full\n")<br>
        elif (self.head == -1):<br>
            self.head = 0<br>
            self.tail = 0<br>
            self.queue[self.tail] = data<br>
        else:<br>
            self.tail = (self.tail + 1) % self.k<br>
            self.queue[self.tail] = data<br>
    #
    def printCQueue(self):<br>
        if(self.head == -1):<br>
            print("No element in the circular queue")<br>
        elif (self.tail >= self.head):<br>
            for i in range(self.head, self.tail + 1):<br>
                print(self.queue[i], end=" ")<br>
            print()<br>
        else:<br>
            for i in range(self.head, self.k):<br>
                print(self.queue[i], end=" ")<br>
            for i in range(0, self.tail + 1):<br>
                print(self.queue[i], end=" ")<br>
            print()<br>
obj = MyCircularQueue(5)<br>
for i in range(5):<br>
    obj.enqueue(int(input()))<br>
obj.printCQueue()


### Output:
<img width="503" height="393" alt="image" src="https://github.com/user-attachments/assets/a73c5930-419b-473f-997e-5b5c594a1264" />

## Result:
Thus the output is verified.



