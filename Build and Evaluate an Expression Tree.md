# Ex. No: 15E - Build and Evaluate an Expression Tree

## AIM:
To write a Python program to build and evaluate the given Expression tree.

## ALGORITHM:

1. **Start the program.**
2. Create nodes for operators and operands.
3. Build the expression tree by connecting nodes in the correct hierarchical structure.
4. Define a recursive function `evaluate(root)`:
   - If the node is a number (leaf), return it.
   - Else, recursively evaluate left and right subtrees.
   - Apply the operator at the current node to the results.
5. Return the final result from the root node.
6. **End the program.**

## PROGRAM:

```
from binarytree import Node
class Node:
    def __init__(self, val, left=None, right=None):
        self.val = val
        self.left = left
        self.right = right

def isLeaf(node):
    return node.left is None and node.right is None
 
def process(op, x, y):
    if op == '+':
        return x + y
    if op == '-':
        return x - y
    if op == '*':
        return x * y
    if op == '/':
        return x / y
 
def evaluate(root):
    if root is None:
        return 0
    if isLeaf(root):
        return float(root.val)
    x=evaluate(root.left)
    y=evaluate(root.right)
    return process(root.val,x,y)

root=Node('*')
root.left=Node('+')
root.right=Node('+')
root.left.left=Node(7)
root.left.right=Node(6)
root.right.left=Node(2)
root.right.right=Node(6)
print("The value of the expression tree is",evaluate(root))
```

## OUTPUT:

![image](https://github.com/user-attachments/assets/109cb74e-2f7c-4f86-9225-bf53f2a34402)


## RESULT:

Thus the Python program to build and evaluate the given Expression tree was successfully executed.
