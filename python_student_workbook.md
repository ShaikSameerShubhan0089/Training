# Python Placement Training Student Workbook

For third-year students, non-IT students, and absolute beginners

This workbook is designed for students to write, think, dry run, and practice during the 5-day Python training.

Use this workbook with the main course manual:
[python_5_day_placement_training_manual.md](C:/Users/S Sameer/Desktop/training/python_5_day_placement_training_manual.md)

---

# How to Use This Workbook

## Student Promise
While learning from this workbook:
- I will not fear mistakes
- I will first think, then code
- I will dry run before running the code
- I will practice every day

## Golden Method
For every problem, follow this order:
1. What is the input?
2. What is the output?
3. What should happen step by step?
4. Which concept is needed?
5. Write the logic in plain English
6. Then write Python code

## My Notes Area

Name: ______________________

College: ____________________

Branch: _____________________

Date: ______________________

---

# DAY 1 WORKBOOK

## Topics
- Input/Output
- Variables
- Data Types
- Type Casting
- Operators
- Conditional Statements
- Loops
- Number Problems

## Before We Start

### Write in your own words
1. What is a variable?

Answer:
____________________________________________________
____________________________________________________

2. What is input?

Answer:
____________________________________________________
____________________________________________________

3. What is output?

Answer:
____________________________________________________
____________________________________________________

4. Why do we use loops?

Answer:
____________________________________________________
____________________________________________________

---

## Quick Warm-up

### Predict the output

1.
```python
x = 10
print(x)
```
My answer: ____________________

2.
```python
a = 5
b = 2
print(a + b)
```
My answer: ____________________

3.
```python
num = 7
print(num % 2)
```
My answer: ____________________

4.
```python
for i in range(3):
    print(i)
```
My answer:
____________________
____________________
____________________

---

## Section 1: Variables Practice

### Fill the blanks

1. A variable is like a __________________ box.
2. In `age = 20`, `age` is the __________________.
3. In `age = 20`, `20` is the __________________.
4. `=` means __________________ in Python.

### Write your own examples

Store your name in a variable:
```python

```

Store your age in a variable:
```python

```

Store your college name in a variable:
```python

```

---

## Section 2: Input and Output Practice

### Write a program
Take your name and print:
`Welcome <name>`

```python



```

### Dry run area
If input is `Asha`, what should output be?

Answer:
____________________________________________________

### Write a program
Take two numbers and print their sum.

```python




```

### My thinking
- Input: __________________________________________
- Output: _________________________________________
- Formula: ________________________________________

---

## Section 3: Data Types and Type Casting

### Match the type

| Value | Data Type |
|---|---|
| `10` | __________________ |
| `3.14` | __________________ |
| `"hello"` | __________________ |
| `True` | __________________ |

### Write answers

1. Why do we use `int(input())`?

Answer:
____________________________________________________
____________________________________________________

2. What is the difference between `"10"` and `10`?

Answer:
____________________________________________________
____________________________________________________

### Practice code
Take a number as input and print its square.

```python



```

---

## Section 4: Operators

### Complete the table

| Expression | My Answer |
|---|---|
| `10 + 5` | __________ |
| `10 - 5` | __________ |
| `10 * 5` | __________ |
| `10 / 5` | __________ |
| `10 % 3` | __________ |
| `10 // 3` | __________ |
| `2 ** 3` | __________ |

### True or False

| Condition | True/False |
|---|---|
| `10 > 5` | __________ |
| `3 == 4` | __________ |
| `7 != 2` | __________ |
| `5 <= 5` | __________ |

### Write a program
Take two numbers and print:
- addition
- subtraction
- multiplication
- division

```python






```

---

## Section 5: Conditional Statements

### Think first

Problem:
Take a number and check if it is even or odd.

### How to think
- What should be checked? ___________________________
- What condition is needed? _________________________
- If condition is true, print _______________________
- Else print _______________________________________

### Write code
```python




```

### Dry run
If input is `8`:
- `8 % 2 =` __________
- Output = __________________

If input is `5`:
- `5 % 2 =` __________
- Output = __________________

---

## Section 6: Loops

### `for` loop practice
Write a program to print numbers from 1 to 10.

```python



```

### Dry run area

| Loop variable value | Printed output |
|---|---|
| 1 | __________ |
| 2 | __________ |
| 3 | __________ |
| 4 | __________ |

### `while` loop practice
Write a program to print numbers from 1 to 5 using `while`.

```python




```

### Important check

What happens if you forget `i += 1`?

Answer:
____________________________________________________

---

## Section 7: Number Problems

## Problem 1: Sum of first n numbers

### How to think
- Start total from: __________________
- Repeat from: _______________________
- Add each number to: ________________

### Dry run for `n = 5`

| i | total before | total after |
|---|---|---|
| 1 | _____ | _____ |
| 2 | _____ | _____ |
| 3 | _____ | _____ |
| 4 | _____ | _____ |
| 5 | _____ | _____ |

### Write code
```python




```

---

## Problem 2: Factorial

### Meaning
`5! = _____________________________________________`

### Dry run for `n = 4`

| i | fact before | fact after |
|---|---|---|
| 1 | _____ | _____ |
| 2 | _____ | _____ |
| 3 | _____ | _____ |
| 4 | _____ | _____ |

### Write code
```python




```

---

## Problem 3: Fibonacci

### Fill the sequence
`0, 1, ___, ___, ___, ___`

### Dry run

| Step | a | b | Printed |
|---|---|---|---|
| 1 | _____ | _____ | _____ |
| 2 | _____ | _____ | _____ |
| 3 | _____ | _____ | _____ |
| 4 | _____ | _____ | _____ |

### Write code
```python




```

---

## Problem 4: Reverse Number

### Concept check
- Last digit comes from: __________________
- Remove last digit using: ________________

### Dry run for `123`

| num | digit | rev |
|---|---|---|
| 123 | _____ | _____ |
| 12 | _____ | _____ |
| 1 | _____ | _____ |

### Write code
```python




```

---

## Problem 5: Palindrome Number

### Example
Is `121` a palindrome? __________________

Why?
____________________________________________________

### Write code
```python




```

---

## Problem 6: Prime Number

### Think first
Prime means it has exactly __________________ factors.

### Check manually
Is 7 prime?

Divisibility table:

| Check with | Remainder / result |
|---|---|
| 2 | __________ |
| 3 | __________ |
| 4 | __________ |
| 5 | __________ |
| 6 | __________ |

Conclusion:
____________________________________________________

### Write code
```python





```

---

## Problem 7: Armstrong Number

### Example
`153 = 1^3 + 5^3 + 3^3`

Complete:
- `1^3 = ______`
- `5^3 = ______`
- `3^3 = ______`
- Total = ______

### Write code
```python




```

---

## Day 1 Practice Set

### Easy
1. Check even or odd
2. Check positive or negative
3. Print 1 to n
4. Sum of digits
5. Count digits

### Write your answers

1.
```python


```

2.
```python


```

3.
```python


```

4.
```python


```

5.
```python


```

### Medium
1. Greatest of 3 numbers
2. Multiplication table
3. Reverse a number
4. Palindrome number
5. Factorial

### Challenge
1. Prime number
2. Fibonacci series
3. Armstrong number

## Day 1 Reflection

Today I understood best:
____________________________________________________

Today I found difficult:
____________________________________________________

I need more practice in:
____________________________________________________

---

# DAY 2 WORKBOOK

## Topics
- Pattern Problems
- Lists
- Strings
- Matrices

## Section 1: Pattern Thinking

### Rule to remember
- Outer loop = ______________________
- Inner loop = ______________________

### Pattern Observation Practice

Pattern:
```text
*
**
***
****
```

Fill:
- Number of rows = __________________
- Row 1 stars = _____________________
- Row 2 stars = _____________________
- Row 3 stars = _____________________
- Row 4 stars = _____________________

### Write code
```python




```

### Pattern 2
```text
****
***
**
*
```

How do stars change?
____________________________________________________

Write code:
```python




```

### Pattern 3
```text
1
12
123
1234
```

What changes in each row?
____________________________________________________

Write code:
```python




```

### Pattern 4
```text
   *
  **
 ***
****
```

Fill:
- Row 1 spaces = ______, stars = ______
- Row 2 spaces = ______, stars = ______
- Row 3 spaces = ______, stars = ______
- Row 4 spaces = ______, stars = ______

Write code:
```python




```

---

## Section 2: Lists

### Concept check
List index starts from: __________________

For `nums = [10, 20, 30, 40]`
- `nums[0] = __________________`
- `nums[2] = __________________`
- `nums[-1] = __________________`

### Write and test
Create a list of 5 numbers and print:
- whole list
- first element
- last element

```python




```

### List operations
Fill the meaning:
- `append()` = ______________________
- `insert()` = ______________________
- `remove()` = ______________________
- `sort()` = ________________________

### Practice
Write code to find largest element in list.

```python




```

### Dry run
For `[5, 1, 9, 2]`

| Current value | Largest so far |
|---|---|
| 5 | ______ |
| 1 | ______ |
| 9 | ______ |
| 2 | ______ |

---

## Section 3: Strings

### Concept check
A string is a collection of __________________

For `text = "python"`
- `text[0] = __________________`
- `text[2] = __________________`
- `text[-1] = __________________`

### Slicing
For `text = "python"`
- `text[0:2] = __________________`
- `text[2:5] = __________________`
- `text[::-1] = __________________`

### Immutability
Can we do this?
```python
text = "cat"
text[0] = "b"
```

Answer: __________________

Why?
____________________________________________________

### Practice
Write code to count vowels in a string.

```python




```

### Practice
Write code to reverse a string.

```python




```

### Palindrome string
Check if `"madam"` is palindrome:
___________________________________________

Write code:
```python



```

---

## Section 4: Matrices

### Concept check
Matrix means list of __________________

For:
```python
matrix = [
    [1, 2, 3],
    [4, 5, 6]
]
```

Fill:
- `matrix[0][0] = __________________`
- `matrix[0][2] = __________________`
- `matrix[1][1] = __________________`
- `matrix[1][2] = __________________`

### Practice
Write code to print all elements row by row.

```python




```

### Practice
Write code to find sum of all matrix elements.

```python




```

---

## Day 2 Practice Set

### Easy
1. Square pattern
2. Sum of list elements
3. First and last character of string
4. Count vowels
5. Print matrix elements

### Medium
1. Reverse list
2. Largest element in list
3. Reverse string
4. Palindrome string
5. Row sums in matrix

### Challenge
1. Anagram check
2. Word count in sentence
3. Matrix transpose

## Day 2 Reflection

Pattern logic I understood:
____________________________________________________

String topic I need more practice in:
____________________________________________________

Matrix indexing confusion:
____________________________________________________

---

# DAY 3 WORKBOOK

## Topics
- Searching
- Sorting
- Functions
- Recursion

## Section 1: Searching

### Linear Search
What is linear search in your own words?
____________________________________________________

For list `[2, 5, 7, 9]`, find `7`

| Checked value | Found or not? |
|---|---|
| 2 | __________ |
| 5 | __________ |
| 7 | __________ |

Write code:
```python




```

### Binary Search
Important rule:
Binary search works only on __________________ list.

For `[2, 4, 6, 8, 10]`, find `8`

| low | high | mid | value at mid | next step |
|---|---|---|---|---|
| _____ | _____ | _____ | _____ | _____ |
| _____ | _____ | _____ | _____ | _____ |

Write code:
```python





```

---

## Section 2: Sorting

### Bubble Sort
Sort `[5, 3, 1, 4]`

Pass 1:
____________________________________________________

Pass 2:
____________________________________________________

Pass 3:
____________________________________________________

Write code:
```python




```

### Selection Sort
Idea:
Each round we choose the __________________ element.

Write code:
```python




```

### Insertion Sort
Real-life analogy:
____________________________________________________

Write code:
```python




```

---

## Section 3: Functions

### Fill the blanks
- `def` is used to __________________
- `return` is used to __________________
- Parameter means ____________________

### Write a function
Function to add 2 numbers:
```python



```

### Write a function
Function to check prime number:
```python




```

---

## Section 4: Recursion

### What is recursion?
____________________________________________________

### Most important thing in recursion
____________________________________________________

### Dry run factorial(4)

Complete:
- `factorial(4) = 4 * factorial(_____)`
- `factorial(3) = 3 * factorial(_____)`
- `factorial(2) = 2 * factorial(_____)`
- `factorial(1) = _____`

Write code:
```python




```

---

## Day 3 Practice Set

### Easy
1. Linear search
2. Function to square number
3. Function to check even
4. Bubble sort
5. Recursive sum

### Medium
1. Binary search
2. Selection sort
3. Insertion sort
4. Largest of 3 using function
5. Recursive power

### Challenge
1. Recursive Fibonacci
2. Binary search as function
3. Count occurrences in list

## Day 3 Reflection

Searching concept:
____________________________________________________

Sorting concept:
____________________________________________________

Recursion fear level now:
____________________________________________________

---

# DAY 4 WORKBOOK

## Topics
- Python Memory Model
- References
- Mathematical Problems
- Built-in Data Structures
- Built-in Functions and Libraries

## Section 1: References

### Think in your own words
What happens here?
```python
a = [1, 2, 3]
b = a
b[0] = 99
```

Answer:
____________________________________________________
____________________________________________________

### What if we use `.copy()`?
```python
a = [1, 2, 3]
b = a.copy()
b[0] = 99
```

What changes now?
____________________________________________________

---

## Section 2: GCD and LCM

### GCD
Find GCD of 12 and 18 manually:

| a | b | a % b |
|---|---|---|
| _____ | _____ | _____ |
| _____ | _____ | _____ |
| _____ | _____ | _____ |

Answer: __________________

Write code:
```python




```

### LCM
Formula:
`LCM = _____________________________________________`

Write code:
```python




```

---

## Section 3: Data Structures

### List
When do we use list?
____________________________________________________

### Set
When do we use set?
____________________________________________________

### Dictionary
When do we use dictionary?
____________________________________________________

### Practice
Remove duplicates from list:
```python



```

### Practice
Count frequency using dictionary:
```python




```

---

## Section 4: Built-in Functions and Libraries

### Fill the purpose
- `len()` = __________________________
- `sum()` = __________________________
- `max()` = __________________________
- `min()` = __________________________
- `sorted()` = _______________________

### Counter
What is `Counter` useful for?
____________________________________________________

### Practice
Count character frequency in `"banana"`

```python



```

---

## Day 4 Practice Set

### Easy
1. GCD
2. LCM
3. Remove duplicates
4. Frequency using dictionary
5. Sum using built-in

### Medium
1. Perfect number
2. Common elements in two lists
3. Second largest element
4. Word frequency
5. Counter usage

### Challenge
1. Coprime numbers
2. Highest frequency element
3. Reference vs copy example

## Day 4 Reflection

What I understood about references:
____________________________________________________

Which data structure is most useful for me?
____________________________________________________

---

# DAY 5 WORKBOOK

## Topics
- Time Complexity
- Optimization
- Bit Manipulation

## Section 1: Time Complexity

### Write in simple words
What is time complexity?
____________________________________________________
____________________________________________________

### Match the idea

| Type | Meaning |
|---|---|
| `O(1)` | __________________ |
| `O(n)` | __________________ |
| `O(n^2)` | __________________ |

### Identify

1.
```python
print(nums[0])
```
Complexity: __________________

2.
```python
for x in nums:
    print(x)
```
Complexity: __________________

3.
```python
for i in nums:
    for j in nums:
        print(i, j)
```
Complexity: __________________

---

## Section 2: Optimization Thinking

### Problem
Find duplicate in list.

Slow method idea:
____________________________________________________

Better method idea:
____________________________________________________

Which data structure helps?
____________________________________________________

Write optimized code:
```python




```

---

## Section 3: Binary Basics

### Fill the blanks
- Decimal 5 in binary = __________________
- Decimal 6 in binary = __________________
- Binary uses only digits __________________ and __________________

---

## Section 4: Bit Manipulation

### Even or odd using bit
Write code:
```python



```

### Multiply by 2 using shift
Write code:
```python


```

### Divide by 2 using shift
Write code:
```python


```

### Power of 2
Write code:
```python



```

### Count set bits
Write code:
```python




```

---

## Day 5 Practice Set

### Easy
1. Explain `O(1)`
2. Explain `O(n)`
3. Explain `O(n^2)`
4. Even/odd using bit
5. Multiply by 2 using shift

### Medium
1. Divide by 2 using shift
2. Count set bits
3. Power of 2
4. Duplicate using set
5. Frequency using dictionary

### Challenge
1. Single number using XOR
2. Pair sum using set
3. Compare brute force vs optimized approach

## Day 5 Reflection

Optimization idea I understood:
____________________________________________________

Bit manipulation idea I understood:
____________________________________________________

---

# Final Student Self-Check

## I can now do these on my own

Put a tick:

- [ ] Take input and print output
- [ ] Use variables and data types
- [ ] Write `if-else`
- [ ] Use `for` and `while`
- [ ] Solve factorial
- [ ] Reverse a number
- [ ] Work with lists
- [ ] Work with strings
- [ ] Solve pattern problems
- [ ] Use functions
- [ ] Explain recursion
- [ ] Use set and dictionary
- [ ] Explain time complexity simply
- [ ] Solve basic bit problems

## My weak areas
____________________________________________________
____________________________________________________

## My next 7-day practice plan

Day 1: _____________________________________________

Day 2: _____________________________________________

Day 3: _____________________________________________

Day 4: _____________________________________________

Day 5: _____________________________________________

Day 6: _____________________________________________

Day 7: _____________________________________________

