# Assignment 2 – Expression Tree and Postfix Evaluation

## Data Structures and Algorithms

Subject:PCCST303 – Data Structures and Algorithms
Branch: ADS-B
Year/Semester: Second Year – III Semester
Assignment: Assignment 2
Question: 4

---

## 1. Problem Statement

Consider the following postfix expression:


8 3 2 * + 6 2 / -


The objective of this assignment is to implement an **Expression Tree** using the given postfix expression and evaluate the expression using two different approaches:

1. Stack-based Postfix Evaluation
2. Expression Tree Evaluation

The assignment also requires comparison of the two approaches based on operations, data structure, time complexity, and space requirements.



## 2. Objectives

* Construct an Expression Tree from a postfix expression.
* Display the Expression Tree.
* Perform inorder, preorder, and postorder traversals.
* Evaluate the postfix expression using a stack.
* Evaluate the expression using the Expression Tree.
* Record the important intermediate operations using trace tables.
* Compare the two evaluation methods.
* Analyse their time and space complexities.
* Understand the additional structural information provided by an Expression Tree.



## 3. Input

The postfix expression used in this assignment is:


8 3 2 * + 6 2 / -




## 4. Expression Tree

The expression tree constructed from the postfix expression is:


          -
        /   \
       +     /
      / \   / \
     8   * 6   2
        / \
       3   2


The root of the expression tree is `-`.

---

## 5. Traversals

The expression tree is traversed using:

### Inorder Traversal


8 + 3 * 2 - 6 / 2


### Preorder Traversal


- + 8 * 3 2 / 6 2


### Postorder Traversal


8 3 2 * + 6 2 / -


The postorder traversal represents the original postfix expression.



## 6. Evaluation

### Stack-Based Postfix Evaluation

The postfix expression is scanned from left to right.

Important operations include:


3 * 2 = 6
8 + 6 = 14
6 / 2 = 3
14 - 3 = 11


Therefore:


Result = 11


### Expression Tree Evaluation

The left and right subtrees are evaluated recursively.


3 * 2 = 6
8 + 6 = 14
6 / 2 = 3
14 - 3 = 11


Therefore:


Result = 11

Both methods produce the same final result.

---

## 7. Files and Folders

The repository contains the following files:

Assignment-2-Question-4/
│
├── README.md
│
├── src/
│   └── expression_tree.c
│
├── input/
│   └── input.txt
│
├── output/
│   └── output.txt
│
├── trace/
│   ├── postfix_evaluation_trace.txt
│   └── expression_tree_trace.txt
│
├── diagrams/
│   └── expression_tree.png
│
├── analysis/
│   ├── complexity_analysis.md
│   └── comparison_table.md
│
└── conclusion/
    └── conclusion.md


---

## 8. Complexity Analysis

| Operation                    | Time Complexity | Space Complexity |
| ---------------------------- | --------------- | ---------------- |
| Expression Tree Construction | O(n)            | O(n)             |
| Postfix Evaluation           | O(n)            | O(n)             |
| Tree Traversal               | O(n)            | O(h)             |
| Expression Tree Evaluation   | O(n)            | O(h)             |

Where:

* `n` = number of tokens in the expression
* `h` = height of the expression tree

---

## 9. Comparison

| Feature                | Stack-Based Postfix Evaluation | Expression Tree Evaluation      |
| ---------------------- | ------------------------------ | ------------------------------- |
| Data Structure         | Stack                          | Binary Tree                     |
| Evaluation             | Scans postfix expression       | Traverses expression tree       |
| Time Complexity        | O(n)                           | O(n)                            |
| Space Requirement      | O(n)                           | O(h) for recursive evaluation   |
| Structural Information | Limited                        | Provides hierarchical structure |
| Representation         | Postfix form                   | Tree representation             |

The Expression Tree provides additional structural information because it clearly represents the relationship between operands and operators. It shows which operands are combined by each operator and represents the hierarchical structure of the expression.

---

## 10. How to Compile and Run

The program is written in C.

### Compile


gcc expression_tree.c -o expression_tree


### Run

On Linux/macOS:


./expression_tree


On Windows:
expression_tree.exe

## 11. Expected Output

Postfix Expression:
8 3 2 * + 6 2 / -

Inorder Traversal:
8 + 3 * 2 - 6 / 2

Preorder Traversal:
- + 8 * 3 2 / 6 2

Postorder Traversal:
8 3 2 * + 6 2 / -

Stack-Based Postfix Evaluation
Result = 11

Expression Tree Evaluation
Result = 11


## 12. Conclusion

The postfix expression was successfully converted into an Expression Tree and evaluated using both stack-based postfix evaluation and Expression Tree evaluation.

Both methods produced the same result, which is **11**.

Stack-based postfix evaluation provides a direct way to evaluate a postfix expression using a stack. The Expression Tree, in addition to allowing evaluation, provides a clear hierarchical representation of the expression and supports different tree traversals.

Thus, the implementation demonstrates how stacks and trees can be used to process and represent arithmetic expressions.
