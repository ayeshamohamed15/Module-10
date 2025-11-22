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
