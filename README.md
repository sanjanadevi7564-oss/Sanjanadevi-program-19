# Sanjanadevi-program-19class Node:
    def __init__(self, marks, name):
        self.marks = marks
        self.name = name
        self.left = None
        self.right = None

def insert(root, marks, name):
    if root is None:
        return Node(marks, name)
    if marks < root.marks:
        root.left = insert(root.left, marks, name)
    else:
        root.right = insert(root.right, marks, name)
    return root

def display(root):
    if root:
