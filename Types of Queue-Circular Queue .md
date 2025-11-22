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
