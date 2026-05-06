# 5-Day Python Placement Training Program

Beginner-friendly training manual for third-year university students, including non-IT students.

Goal: Help students become comfortable with basic Python, problem solving, interview-style questions, and coding confidence in 5 days.

---

## How to Use This Manual

- Teach slowly and interactively.
- Ask students to predict output before running code.
- Encourage dry runs on paper.
- Start with simple examples before moving to interview problems.
- Repeat the pattern:
  1. Understand the problem
  2. Think step by step
  3. Dry run
  4. Code
  5. Test with small inputs

---

# DAY 1
## Topics
- Input/Output and Operators
- Conditional Statements
- Loops: `for`, `while`
- Number Problems

## Morning Session (Theory Plan)
- What is Python and why it is beginner-friendly
- How to take input and print output
- Operators: arithmetic, comparison, logical
- Decision making using `if`, `elif`, `else`
- Repeating work using loops
- How number-based interview questions are solved step by step

## Afternoon Session (Hands-on Plan)
- Run simple input/output programs
- Practice operator-based questions
- Write small `if-else` programs
- Solve looping examples
- Solve number problems one by one with dry runs

## 1. Input and Output

### What it is
Input means taking data from the user.
Output means showing a result to the user.

### Why we use it
Programs become useful only when they can receive information and respond.

### Step-by-step
1. Use `input()` to take data.
2. By default, `input()` gives text.
3. Use `int()` if you want a whole number.
4. Use `print()` to show results.

### Dry Run
If user enters `5`:
- `input()` reads `"5"` as text
- `int("5")` converts it to number `5`
- `print()` displays it

### Python Code
```python
# taking a number from user
num = int(input("Enter a number: "))

# showing output
print("You entered:", num)
```

### Output Explanation
If user types `5`, Python stores `5` in `num` and prints:
`You entered: 5`

## 2. Operators

### What it is
Operators are symbols that perform actions.

### Why we use it
We use them for calculation, comparison, and checking conditions.

### Main Types
- Arithmetic: `+ - * / % // **`
- Comparison: `== != > < >= <=`
- Logical: `and or not`

### Dry Run
If `a = 10`, `b = 3`:
- `a + b = 13`
- `a % b = 1` because remainder is 1
- `a > b = True`

### Python Code
```python
a = 10
b = 3

print("Addition:", a + b)
print("Remainder:", a % b)
print("Is a greater than b?", a > b)
```

### Output Explanation
Python performs the requested operation and prints the result line by line.

## 3. Conditional Statements

### What it is
Conditions help a program choose one path from many paths.

### Why we use it
Real life decisions happen all the time.
Example: if it rains, take an umbrella.

### Step-by-step
1. Write a condition after `if`
2. If condition is true, run that block
3. If false, check `elif` or `else`

### Dry Run
Age = 18
- Check `age >= 18`
- True
- Print "Eligible to vote"

### Python Code
```python
age = int(input("Enter your age: "))

if age >= 18:
    print("Eligible to vote")
else:
    print("Not eligible to vote")
```

### Output Explanation
Python checks the condition and prints one of the two messages.

## 4. Loops

### What it is
Loops repeat a task many times.

### Why we use it
Without loops, we would have to write the same code again and again.

## `for` Loop

### Step-by-step
1. Decide how many times to repeat
2. Use `range()`
3. Run the block each time

### Dry Run
`range(1, 4)` gives `1, 2, 3`

### Python Code
```python
for i in range(1, 4):
    print(i)
```

## `while` Loop

### Step-by-step
1. Start with a value
2. Check the condition
3. Run the block
4. Update the value

### Dry Run
`i = 1`
- check `i <= 3` -> True -> print 1
- `i = 2`
- check `i <= 3` -> True -> print 2
- `i = 3`
- check `i <= 3` -> True -> print 3
- `i = 4`
- check `i <= 3` -> False -> stop

### Python Code
```python
i = 1

while i <= 3:
    print(i)
    i += 1
```

## Think Like This
- If the number of repetitions is known, try `for`
- If repetition depends on a condition, try `while`
- For number problems, first understand digit-by-digit logic

## Number Problems

### 1. Sum of First `n` Numbers

#### What it is
Add numbers from 1 to `n`.

#### Why we use it
This teaches loop basics and accumulation.

#### Dry Run for `n = 5`
- sum = 0
- add 1 -> 1
- add 2 -> 3
- add 3 -> 6
- add 4 -> 10
- add 5 -> 15

#### Python Code
```python
n = int(input("Enter n: "))
total = 0

for i in range(1, n + 1):
    total += i

print("Sum =", total)
```

### 2. Factorial

#### What it is
Factorial of 5 means `5 * 4 * 3 * 2 * 1`.

#### Why we use it
Very common interview question.

#### Dry Run for `n = 4`
- fact = 1
- fact = 1 * 1 = 1
- fact = 1 * 2 = 2
- fact = 2 * 3 = 6
- fact = 6 * 4 = 24

#### Python Code
```python
n = int(input("Enter a number: "))
fact = 1

for i in range(1, n + 1):
    fact *= i

print("Factorial =", fact)
```

### 3. Fibonacci Series

#### What it is
A series where each number is the sum of the previous two.
Example: `0 1 1 2 3 5 8`

#### Dry Run for 5 terms
- start with 0, 1
- next = 0 + 1 = 1
- next = 1 + 1 = 2
- next = 1 + 2 = 3

#### Python Code
```python
n = int(input("Enter number of terms: "))
a, b = 0, 1

for _ in range(n):
    print(a, end=" ")
    a, b = b, a + b
```

### 4. Reverse a Number

#### What it is
Change `1234` into `4321`.

#### Step-by-step
1. Take last digit using `% 10`
2. Add it to reversed number
3. Remove last digit using `// 10`

#### Dry Run for `123`
- last digit = 3, rev = 3
- number = 12
- last digit = 2, rev = 32
- number = 1
- last digit = 1, rev = 321

#### Python Code
```python
num = int(input("Enter a number: "))
rev = 0

while num > 0:
    digit = num % 10
    rev = rev * 10 + digit
    num = num // 10

print("Reversed number =", rev)
```

### 5. Prime Number

#### What it is
A prime number has exactly 2 factors: 1 and itself.

#### Why we use it
This checks understanding of loops and conditions.

#### Dry Run for `7`
- check divisibility from 2 to 6
- none divide exactly
- so 7 is prime

#### Python Code
```python
num = int(input("Enter a number: "))
is_prime = True

if num <= 1:
    is_prime = False
else:
    for i in range(2, num):
        if num % i == 0:
            is_prime = False
            break

if is_prime:
    print("Prime")
else:
    print("Not Prime")
```

### 6. Palindrome Number

#### What it is
A number that reads the same forward and backward.
Example: `121`

#### Python Code
```python
num = int(input("Enter a number: "))
original = num
rev = 0

while num > 0:
    digit = num % 10
    rev = rev * 10 + digit
    num //= 10

if original == rev:
    print("Palindrome")
else:
    print("Not Palindrome")
```

### 7. Armstrong Number

#### What it is
For a 3-digit number, add cubes of digits.
If the result equals the number, it is Armstrong.
Example: `153 = 1^3 + 5^3 + 3^3`

#### Dry Run for `153`
- `1^3 = 1`
- `5^3 = 125`
- `3^3 = 27`
- total = `153`

#### Python Code
```python
num = int(input("Enter a 3-digit number: "))
original = num
total = 0

while num > 0:
    digit = num % 10
    total += digit ** 3
    num //= 10

if original == total:
    print("Armstrong")
else:
    print("Not Armstrong")
```

## Practice Problems with Solutions

1. Check even or odd
```python
num = int(input())
print("Even" if num % 2 == 0 else "Odd")
```

2. Find greatest of two numbers
```python
a = int(input())
b = int(input())
print(a if a > b else b)
```

3. Find greatest of three numbers
```python
a = int(input())
b = int(input())
c = int(input())
print(max(a, b, c))
```

4. Print numbers from 1 to `n`
```python
n = int(input())
for i in range(1, n + 1):
    print(i)
```

5. Print table of a number
```python
n = int(input())
for i in range(1, 11):
    print(n, "x", i, "=", n * i)
```

6. Count digits in a number
```python
num = int(input())
count = 0

while num > 0:
    count += 1
    num //= 10

print(count)
```

7. Sum of digits
```python
num = int(input())
total = 0

while num > 0:
    total += num % 10
    num //= 10

print(total)
```

8. Product of digits
```python
num = int(input())
product = 1

while num > 0:
    product *= num % 10
    num //= 10

print(product)
```

9. Check leap year
```python
year = int(input())

if (year % 400 == 0) or (year % 4 == 0 and year % 100 != 0):
    print("Leap Year")
else:
    print("Not Leap Year")
```

10. Print all factors of a number
```python
n = int(input())
for i in range(1, n + 1):
    if n % i == 0:
        print(i, end=" ")
```

## Coding Exercises

### Easy
- Even or odd
- Positive, negative, or zero
- Sum of digits

### Medium
- Reverse a number
- Prime number
- Fibonacci series

### Challenge
- Armstrong number
- Strong number
- Prime numbers in a range

## Mini Assignment
- Write a menu-driven calculator using `if-elif`
- Write a program to check whether a number is palindrome, prime, and Armstrong

## Interview Tips
- Explain your logic before coding
- Use small sample input for dry run
- For digit problems, mention `% 10` and `// 10`
- Do not rush into writing full code

## Common Mistakes Students Make
- Forgetting `int(input())`
- Infinite `while` loop because update is missing
- Using `=` instead of `==`
- Wrong indentation
- Forgetting to store original number before modifying it

## Quick Revision Summary
- `input()` takes data, `print()` shows result
- Operators perform calculations and comparisons
- `if-else` helps in decisions
- `for` and `while` repeat work
- Number problems often use `% 10` and `// 10`

---

# DAY 2
## Topics
- Pattern Problems
- 1D Arrays (Lists)
- Strings Basics and Problems
- 2D Arrays (Matrices)

## Morning Session (Theory Plan)
- How to think about rows and columns in patterns
- Lists as a collection of values
- Strings as text made of characters
- Matrix basics using rows and columns

## Afternoon Session (Hands-on Plan)
- Build 4 to 5 simple patterns
- Solve list-based problems
- Practice string operations and interview questions
- Solve matrix input and traversal problems

## 1. Pattern Problems

### What it is
Pattern problems print shapes using stars, numbers, or letters.

### Why we use it
They build logic and control over loops.

## Think Like This
- Outer loop controls rows
- Inner loop controls what happens inside each row
- First ask: how many rows?
- Then ask: how many stars/spaces in each row?

## Pattern 1
```text
*
**
***
****
```

### Step-by-step
- Row 1 -> print 1 star
- Row 2 -> print 2 stars
- Row 3 -> print 3 stars

### Python Code
```python
rows = 4

for i in range(1, rows + 1):
    for j in range(i):
        print("*", end="")
    print()
```

## Pattern 2
```text
****
***
**
*
```

### Python Code
```python
rows = 4

for i in range(rows, 0, -1):
    for j in range(i):
        print("*", end="")
    print()
```

## Pattern 3
```text
1
12
123
1234
```

### Python Code
```python
rows = 4

for i in range(1, rows + 1):
    for j in range(1, i + 1):
        print(j, end="")
    print()
```

## Pattern 4
```text
   *
  **
 ***
****
```

### Logic
- Spaces decrease
- Stars increase

### Python Code
```python
rows = 4

for i in range(1, rows + 1):
    print(" " * (rows - i) + "*" * i)
```

## 2. 1D Arrays in Python: Lists

### What it is
A list stores many values in one variable.

### Why we use it
Instead of making separate variables like `a1, a2, a3`, we use one list.

### Dry Run
`nums = [10, 20, 30]`
- `nums[0] = 10`
- `nums[1] = 20`
- `nums[2] = 30`

### Python Code
```python
nums = [10, 20, 30, 40]

print(nums)
print(nums[0])
print(nums[-1])
```

### Output Explanation
- Whole list is printed
- First element is `10`
- Last element is `40`

## Common List Operations
```python
nums = [1, 2, 3]

nums.append(4)      # add at end
nums.insert(1, 10)  # add at index 1
nums.remove(2)      # remove value 2
nums.sort()         # sort ascending

print(nums)
```

## 3. Strings Basics

### What it is
A string is text.

### Why we use it
Names, sentences, passwords, email IDs, and messages are all strings.

### Dry Run
`word = "cat"`
- `word[0] = 'c'`
- `word[1] = 'a'`
- `word[2] = 't'`

### Common Operations
```python
text = "python"

print(text.upper())
print(text.lower())
print(text[0])
print(len(text))
```

## String Problem: Reverse a String

### Step-by-step
Take characters from the end to the beginning.

### Python Code
```python
text = input("Enter a string: ")
rev = ""

for ch in text:
    rev = ch + rev

print("Reversed string:", rev)
```

## String Problem: Palindrome
```python
text = input("Enter a string: ")

if text == text[::-1]:
    print("Palindrome")
else:
    print("Not Palindrome")
```

## 4. 2D Arrays: Matrices

### What it is
A matrix is a list of lists.
Think of it like seats in a classroom: rows and columns.

### Why we use it
Useful for tables, grids, game boards, marksheets, and image-like data.

### Example
```python
matrix = [
    [1, 2, 3],
    [4, 5, 6]
]
```

### Indexing Explanation
- `matrix[0][0] = 1`
- `matrix[0][1] = 2`
- `matrix[1][2] = 6`

### Traversing Matrix
```python
matrix = [
    [1, 2, 3],
    [4, 5, 6]
]

for row in matrix:
    for value in row:
        print(value, end=" ")
    print()
```

## Matrix Problem: Sum of All Elements
```python
matrix = [
    [1, 2],
    [3, 4]
]

total = 0

for row in matrix:
    for value in row:
        total += value

print("Sum =", total)
```

## Practice Problems

1. Print square star pattern
2. Print right triangle pattern
3. Print inverted triangle
4. Print number triangle
5. Find sum of list elements
```python
nums = [2, 4, 6, 8]
print(sum(nums))
```

6. Find largest element in a list
```python
nums = [5, 9, 2, 11]
largest = nums[0]
for x in nums:
    if x > largest:
        largest = x
print(largest)
```

7. Count even numbers in a list
```python
nums = [1, 2, 3, 4, 6]
count = 0
for x in nums:
    if x % 2 == 0:
        count += 1
print(count)
```

8. Reverse a list
```python
nums = [1, 2, 3, 4]
print(nums[::-1])
```

9. Count vowels in a string
```python
text = input()
count = 0
for ch in text.lower():
    if ch in "aeiou":
        count += 1
print(count)
```

10. Count words in a sentence
```python
text = input()
words = text.split()
print(len(words))
```

11. Remove spaces from string
```python
text = input()
print(text.replace(" ", ""))
```

12. Check anagram using sorting
```python
a = input()
b = input()
print(sorted(a) == sorted(b))
```

13. Print matrix row wise
14. Print matrix column wise
15. Find row sum in matrix
```python
matrix = [[1, 2], [3, 4]]
for row in matrix:
    print(sum(row))
```

## Coding Exercises

### Easy
- Sum of list elements
- Count vowels
- Print simple star pattern

### Medium
- Reverse string
- Largest element in list
- Matrix sum

### Challenge
- Anagram check
- Transpose of matrix
- Pyramid pattern

## Mini Assignment
- Build 5 patterns and explain row/column logic in words
- Take a sentence as input and print:
  - number of words
  - number of vowels
  - reversed sentence

## Interview Tips
- In pattern questions, speak row by row
- In list questions, mention indexing clearly
- In string questions, tell whether you are comparing, counting, or building a new string
- In matrix questions, explain rows and columns before coding

## Quick Revision Summary
- Patterns are mainly nested loops
- Lists store many values together
- Strings are text and support indexing
- Matrices are lists inside lists

---

# DAY 3
## Topics
- Searching
- Sorting
- Functions
- Recursion

## Morning Session (Theory Plan)
- Search basics and when to use each type
- Sorting methods step by step
- Why functions make code cleaner
- Recursion as a function calling itself

## Afternoon Session (Hands-on Plan)
- Dry run linear and binary search
- Visual pass-by-pass sorting practice
- Write reusable functions
- Trace recursive calls on paper

## 1. Searching

### Linear Search

#### What it is
Check elements one by one from start to end.

#### Why we use it
Simple and works on any list.

#### Dry Run
Find `7` in `[2, 5, 7, 9]`
- check 2 -> no
- check 5 -> no
- check 7 -> yes

#### Python Code
```python
nums = [2, 5, 7, 9]
target = 7
found = False

for i in range(len(nums)):
    if nums[i] == target:
        print("Found at index", i)
        found = True
        break

if not found:
    print("Not found")
```

### Binary Search

#### What it is
Search in a sorted list by checking the middle element.

#### Why we use it
Much faster for sorted data.

#### Think Like This
Like searching a word in a dictionary.
You do not start from page 1.
You open near the middle.

#### Dry Run
Find `8` in `[2, 4, 6, 8, 10]`
- middle = 6
- 8 is greater, move right
- middle = 8
- found

#### Python Code
```python
nums = [2, 4, 6, 8, 10]
target = 8
low = 0
high = len(nums) - 1

while low <= high:
    mid = (low + high) // 2

    if nums[mid] == target:
        print("Found at index", mid)
        break
    elif nums[mid] < target:
        low = mid + 1
    else:
        high = mid - 1
else:
    print("Not found")
```

## Comparison
- Linear search: simple, no sorting needed
- Binary search: faster, but list must be sorted

## 2. Sorting

### Bubble Sort

#### What it is
Big values slowly move to the end, like bubbles rising up.

#### Step-by-step on `[5, 3, 1]`
- Compare 5 and 3 -> swap -> `[3, 5, 1]`
- Compare 5 and 1 -> swap -> `[3, 1, 5]`
- Compare 3 and 1 -> swap -> `[1, 3, 5]`

#### Python Code
```python
nums = [5, 3, 1, 4]
n = len(nums)

for i in range(n):
    for j in range(0, n - i - 1):
        if nums[j] > nums[j + 1]:
            nums[j], nums[j + 1] = nums[j + 1], nums[j]

print(nums)
```

### Selection Sort

#### What it is
Pick the smallest element and place it in the correct position.

#### Python Code
```python
nums = [5, 3, 1, 4]
n = len(nums)

for i in range(n):
    min_index = i
    for j in range(i + 1, n):
        if nums[j] < nums[min_index]:
            min_index = j
    nums[i], nums[min_index] = nums[min_index], nums[i]

print(nums)
```

### Insertion Sort

#### What it is
Take one element and insert it into the correct place in the already sorted left part.

#### Real-life Analogy
Like arranging playing cards in your hand.

#### Python Code
```python
nums = [5, 3, 1, 4]

for i in range(1, len(nums)):
    key = nums[i]
    j = i - 1

    while j >= 0 and nums[j] > key:
        nums[j + 1] = nums[j]
        j -= 1

    nums[j + 1] = key

print(nums)
```

## 3. Functions

### What it is
A function is a reusable block of code.

### Why we use it
Write once, use many times.

### Python Code
```python
def greet(name):
    print("Hello", name)

greet("Ravi")
greet("Anita")
```

### Output Explanation
Same logic is reused for different names.

## 4. Recursion

### What it is
A function calling itself.

### Why we use it
Useful when a problem can be broken into smaller versions of the same problem.

### Recursion Story
Think of climbing stairs.
To reach step 5, you first reach step 4.
To reach step 4, you first reach step 3.

### Important Rule
There must be a stopping point.
This is called the base case.

### Factorial Using Recursion

#### Dry Run for `factorial(4)`
- `factorial(4)` = `4 * factorial(3)`
- `factorial(3)` = `3 * factorial(2)`
- `factorial(2)` = `2 * factorial(1)`
- `factorial(1)` = `1`
- return back upward:
  - `2 * 1 = 2`
  - `3 * 2 = 6`
  - `4 * 6 = 24`

#### Python Code
```python
def factorial(n):
    if n == 1:
        return 1
    return n * factorial(n - 1)

print(factorial(4))
```

## Practice Problems

1. Linear search
2. Binary search
3. Bubble sort
4. Selection sort
5. Insertion sort
6. Function to find square of a number
```python
def square(n):
    return n * n

print(square(5))
```

7. Function to check even or odd
```python
def is_even(n):
    return n % 2 == 0

print(is_even(6))
```

8. Recursive sum of first `n` numbers
```python
def total(n):
    if n == 1:
        return 1
    return n + total(n - 1)

print(total(5))
```

9. Recursive power
```python
def power(a, b):
    if b == 0:
        return 1
    return a * power(a, b - 1)

print(power(2, 3))
```

10. Find smallest element in list
11. Count occurrences of target in list
12. Binary search using a function

## Coding Exercises

### Easy
- Function for sum of two numbers
- Linear search
- Smallest number in list

### Medium
- Binary search
- Bubble sort
- Recursive sum

### Challenge
- Recursive Fibonacci
- Sort list in descending order
- Search target in sorted list and return insertion position

## Mini Assignment
- Write one program that shows:
  - linear search
  - binary search
  - bubble sort
- Ask students to explain which one is faster and why

## Interview Tips
- In binary search, always say “works on sorted list”
- In recursion, always mention base case
- In sorting, explain what changes after each pass
- Use functions to keep code clean in interviews

## Quick Revision Summary
- Linear search checks one by one
- Binary search checks middle and reduces search area
- Sorting arranges data in order
- Functions avoid repetition
- Recursion means function calling itself with smaller input

---

# DAY 4
## Topics
- References in Python
- Mathematical Problems
- Built-in Functions and Libraries

## Morning Session (Theory Plan)
- Python variables and memory references
- Common math problems used in interviews
- Useful built-ins for faster coding
- Helpful libraries like `math` and `collections`

## Afternoon Session (Hands-on Plan)
- Show list reference behavior
- Solve GCD, LCM, power, and related math questions
- Practice using `list`, `set`, `dict`, and `Counter`

## 1. References in Python

### What it is
In Python, variables do not hold the actual box of data in a simple way.
They point to the data.

### Real-life Analogy
Think of a house and its address.
The house is the data.
The address is the reference.
Two people can have the same address written on paper.

### Why we use it
This helps us understand why changing one list can affect another variable if both point to the same list.

### Dry Run
```python
a = [1, 2, 3]
b = a
b[0] = 99
```

- `a` and `b` point to the same list
- changing through `b` also changes `a`

### Python Code
```python
a = [1, 2, 3]
b = a

b[0] = 99

print("a =", a)
print("b =", b)
```

### Safe Copy
```python
a = [1, 2, 3]
b = a.copy()

b[0] = 99

print("a =", a)
print("b =", b)
```

## 2. Mathematical Problems

### GCD

#### What it is
Greatest Common Divisor means the biggest number that divides both numbers exactly.

#### Dry Run for 12 and 18
Factors of 12: 1, 2, 3, 4, 6, 12
Factors of 18: 1, 2, 3, 6, 9, 18
Greatest common factor is 6

#### Python Code
```python
a = int(input())
b = int(input())

while b != 0:
    a, b = b, a % b

print("GCD =", a)
```

### LCM

#### What it is
Least Common Multiple means the smallest number that both numbers can divide.

#### Formula
`LCM = (a * b) // GCD`

#### Python Code
```python
def gcd(a, b):
    while b != 0:
        a, b = b, a % b
    return a

a = int(input())
b = int(input())

lcm = (a * b) // gcd(a, b)
print("LCM =", lcm)
```

### Power

#### What it is
`2^3` means `2 * 2 * 2`

#### Python Code
```python
base = int(input())
exp = int(input())
result = 1

for _ in range(exp):
    result *= base

print(result)
```

## 3. Built-in Functions and Useful Libraries

## `list`
Useful for ordered data
```python
nums = [3, 1, 4]
print(len(nums))
print(max(nums))
print(min(nums))
print(sum(nums))
```

## `set`
Useful for unique values
```python
nums = [1, 2, 2, 3, 3, 3]
print(set(nums))
```

## `dict`
Useful for key-value pairs
```python
student = {"name": "Asha", "marks": 85}
print(student["name"])
```

## `Counter`
Useful for frequency counting
```python
from collections import Counter

text = "banana"
count = Counter(text)
print(count)
```

## `math` library
```python
import math

print(math.sqrt(25))
print(math.ceil(4.2))
print(math.floor(4.8))
```

## Practical Interview Usage
- Use `set()` to remove duplicates quickly
- Use `Counter` for frequency-based questions
- Use `dict` for counting and mapping
- Use `sum`, `max`, `min` when allowed to keep code short

## Practice Problems

1. Find GCD
2. Find LCM
3. Find power without using `**`
4. Check perfect number
```python
num = int(input())
total = 0
for i in range(1, num):
    if num % i == 0:
        total += i
print("Perfect" if total == num else "Not Perfect")
```

5. Find all divisors
6. Remove duplicates from list
```python
nums = [1, 2, 2, 3, 4, 4]
print(list(set(nums)))
```

7. Count frequency using dictionary
```python
nums = [1, 2, 2, 3]
freq = {}
for x in nums:
    freq[x] = freq.get(x, 0) + 1
print(freq)
```

8. Count frequency using `Counter`
```python
from collections import Counter
nums = [1, 2, 2, 3]
print(Counter(nums))
```

9. Find second largest element
10. Find common elements in two lists
```python
a = [1, 2, 3, 4]
b = [3, 4, 5]
print(list(set(a) & set(b)))
```

## Coding Exercises

### Easy
- GCD
- Power
- Remove duplicates

### Medium
- Frequency counting
- Common elements
- Perfect number

### Challenge
- Second largest without sorting
- Check coprime numbers
- Use dictionary to count words in a sentence

## Mini Assignment
- Compare frequency counting using:
  - normal dictionary
  - `Counter`
- Explain which one is easier and why

## Interview Tips
- In Python interviews, clean code matters
- Built-ins save time, but understand the logic too
- If asked for manual logic, do not depend only on built-ins
- Explain reference behavior clearly using list example

## Quick Revision Summary
- Variables can refer to the same object
- Use `.copy()` when needed
- GCD and LCM are common interview math questions
- Python built-ins make coding faster and cleaner

---

# DAY 5
## Topics
- Time Complexity
- Optimization Techniques
- Bit Manipulation

## Morning Session (Theory Plan)
- Basic idea of time complexity
- How to compare slow and fast approaches
- Simple optimization mindset
- Binary numbers and bit operations

## Afternoon Session (Hands-on Plan)
- Compare nested loops vs better approaches
- Solve optimized interview problems
- Practice binary conversion and bit logic

## 1. Time Complexity

### What it is
Time complexity tells us how the running time grows when input grows.

### Simple Analogy
If 10 students submit papers, checking all papers is easy.
If 10,000 students submit papers, the same method may become slow.

### Why we use it
In interviews, the answer is not just “works”.
It should also be “works efficiently”.

## Big-O in Simple Terms
- `O(1)` : same work every time
- `O(n)` : work grows with input size
- `O(n^2)` : very slow for big input because of nested loops

### Examples
- Accessing one list element: `O(1)`
- Checking every element once: `O(n)`
- Two nested loops over same list: `O(n^2)`

## 2. Optimization Techniques

### Before vs After Example: Find Duplicate

#### Slow Approach
Check every pair
```python
nums = [1, 2, 3, 2]
found = False

for i in range(len(nums)):
    for j in range(i + 1, len(nums)):
        if nums[i] == nums[j]:
            found = True

print(found)
```

#### Better Approach
Use a set
```python
nums = [1, 2, 3, 2]
seen = set()
found = False

for x in nums:
    if x in seen:
        found = True
        break
    seen.add(x)

print(found)
```

### Think Like This
- Can I avoid repeating work?
- Can I store something to save time later?
- Can I sort first?
- Can I use `set` or `dict`?

## 3. Bit Manipulation

### Binary Basics
Computers store data in binary: only `0` and `1`

Example:
- Decimal `5` = Binary `101`
- Decimal `6` = Binary `110`

### Common Bit Operators
- `&` AND
- `|` OR
- `^` XOR
- `~` NOT
- `<<` left shift
- `>>` right shift

### What it is
Bit manipulation means solving problems using binary-level operations.

### Why we use it
Some interview questions become very short and fast using bits.

## Even or Odd Using Bit

### Logic
If last bit is `0`, number is even.
If last bit is `1`, number is odd.

### Python Code
```python
num = int(input())

if num & 1:
    print("Odd")
else:
    print("Even")
```

## Swap Two Numbers Using XOR
```python
a = 5
b = 3

a = a ^ b
b = a ^ b
a = a ^ b

print(a, b)
```

## Check Power of 2

### Trick
A power of 2 has only one `1` bit.

### Python Code
```python
num = int(input())

if num > 0 and (num & (num - 1)) == 0:
    print("Power of 2")
else:
    print("Not Power of 2")
```

## Practice Problems

1. Explain `O(1)`, `O(n)`, `O(n^2)` in your own words
2. Find duplicate using nested loops
3. Find duplicate using set
4. Count frequency using dictionary
5. Find first non-repeating character
```python
from collections import Counter

text = input()
count = Counter(text)

for ch in text:
    if count[ch] == 1:
        print(ch)
        break
```

6. Check even/odd using bit
7. Multiply by 2 using left shift
```python
n = int(input())
print(n << 1)
```

8. Divide by 2 using right shift
```python
n = int(input())
print(n >> 1)
```

9. Check power of 2
10. Count set bits
```python
num = int(input())
count = 0

while num > 0:
    count += num & 1
    num >>= 1

print(count)
```

## Coding Exercises

### Easy
- Even/odd using bit
- Multiply by 2
- Divide by 2

### Medium
- Count set bits
- Check power of 2
- Find duplicate using set

### Challenge
- Single number in list where every other number appears twice
- Optimize pair-checking problem using dictionary/set
- Compare two solutions and discuss time complexity

## Mini Assignment
- Take 5 interview problems already learned and ask students to say:
  - brute force approach
  - better approach
  - expected time complexity

## Interview Tips
- First give a working idea
- Then ask: “Can we optimize it?”
- Use Big-O words in simple language
- In bit problems, mention binary representation clearly

## Quick Revision Summary
- Time complexity is about growth of running time
- Optimization means avoiding unnecessary work
- `set` and `dict` are common interview tools
- Bit manipulation uses binary tricks for faster solutions

---

# Final Instructor Notes

## Teaching Strategy
- Start with paper dry runs before code
- Encourage students to speak their logic aloud
- Keep one concept per board/screen
- Solve one easy, one medium, one interview-style problem for each topic
- Revisit previous-day topics daily for 15 minutes

## Daily Warm-up Suggestion
- 3 quick revision questions
- 1 output prediction question
- 1 small coding task

## Final Mock Interview Plan
- Ask student to explain one program in plain English
- Give one number problem
- Give one string/list problem
- Ask one optimization question
- Ask one function or recursion question

## Confidence Message for Students
Programming is not about being fast on day one.
It is about thinking clearly, practicing small steps, and improving daily.
If you can dry run a problem, you can slowly learn to code it too.

