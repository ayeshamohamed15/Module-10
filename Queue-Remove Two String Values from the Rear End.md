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
