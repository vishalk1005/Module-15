# Ex. No: 15A - Build a Binary Tree with String Values

## AIM:
To write a Python program to build a binary tree with a root, left, and right node using string values.

## ALGORITHM:

1. **Start the program.**
2. **Import** the `Node` class from the `binarytree` module.
3. **Create a root node** using the `Node` class and assign a floating-point value.
4. **Create left and right child nodes** for the root with string values.
5. **Convert the tree** to a list and print the list of nodes.
6. **End the program.**

## PYTHON PROGRAM

```
from binarytree  import Node
l=[]
for i in range(3):
    n=input()
    l.append(n)
root=Node(l[0])
root.left=Node(l[1])
root.right=Node(l[2])
#rootNode=[root,root.left,root.right]
print("Binary Tree :")
for i in root.values:
    print(i,'--> ',end='')
```

## OUTPUT

![image](https://github.com/user-attachments/assets/723441bb-e647-45a7-93a8-b09d74155d3e)

## RESULT

Thus the python program to build a binary tree with a root, left, and right node using floating-point values was successfully executed.
