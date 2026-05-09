# Advanced 5-Day Python Placement Training Program

Trainer Manual

Audience: Third-year engineering students with basic programming syntax knowledge who need to become placement-ready for coding rounds and technical interviews.

Primary goal: Move students from "I can write code" to "I can solve unfamiliar interview problems with structure, clarity, and optimization awareness."

---

# Contents

1. Program Design Principles
2. Trainer Delivery Framework
3. Day 1: Core Programming Logic
4. Day 2: Patterns, Arrays, Strings
5. Day 3: Searching, Sorting, Functions, Recursion
6. Day 4: Advanced Python for Placements
7. Day 5: Optimization and Interview Thinking
8. Final Mock Interview Framework

---

# Program Design Principles

## What this course is optimizing for
- Logic building under pressure
- Recognizing common interview patterns
- Moving from brute force to optimized code
- Clean Python implementation
- Clear verbal explanation during interviews
- Strong dry-run discipline

## What this course is not
- A syntax tutorial from zero
- A library-heavy Python course
- A competitive programming tricks-only course

## Core teaching philosophy
Every good interview solution should pass through these stages:
1. Understand the problem clearly
2. Identify inputs, outputs, and constraints
3. Start with a brute force solution
4. Measure why brute force is weak
5. Improve using a pattern or data structure
6. Write clean code
7. Analyze complexity
8. Discuss edge cases

## Golden interview line to teach students
"I’ll start with a straightforward approach first, then improve it if constraints demand optimization."

---

# Trainer Delivery Framework

## Standard teaching flow for each major topic
1. Intuition
2. Real interview framing
3. Brute force approach
4. Why brute force may fail
5. Optimized idea
6. Dry run
7. Python implementation
8. Complexity
9. Edge cases
10. Interview follow-up variations

## What the trainer should repeatedly ask
- What is the simplest correct solution?
- What is repeated work here?
- Can we reduce the search space?
- Can we precompute or store something?
- Does order matter?
- Do we need all results or just one answer?

## Common student failure patterns
- Jumping to code too early
- Writing syntax before defining logic
- Ignoring edge cases
- Assuming optimization before understanding the base problem
- Forgetting to justify time complexity

## Board explanation sequence
For problem-solving sessions, use this order:
1. Problem statement
2. Sample input/output
3. Observations
4. Brute force logic
5. Optimization trigger
6. Final algorithm
7. Code
8. Complexity

---

# DAY 1 — Core Programming Logic

## Day Objective
Students should strengthen control over:
- expression building
- condition-based logic
- loop reasoning
- number theory basics
- brute force vs mathematical optimization

## Morning Session Plan

### Trainer opening
What to say:
"You already know syntax. Today we improve how you think with syntax."

"Most coding-round failures do not happen because students forget Python keywords. They happen because students do not structure the logic."

### Morning teaching blocks
1. Input/output discipline and validation mindset
2. Expressions and operators as logic tools
3. Loop mastery
4. Digit-based problems
5. Number theory intuition

## Afternoon Session Plan
- Guided solving: prime, reverse, palindrome, Armstrong
- Optimization discussion: prime range, Fibonacci, factorial
- Timed coding set
- Debugging round

---

## Topic 1: Input/Output Mastery

### Theory
At interview level, input/output is not difficult, but sloppy handling causes bugs.

Students must understand:
- type expectations
- input validation
- clean variable naming
- avoiding repeated conversions

### Interview perspective
Even simple tasks become error-prone if input types are mishandled.

### Brute force thinking mistake
Students often write code assuming perfect input and then mix strings with integers.

### Better approach
Normalize input early.

### Example
```python
n = int(input().strip())
```

### Trainer note
Stress that `strip()` is often good hygiene when reading textual input.

### Common mistakes
- forgetting numeric conversion
- naming variables `a`, `b`, `c` for everything
- re-reading input unnecessarily

### Frequently asked student doubt
Q: "Do interviews really care about input code?"
A: They care less about format and more about correctness, but sloppy input often reveals weak coding habits.

---

## Topic 2: Operators and Expressions

### Intuition
Operators are not just for calculation. They form conditions, simplify updates, and encode logic.

### Interview perspective
Students who misuse `%`, `//`, `==`, `and`, `or` often fail basic screening problems.

### Key operator uses for placements
- `%` for divisibility and digit extraction
- `//` for shrinking numbers
- `**` for powers
- comparison operators for condition construction
- logical operators for compound filtering

### Whiteboard emphasis
Show:
```python
if n % 2 == 0 and n > 10:
```
Then ask students to explain it in English.

### Teaching tip
If they cannot explain the expression in English, they do not fully understand it.

---

## Topic 3: Conditional Statements

### Intuition
Conditions partition the problem space.
Interview logic often reduces to:
- classify input
- branch based on property
- handle edge cases explicitly

### Real interview perspective
Interviewers watch whether students cover:
- negative numbers
- zero
- boundary values

### Example discussion
Check whether a number is positive, negative, or zero.

#### Brute force
Just start writing `if num > 0`.

#### Better reasoning
There are 3 disjoint categories:
- greater than 0
- less than 0
- equal to 0

### Code
```python
num = int(input())

if num > 0:
    print("Positive")
elif num < 0:
    print("Negative")
else:
    print("Zero")
```

### Common mistakes
- overlapping conditions
- missing edge category
- using multiple `if` when `elif` is more appropriate

---

## Topic 4: Loop Mastery

### Intuition
Loops are where interview logic lives.
Students must distinguish:
- fixed-iteration loops
- condition-controlled loops
- loops that accumulate
- loops that search
- loops that transform state

### Interview perspective
Most Day 1 number problems are really loop-control tests.

### Brute force mistake pattern
Students often know what they want to repeat but do not know:
- starting state
- stopping condition
- update rule

### Trainer framework
Before any loop, ask students to state:
1. Initial value
2. Loop condition
3. Update rule
4. What changes per iteration

---

## Topic 5: Number Theory Basics

### Why this matters
Placement rounds frequently use number properties to test:
- divisibility thinking
- digit extraction
- factor logic
- mathematical optimization

### Core sub-skills
- factors and multiples
- digit extraction using `% 10`
- digit removal using `// 10`
- divisor checks
- square root optimization

---

## Major Problem 1: Prime Number Check

### Problem understanding
Determine whether a given integer `n` is prime.

### Input/Output analysis
- Input: integer `n`
- Output: boolean-style answer or text classification

### Constraint thinking
If `n` is large, checking all values from 2 to `n-1` is wasteful.

### Pattern identification
This is a divisibility problem with symmetry in factor pairs.

## Brute force approach
Check all integers from 2 to `n-1`.

### Brute force runnable program
```python
n = int(input("Enter a number: "))

if n <= 1:
    print("Not Prime")
else:
    is_prime = True

    for i in range(2, n):
        if n % i == 0:
            is_prime = False
            break

    if is_prime:
        print("Prime")
    else:
        print("Not Prime")
```

### Sample input
```text
11
```

### Sample output
```text
Prime
```

### Why brute force works
If any number divides `n`, it is composite.

### Why brute force is weak
It performs unnecessary checks.
If `n = 101`, checking divisibility by 80 or 90 gives no extra value after smaller factors already failed.

## Optimization insight
Factors come in pairs.
If `n = a * b` and both `a` and `b` were greater than `sqrt(n)`, then `a * b` would exceed `n`.
So at least one factor must be less than or equal to `sqrt(n)`.

### Optimized strategy
Check divisibility only up to `int(sqrt(n))`.

### Dry run for `n = 29`
- sqrt(29) is a little above 5
- check 2, 3, 4, 5
- none divide
- therefore prime

### Dry run table for `n = 29`

| i | `29 % i` | Action |
|---:|---:|---|
| 2 | 1 | continue |
| 3 | 2 | continue |
| 4 | 1 | continue |
| 5 | 4 | continue |

Result: Prime

### Python implementation
```python
n = int(input("Enter a number: "))

if n <= 1:
    print("Not Prime")
else:
    is_prime = True
    limit = int(n ** 0.5)

    for i in range(2, limit + 1):
        if n % i == 0:
            is_prime = False
            break

    if is_prime:
        print("Prime")
    else:
        print("Not Prime")
```

### Sample input
```text
29
```

### Sample output
```text
Prime
```

### Time complexity
- Brute force: `O(n)`
- Optimized: `O(sqrt(n))`

### Space complexity
`O(1)`

### Edge cases
- `n <= 1` is not prime
- `n = 2` is prime
- negative inputs are not prime

### Interview discussion points
- Why `sqrt(n)` is enough
- Why `<= 1` must be handled separately

### Common mistakes
- treating 1 as prime
- looping to `n` instead of `sqrt(n)`
- forgetting inclusive end at `limit + 1`

### Student likely doubt
Q: "Why do we not check beyond sqrt?"
A: Because any larger factor would require a smaller partner factor already checked.

---

## Major Problem 2: Prime Numbers in a Range

### Problem understanding
Print all primes between `L` and `R`.

### Brute force
For every number in range, test divisibility from 2 to `n-1`.

### Limitation
This becomes too slow for large ranges.

### Optimization strategy
Use the optimized prime check for each number.

### Code
```python
def is_prime(n):
    if n <= 1:
        return False
    for i in range(2, int(n ** 0.5) + 1):
        if n % i == 0:
            return False
    return True

def primes_in_range(left, right):
    result = []
    for num in range(left, right + 1):
        if is_prime(num):
            result.append(num)
    return result

left = int(input("Enter range start: "))
right = int(input("Enter range end: "))

print("Primes:", primes_in_range(left, right))
```

### Sample input
```text
10
30
```

### Sample output
```text
Primes: [11, 13, 17, 19, 23, 29]
```

### Dry run for range `10` to `15`

| Number | Prime? |
|---:|---|
| 10 | No |
| 11 | Yes |
| 12 | No |
| 13 | Yes |
| 14 | No |
| 15 | No |

### Complexity
Approximately `O((R-L+1) * sqrt(R))`

### Interview follow-up
Ask students when sieve-based methods would be better, even if not implemented today.

---

## Major Problem 3: Reverse Number

### Pattern identification
This is a digit extraction and reconstruction problem.

### Brute force mental model
Take last digit repeatedly and build answer from left to right via multiplication.

### Code
```python
n = int(input("Enter a number: "))
rev = 0
sign = -1 if n < 0 else 1
temp = abs(n)

if temp == 0:
    print("Reverse = 0")
else:
    while temp > 0:
        digit = temp % 10
        rev = rev * 10 + digit
        temp //= 10

    print("Reverse =", sign * rev)
```

### Dry run for `1234`
- rev = 0
- digit 4 -> rev = 4
- digit 3 -> rev = 43
- digit 2 -> rev = 432
- digit 1 -> rev = 4321

### Dry run table for `1234`

| temp | digit | rev |
|---:|---:|---:|
| 1234 | 4 | 4 |
| 123 | 3 | 43 |
| 12 | 2 | 432 |
| 1 | 1 | 4321 |

### Sample input
```text
1234
```

### Sample output
```text
Reverse = 4321
```

### Complexity
`O(d)` where `d` is number of digits

### Edge cases
- `0`
- negative numbers
- trailing zeroes such as `1200`

---

## Major Problem 4: Palindrome Number

### Intuition
A number is palindrome if it matches its reverse.

### Brute force
Convert to string and compare with reverse.

### Brute force runnable program
```python
n = input("Enter a number: ")

if n == n[::-1]:
    print("Palindrome")
else:
    print("Not Palindrome")
```

### Sample input
```text
1221
```

### Sample output
```text
Palindrome
```

### Optimized numeric approach
Reverse digits numerically and compare.

### Discussion point
In Python, string solution is valid and often concise, but interviewers may ask for numeric logic.

### Numeric solution
```python
n = int(input("Enter a number: "))

if n < 0:
    print("Not Palindrome")
else:
    original = n
    rev = 0

    while n > 0:
        rev = rev * 10 + (n % 10)
        n //= 10

    if original == rev:
        print("Palindrome")
    else:
        print("Not Palindrome")
```

### Dry run for `1221`

| n | digit | rev |
|---:|---:|---:|
| 1221 | 1 | 1 |
| 122 | 2 | 12 |
| 12 | 2 | 122 |
| 1 | 1 | 1221 |

### Sample input
```text
1221
```

### Sample output
```text
Palindrome
```

### Complexity
`O(d)`

---

## Major Problem 5: Armstrong Number

### Problem understanding
An Armstrong number equals the sum of each digit raised to the power of total digits.

### Brute force pattern
Extract each digit, raise it, sum it.

### Code
```python
n = int(input("Enter a number: "))
original = n
digits = len(str(n))
total = 0
temp = n

while temp > 0:
    digit = temp % 10
    total += digit ** digits
    temp //= 10

if total == original:
    print("Armstrong")
else:
    print("Not Armstrong")
```

### Dry run for `153`

| temp | digit | `digit ** 3` | total |
|---:|---:|---:|---:|
| 153 | 3 | 27 | 27 |
| 15 | 5 | 125 | 152 |
| 1 | 1 | 1 | 153 |

### Sample input
```text
153
```

### Sample output
```text
Armstrong
```

### Edge case
If handling `0`, decide explicitly. `0` is Armstrong because `0^1 = 0`.

### Teaching tip
Differentiate 3-digit textbook Armstrong from generalized Armstrong.

---

## Major Problem 6: Fibonacci

### Problem understanding
Find nth Fibonacci number or print series.

### Brute force recursive thinking
`fib(n) = fib(n-1) + fib(n-2)`

### Brute force recursive runnable program
```python
def fib(n):
    if n == 0:
        return 0
    if n == 1:
        return 1
    return fib(n - 1) + fib(n - 2)

n = int(input("Enter n: "))
print("Fibonacci =", fib(n))
```

### Why brute force recursion is weak
Huge repeated work.

### Optimization strategy
Use iterative rolling variables.

### Iterative optimized code
```python
n = int(input("Enter n: "))

if n == 0:
    print("Fibonacci = 0")
elif n == 1:
    print("Fibonacci = 1")
else:
    prev2, prev1 = 0, 1
    for _ in range(2, n + 1):
        curr = prev1 + prev2
        prev2, prev1 = prev1, curr
    print("Fibonacci =", prev1)
```

### Dry run for `n = 6`

| Step | prev2 | prev1 | curr |
|---:|---:|---:|---:|
| start | 0 | 1 | - |
| 2 | 1 | 1 | 1 |
| 3 | 1 | 2 | 2 |
| 4 | 2 | 3 | 3 |
| 5 | 3 | 5 | 5 |
| 6 | 5 | 8 | 8 |

### Sample input
```text
6
```

### Sample output
```text
Fibonacci = 8
```

### Complexity
- Recursive naive: exponential
- Iterative optimized: `O(n)` time, `O(1)` space

### Interview perspective
This is a good place to teach "same recurrence, different implementation efficiency."

---

## Major Problem 7: Factorial

### Brute force
Recursive factorial.

### Optimization discussion
Unlike Fibonacci, factorial recursion does not duplicate subproblems.
Its recursion is acceptable conceptually but iterative version avoids recursion overhead.

### Iterative code
```python
n = int(input("Enter a number: "))
result = 1

for i in range(2, n + 1):
    result *= i

print("Factorial =", result)
```

### Dry run for `n = 5`

| i | result before | result after |
|---:|---:|---:|
| 2 | 1 | 2 |
| 3 | 2 | 6 |
| 4 | 6 | 24 |
| 5 | 24 | 120 |

### Sample input
```text
5
```

### Sample output
```text
Factorial = 120
```

### Recursive code
```python
def factorial_recursive(n):
    if n <= 1:
        return 1
    return n * factorial_recursive(n - 1)

n = int(input("Enter a number: "))
print("Factorial =", factorial_recursive(n))
```

### Comparison
| Approach | Time | Space | Discussion |
|---|---:|---:|---|
| Iterative | `O(n)` | `O(1)` | More practical |
| Recursive | `O(n)` | `O(n)` | Good for recursion understanding |

---

## Day 1 Practice Questions

### Easy
1. Count digits in a number
2. Sum of digits
3. Product of digits
4. Check even/odd
5. Check positive/negative/zero

### Medium
1. Reverse number
2. Palindrome number
3. Factorial
4. Prime check with optimization
5. Strong number

### Interview-level
1. Prime range
2. Armstrong numbers in a range
3. nth Fibonacci optimized
4. Count primes in a range
5. Sum of prime digits in a number

## Mini Assignment
- Build a menu-driven number toolkit for:
  - reverse
  - palindrome
  - prime
  - Armstrong
  - factorial

## Timed Coding Test
- 25 minutes
- Problems:
  1. Prime check optimized
  2. Reverse number
  3. nth Fibonacci

## Debugging Exercises
1. Prime code that treats 1 as prime
2. Reverse-number code that forgets `rev * 10`
3. Factorial code with wrong starting value

---

# DAY 2 — Patterns, Arrays, Strings

## Day Objective
Students should learn to recognize:
- nested-loop structure
- row-column symmetry
- array traversal patterns
- string counting and transformation patterns
- frequency-map thinking

## Morning Session Plan
- Pattern derivation methodology
- Lists and transformation operations
- String internals and optimized manipulation

## Afternoon Session Plan
- Matrix traversals
- Frequency problems
- Sliding window introduction
- Spiral and diagonal thinking

---

## Topic 1: Pattern Problems

### Why pattern problems matter
Patterns train nested-loop intuition, symmetry detection, and space management.
They are less about stars and more about control logic.

### Systematic approach to patterns
Teach students to ask:
1. How many rows?
2. What is printed in each row?
3. Are spaces involved?
4. Is the count increasing or decreasing?
5. Is there mirror symmetry?

### Board explanation sequence
1. Draw row numbers
2. Mark spaces count
3. Mark symbols count
4. Convert into expressions

## Example: Centered Pyramid

```text
   *
  ***
 *****
*******
```

### Derivation
For row `i` starting at 1:
- spaces = `n - i`
- stars = `2*i - 1`

### Code
```python
def pyramid(n):
    for i in range(1, n + 1):
        spaces = n - i
        stars = 2 * i - 1
        print(" " * spaces + "*" * stars)

n = int(input("Enter number of rows: "))
pyramid(n)
```

### Sample input
```text
4
```

### Sample output
```text
   *
  ***
 *****
*******
```

### Common struggle point
Students often memorize formulas without deriving them.

### Trainer teaching tip
Make them fill a row table before coding:

| Row | Spaces | Stars |
|---|---:|---:|
| 1 | 3 | 1 |
| 2 | 2 | 3 |
| 3 | 1 | 5 |
| 4 | 0 | 7 |

---

## Topic 2: Lists and List Manipulation

### Theory
Lists are dynamic arrays in Python with powerful built-in operations.

### Interview perspective
Students must be able to:
- traverse
- update
- accumulate
- filter
- reverse
- track min/max

### Brute force vs cleaner Python
Manual traversal is good for logic clarity.
Built-ins are good when the interview allows concise solutions.

### Major Problem: Find second largest

#### Brute force
Sort and pick second last distinct value.

#### Limitation
Sorting changes order and costs more than necessary.

#### Optimized approach
Track largest and second largest in one pass.

#### Code
```python
nums = list(map(int, input("Enter numbers separated by space: ").split()))

largest = float("-inf")
second = float("-inf")

for x in nums:
    if x > largest:
        second = largest
        largest = x
    elif largest > x > second:
        second = x

if second == float("-inf"):
    print("No second largest distinct element")
else:
    print("Second largest =", second)
```

### Sample input
```text
5 1 9 2 9 7
```

### Sample output
```text
Second largest = 7
```

### Complexity
- sort-based: `O(n log n)`
- one-pass: `O(n)`

### Edge cases
- duplicate max values only
- fewer than 2 distinct elements

---

## Topic 3: Strings

### String internals
Strings are immutable sequences of Unicode characters.

### Interview significance
Strings frequently test:
- indexing
- frequency counting
- substring logic
- window-based reasoning
- normalization

### Major Pattern 1: Frequency counting

#### Problem
Find character frequency in a string.

#### Brute force
For each character, scan entire string and count.

#### Limitation
Repeated work leads to `O(n^2)`.

#### Optimized strategy
Use a dictionary/hash map.

#### Code
```python
s = input("Enter a string: ")
freq = {}

for ch in s:
    freq[ch] = freq.get(ch, 0) + 1

print(freq)
```

### Sample input
```text
banana
```

### Sample output
```text
{'b': 1, 'a': 3, 'n': 2}
```

### Complexity
`O(n)`

### Interview perspective
Hash-map thinking is a major shift from beginner coding to placement coding.

---

## Major Pattern 2: First non-repeating character

### Brute force
For each character, count it again by scanning the whole string.

### Optimized approach
Build frequency map first, then scan original order.

### Code
```python
s = input("Enter a string: ")
freq = {}

for ch in s:
    freq[ch] = freq.get(ch, 0) + 1

answer = None
for ch in s:
    if freq[ch] == 1:
        answer = ch
        break

print("First non-repeating character =", answer)
```

### Sample input
```text
swiss
```

### Sample output
```text
First non-repeating character = w
```

---

## Major Pattern 3: Sliding Window Intro

### Goal
Introduce the idea of maintaining information for a moving substring.

### Example
Length of longest substring without repeating characters.

### Teaching goal
Do not go too deep into advanced windows; introduce why nested rescanning is wasteful.

### Brute force
Generate every substring and test uniqueness.

### Optimized idea
Maintain a moving window and a set/dictionary of seen characters.

### Code
```python
s = input("Enter a string: ")
seen = {}
left = 0
best = 0

for right, ch in enumerate(s):
    if ch in seen and seen[ch] >= left:
        left = seen[ch] + 1
    seen[ch] = right
    best = max(best, right - left + 1)

print("Length =", best)
```

### Sample input
```text
abcabcbb
```

### Sample output
```text
Length = 3
```

### Interview insight
This is often a student's first experience with dynamic two-pointer thinking.

---

## Topic 4: 2D Arrays / Matrices

### Core concepts
- row-major traversal
- column traversal
- diagonal traversal
- boundary-based spiral reasoning

## Major Problem: Diagonal Sum

### Brute force
Traverse entire matrix and check if `i == j`.

### Optimized approach
Directly access diagonal elements.

### Code
```python
n = int(input("Enter size of square matrix: "))
matrix = []

for _ in range(n):
    row = list(map(int, input().split()))
    matrix.append(row)

total = 0
for i in range(len(matrix)):
    total += matrix[i][i]

print("Primary diagonal sum =", total)
```

### Sample input
```text
3
1 2 3
4 5 6
7 8 9
```

### Sample output
```text
Primary diagonal sum = 15
```

### Complexity
- brute force with condition: `O(n^2)`
- direct diagonal: `O(n)`

---

## Major Problem: Spiral Traversal Introduction

### Intuition
Maintain four boundaries:
- top
- bottom
- left
- right

Shrink them after each layer.

### Code
```python
def spiral_order(matrix):
    if not matrix or not matrix[0]:
        return []

    top, bottom = 0, len(matrix) - 1
    left, right = 0, len(matrix[0]) - 1
    result = []

    while top <= bottom and left <= right:

        # Traverse top row
        for col in range(left, right + 1):
            result.append(matrix[top][col])
        top += 1

        # Traverse right column
        for row in range(top, bottom + 1):
            result.append(matrix[row][right])
        right -= 1

        # Traverse bottom row
        if top <= bottom:
            for col in range(right, left - 1, -1):
                result.append(matrix[bottom][col])
            bottom -= 1

        # Traverse left column
        if left <= right:
            for row in range(bottom, top - 1, -1):
                result.append(matrix[row][left])
            left += 1

    return result


rows = int(input("Enter number of rows: "))
cols = int(input("Enter number of columns: "))

matrix = []

print("Enter the matrix row by row:")

for _ in range(rows):
    row = list(map(int, input().split()))

    if len(row) != cols:
        print(f"Please enter exactly {cols} numbers.")
        exit()

    matrix.append(row)

print("Spiral order =", spiral_order(matrix))
```

### Sample input
```text
3
3
1 2 3
4 5 6
7 8 9
```

### Sample output
```text
Spiral order = [1, 2, 3, 6, 9, 8, 7, 4, 5]
```

### Teaching tip
This is a boundary-management problem, not just a nested-loop problem.

---

## Day 2 Practice Questions

### Easy
1. Increasing triangle
2. Decreasing triangle
3. Sum of list elements
4. Reverse string
5. Matrix row sum

### Medium
1. Pyramid pattern
2. Second largest in list
3. Character frequency
4. First non-repeating character
5. Diagonal sum

### Interview-level
1. Longest unique substring length
2. Spiral traversal
3. Anagram check using frequency
4. Matrix transpose
5. Rotate matrix by 90 degrees conceptually

## Mini Assignment
- Pattern sheet with 6 patterns
- Frequency-based string toolkit
- Matrix traversal utility

## Timed Coding Test
1. Centered pyramid
2. Second largest
3. First non-repeating character

## Debugging Exercises
1. Pattern with wrong spaces
2. Frequency code overwriting counts incorrectly
3. Spiral traversal missing boundary checks

---

# DAY 3 — Searching, Sorting, Functions, Recursion

## Day Objective
Students should understand:
- search space reduction
- when sorting is being used as a tool, not just as an algorithm
- function design
- recursion mechanics and backtracking intuition

## Morning Session Plan
- Searching deeply
- Binary search derivation
- Sorting comparisons

## Afternoon Session Plan
- Functions and modular coding
- Recursion and recursive trees
- Backtracking preview

---

## Topic 1: Linear Search

### Intuition
Search without assumptions.

### Interview perspective
Always acceptable when data is unsorted and constraints are small.

### Complexity
`O(n)`

### Limitation
No search space reduction.

---

## Topic 2: Binary Search

### Core intuition
Binary search is not "middle element code." It is "search space halving."

### Search space reduction explanation
At each step, half the remaining candidates become impossible.

### Necessary condition
Data must be sorted or monotonic.

### Major problem: Standard binary search
```python
def binary_search(nums, target):
    left, right = 0, len(nums) - 1

    while left <= right:
        mid = left + (right - left) // 2

        if nums[mid] == target:
            return mid
        if nums[mid] < target:
            left = mid + 1
        else:
            right = mid - 1

    return -1

nums = list(map(int, input("Enter sorted numbers: ").split()))
target = int(input("Enter target: "))
print("Index =", binary_search(nums, target))
```

### Sample input
```text
1 3 5 7 9 11
7
```

### Sample output
```text
Index = 3
```

### Dry run
Use `[1, 3, 5, 7, 9, 11]`, target `7`.

### Time complexity
`O(log n)`

### Edge cases
- empty list
- target absent
- duplicates

### Interview follow-up
- first occurrence
- last occurrence
- lower bound / insertion position

### Common mistakes
- loop condition errors
- wrong pointer update
- using binary search on unsorted list

---

## Topic 3: Sorting Algorithms

## Concept language to teach
- stable: equal elements keep original relative order
- in-place: uses very little extra memory

### Bubble Sort
#### Intuition
Push larger elements right by adjacent swaps.

#### Code
```python
def bubble_sort(nums):
    arr = nums[:]
    n = len(arr)

    for i in range(n):
        swapped = False
        for j in range(0, n - i - 1):
            if arr[j] > arr[j + 1]:
                arr[j], arr[j + 1] = arr[j + 1], arr[j]
                swapped = True
        if not swapped:
            break
    return arr

nums = list(map(int, input("Enter numbers: ").split()))
print("Sorted =", bubble_sort(nums))
```

#### Complexity
- worst: `O(n^2)`
- best with optimization: `O(n)`

### Selection Sort
#### Intuition
Select the smallest remaining element and place it.

```python
def selection_sort(nums):
    arr = nums[:]
    n = len(arr)

    for i in range(n):
        min_index = i
        for j in range(i + 1, n):
            if arr[j] < arr[min_index]:
                min_index = j
        arr[i], arr[min_index] = arr[min_index], arr[i]
    return arr

nums = list(map(int, input("Enter numbers: ").split()))
print("Sorted =", selection_sort(nums))
```

### Insertion Sort
#### Intuition
Grow a sorted left portion by inserting each next item in the correct place.

```python
def insertion_sort(nums):
    arr = nums[:]

    for i in range(1, len(arr)):
        key = arr[i]
        j = i - 1

        while j >= 0 and arr[j] > key:
            arr[j + 1] = arr[j]
            j -= 1

        arr[j + 1] = key

    return arr

nums = list(map(int, input("Enter numbers: ").split()))
print("Sorted =", insertion_sort(nums))
```

### Common sample input for sorting
```text
5 3 1 4
```

### Common sample output for sorting
```text
Sorted = [1, 3, 4, 5]
```

## Sorting comparison table

| Algorithm | Best | Worst | Stable | In-place | Interview Use |
|---|---:|---:|---|---|---|
| Bubble | `O(n)` | `O(n^2)` | Yes | Yes | Logic training |
| Selection | `O(n^2)` | `O(n^2)` | No | Yes | Comparison reasoning |
| Insertion | `O(n)` | `O(n^2)` | Yes | Yes | Good for nearly sorted data |

### Interview discussion
Students should not just memorize complexities. They should explain behavior:
- Bubble does many swaps
- Selection does fewer swaps
- Insertion is strong on nearly sorted arrays

---

## Topic 4: Functions

### Theory
Functions create modularity, improve testability, and help structure interview solutions.

### Interview expectation
Students should:
- choose meaningful names
- avoid giant monolithic code blocks
- separate helper logic cleanly

### Good example
```python
def is_prime(n):
    if n <= 1:
        return False
    for i in range(2, int(n ** 0.5) + 1):
        if n % i == 0:
            return False
    return True

def primes_in_range(left, right):
    return [num for num in range(left, right + 1) if is_prime(num)]

left = int(input("Enter range start: "))
right = int(input("Enter range end: "))
print(primes_in_range(left, right))
```

### Teaching tip
Show how helper functions improve explanation quality in interviews.

---

## Topic 5: Recursion

### Intuition
Recursion is solving a problem using smaller instances of itself.

### Stack frame visualization
Teach each call as a frame that stores:
- local values
- return destination

### Recursive tree visualization
Use Fibonacci to show branch explosion.

### Example: Sum of first n numbers
```python
def sum_n(n):
    if n == 0:
        return 0
    return n + sum_n(n - 1)

n = int(input("Enter n: "))
print("Sum =", sum_n(n))
```

### Example: Fibonacci recursive tree discussion
```python
def fib(n):
    if n <= 1:
        return n
    return fib(n - 1) + fib(n - 2)

n = int(input("Enter n: "))
print("Fibonacci =", fib(n))
```

### Why recursion can be expensive
Repeated overlapping calls.

### Backtracking intuition introduction
Backtracking is recursion plus "choose, explore, undo."
Do not go deep; just plant the concept.

### Common mistakes
- no base case
- wrong smaller subproblem
- not understanding return flow

---

## Day 3 Practice Questions

### Easy
1. Linear search
2. Binary search on sorted list
3. Bubble sort
4. Function to compute gcd
5. Recursive sum

### Medium
1. First occurrence using binary search
2. Selection sort
3. Insertion sort
4. Prime helper function
5. Recursive factorial

### Interview-level
1. Insertion position via binary search
2. Binary search on answer concept discussion
3. Compare all three sorts
4. Recursive Fibonacci complexity discussion
5. Generate subsets intuition discussion

## Mini Assignment
- Build a searching and sorting comparison notebook
- Write helper functions for reused logic

## Timed Coding Test
1. Binary search
2. Insertion sort
3. Recursive factorial

## Debugging Exercises
1. Binary search infinite loop
2. Bubble sort inner loop bound error
3. Recursive missing base case

---

# DAY 4 — Advanced Python for Placements

## Day Objective
Students should become comfortable with:
- Python object behavior
- mutable vs immutable thinking
- hashing-based structures
- collection tools used in coding rounds
- mathematical helpers and optimization

## Morning Session Plan
- Python memory model
- references and object sharing
- dictionaries and sets

## Afternoon Session Plan
- collections module
- pair/frequency problems
- GCD/LCM and modular arithmetic
- fast exponentiation idea

---

## Topic 1: Python Memory Model

### Intuition
Variables are references to objects, not rigid typed boxes like some other languages.

### Mutable vs immutable
- Immutable: int, str, tuple
- Mutable: list, dict, set

### Whiteboard analogy
Two sticky notes can point to the same whiteboard.
If the whiteboard changes, both notes still point to the changed board.

### Example
```python
a = [1, 2, 3]
b = a
b[0] = 99
```

### Interview perspective
This matters when passing lists to functions or copying data.

### Common mistakes
- thinking assignment copies nested objects
- modifying input unintentionally

---

## Topic 2: Hashing Intuition

### Simple explanation
Hashing maps a key to a storage location so lookups are usually fast.

### What trainer should say
"You do not need internal implementation details for placements. You need intuition: dictionaries and sets are often fast because Python uses hash-based lookup."

### Dictionary internals, simply
- keys are hashed
- hash helps find likely location quickly
- collisions are handled internally

### Interview discussion point
Average-case lookup is fast, but hashing still depends on good key behavior.

---

## Topic 3: Dictionaries and Sets

## Major Problem: Duplicate Detection

### Brute force
Compare every pair.

### Limitation
`O(n^2)`

### Optimized approach
Maintain a set of seen values.

### Code
```python
nums = list(map(int, input("Enter numbers: ").split()))
seen = set()
found = False

for x in nums:
    if x in seen:
        found = True
        break
    seen.add(x)

print("Duplicate present =", found)
```

### Sample input
```text
1 2 3 2 5
```

### Sample output
```text
Duplicate present = True
```

### Complexity
Average `O(n)` time, `O(n)` space

### Interview angle
This is a classic "store what you have seen" pattern.

---

## Major Problem: Frequency Counting

### Brute force
Count every value by rescanning.

### Optimized approach
Dictionary or `Counter`.

### Manual dictionary
```python
nums = list(map(int, input("Enter numbers: ").split()))
freq = {}

for x in nums:
    freq[x] = freq.get(x, 0) + 1

print(freq)
```

### Using Counter
```python
from collections import Counter

nums = list(map(int, input("Enter numbers: ").split()))
print(Counter(nums))
```

### Teaching tip
Show both:
- manual method for logic
- `Counter` for production speed

---

## Major Problem: Pair Sum

### Problem understanding
Determine whether two numbers sum to a target.

### Brute force
Check all pairs.

### Limitation
`O(n^2)`

### Optimized approach
For each `x`, check whether `target - x` was seen.

### Code
```python
nums = list(map(int, input("Enter numbers: ").split()))
target = int(input("Enter target sum: "))
seen = set()
found = False

for x in nums:
    if target - x in seen:
        found = True
        break
    seen.add(x)

print("Pair exists =", found)
```

### Sample input
```text
2 7 11 15
9
```

### Sample output
```text
Pair exists = True
```

### Complexity
Average `O(n)` time

### Edge cases
- duplicates may be required
- negative numbers
- pair indices vs just existence

---

## Topic 4: Collections Module

### Must-cover tools
- `Counter`
- `defaultdict`
- `deque` mention if time permits

### defaultdict example
```python
from collections import defaultdict

nums = list(map(int, input("Enter numbers: ").split()))
pos = defaultdict(list)

for i, x in enumerate(nums):
    pos[x].append(i)

print(dict(pos))
```

### Interview discussion
`defaultdict` reduces boilerplate when grouping or building adjacency lists.

---

## Topic 5: Mathematical Problem Solving

## GCD and LCM
Reinforce Euclid's algorithm.

```python
def gcd(a, b):
    while b:
        a, b = b, a % b
    return a

def lcm(a, b):
    return abs(a * b) // gcd(a, b)

a = int(input("Enter first number: "))
b = int(input("Enter second number: "))
print("GCD =", gcd(a, b))
print("LCM =", lcm(a, b))
```

## Modular Arithmetic

### Intuition
When numbers become too large, many problems only need the remainder.

### Example principle
```text
(a + b) % m = ((a % m) + (b % m)) % m
```

### Interview relevance
Used heavily in counting, combinatorics, and overflow-sensitive contexts.

## Fast Exponentiation Idea

### Brute force
Multiply `a` by itself `b` times.

### Limitation
`O(b)`

### Optimized idea
Use repeated squaring.

### Code
```python
base = int(input("Enter base: "))
exp = int(input("Enter exponent: "))
result = 1

while exp > 0:
    if exp % 2 == 1:
        result *= base
    base *= base
    exp //= 2

print("Power =", result)
```

### Sample input
```text
2
10
```

### Sample output
```text
Power = 1024
```

### Complexity
`O(log b)`

### Interview discussion
This is an important example of "use the binary form of exponent."

---

## Day 4 Practice Questions

### Easy
1. Remove duplicates
2. Frequency map
3. Common elements using set intersection
4. GCD
5. LCM

### Medium
1. Duplicate detection
2. Pair sum existence
3. Character frequency with Counter
4. Group indices using defaultdict
5. Fast power

### Interview-level
1. Two-sum returning indices
2. Top-k frequent elements discussion
3. Longest consecutive sequence intuition with set
4. Modular exponentiation discussion
5. Detect duplicates within distance k

## Mini Assignment
- Build a frequency-analysis toolkit
- Build a pair-sum toolkit with both brute force and optimized approaches

## Timed Coding Test
1. Duplicate detection
2. Pair sum
3. Fast power

## Debugging Exercises
1. Dictionary frequency overwriting counts
2. Shared list mutation bug
3. Pair sum set order bug

---

# DAY 5 — Optimization and Interview Thinking

## Day Objective
Students should leave with:
- a strong optimization mindset
- comfort comparing solutions
- practical bit manipulation intuition
- ability to speak Big-O clearly

## Morning Session Plan
- Time and space complexity
- comparing solutions
- optimization patterns

## Afternoon Session Plan
- binary fundamentals
- XOR
- set bits
- bit-mask basics

---

## Topic 1: Time Complexity

### Intuition
Time complexity is about growth of work, not stopwatch seconds on one machine.

### Interview perspective
The interviewer often asks:
- "Can you do better?"
- "What is your time complexity?"

### Core teaching examples
- single lookup
- one pass
- nested loops
- halving loops

### Comparison table

| Pattern | Typical Complexity |
|---|---|
| single direct access | `O(1)` |
| single traversal | `O(n)` |
| nested traversal | `O(n^2)` |
| repeated halving | `O(log n)` |

### Debugging strategy for complexity
Have students count:
- How many times does outer loop run?
- For each outer loop iteration, how many inner operations happen?

---

## Topic 2: Space Complexity

### Intuition
Space complexity is about extra memory used beyond the input.

### Compare
- in-place reverse traversal: low extra space
- building frequency map: extra space proportional to unique elements

### Interview angle
Sometimes a faster solution uses more memory; students should state that trade-off.

---

## Topic 3: Optimization Patterns

### Core optimization triggers
- repeated work -> cache/store
- all-pairs checking -> hashing or sorting
- monotonic search space -> binary search
- rolling dependence -> maintain few variables
- large recomputation -> prefix/suffix/precompute idea

### Major Example: Duplicate detection
Use this to compare `O(n^2)` vs `O(n)`.

### Major Example: Fibonacci
Use this to compare exponential recursion vs iterative DP-style rolling computation.

---

## Topic 4: Bit Manipulation

### Binary fundamentals
Teach:
- binary positional value
- least significant bit
- powers of 2

### XOR properties
- `a ^ a = 0`
- `a ^ 0 = a`
- XOR is commutative and associative

## Major Problem: Unique number using XOR

### Problem
Every element appears twice except one. Find that one.

### Brute force
Count frequencies.

### Optimized insight
Pairs cancel under XOR.

### Code
```python
nums = list(map(int, input("Enter numbers: ").split()))
result = 0

for x in nums:
    result ^= x

print("Single number =", result)
```

### Sample input
```text
2 3 2 4 4
```

### Sample output
```text
Single number = 3
```

### Complexity
`O(n)` time, `O(1)` extra space

### Interview perspective
This is one of the best examples of using a mathematical property for space optimization.

---

## Major Problem: Swap without temp

### Teaching note
Explain it as a bit trick, but also tell students that in Python, tuple unpacking is cleaner.

### XOR method
```python
a = int(input("Enter first number: "))
b = int(input("Enter second number: "))

a = a ^ b
b = a ^ b
a = a ^ b

print("After swap:", a, b)
```

### Pythonic method
```python
a = int(input("Enter first number: "))
b = int(input("Enter second number: "))
a, b = b, a
print("After swap:", a, b)
```

### Interview discussion
Knowing the XOR trick is good.
Using Pythonic swap in real code is better.

---

## Major Problem: Power of 2

### Insight
A power of 2 has exactly one set bit.

### Code
```python
n = int(input("Enter a number: "))

if n > 0 and (n & (n - 1)) == 0:
    print("Power of 2")
else:
    print("Not Power of 2")
```

### Complexity
`O(1)` by fixed machine-word reasoning

---

## Major Problem: Count Set Bits

### Brute force
Shift right and count last bit each time.

### Better idea
Brian Kernighan’s method removes the lowest set bit each step.

### Standard method
```python
n = int(input("Enter a number: "))
count = 0
temp = n

while temp:
    count += temp & 1
    temp >>= 1

print("Set bits =", count)
```

### Optimized method
```python
n = int(input("Enter a number: "))
count = 0
temp = n

while temp:
    temp &= (temp - 1)
    count += 1

print("Set bits =", count)
```

### Complexity discussion
- shift method: proportional to number of bits
- Kernighan: proportional to number of set bits

### Interview teaching point
This is a strong example of "optimize by removing useful structure directly."

---

## Bit Masking Basics

### What to teach
- checking kth bit
- setting kth bit
- clearing kth bit

### Examples
```python
def is_kth_bit_set(n, k):
    return (n & (1 << k)) != 0

def set_kth_bit(n, k):
    return n | (1 << k)

def clear_kth_bit(n, k):
    return n & ~(1 << k)

n = int(input("Enter number: "))
k = int(input("Enter bit position: "))

print("Is kth bit set?", is_kth_bit_set(n, k))
print("After setting kth bit:", set_kth_bit(n, k))
print("After clearing kth bit:", clear_kth_bit(n, k))
```

### Interview perspective
Students need familiarity, not mastery of all bit hacks.

---

## Day 5 Practice Questions

### Easy
1. Explain `O(1)`, `O(n)`, `O(log n)`
2. Even/odd using bit
3. Multiply by 2 using shift
4. Check kth bit
5. Count set bits

### Medium
1. Power of 2
2. Unique number using XOR
3. Fast set-bit counting
4. Compare two duplicate-detection solutions
5. Compare recursive and iterative Fibonacci

### Interview-level
1. Single number with XOR
2. Two non-repeating numbers discussion
3. Range bitwise patterns intro
4. Modular fast exponentiation discussion
5. Optimization explanation for a brute-force string problem

## Mini Assignment
- Build a "brute force vs optimized" revision sheet for 10 problems

## Timed Coding Test
1. Single number using XOR
2. Count set bits fast
3. Power of 2

## Debugging Exercises
1. Wrong bit shift direction
2. Missing positive check in power-of-two logic
3. Duplicate detection with unnecessary nested loops

---

# Final Mock Interview Framework

## Round 1: Explanation-only
Ask students to explain:
- why prime can be checked to sqrt(n)
- why binary search is `O(log n)`
- why hashing helps duplicate detection
- why XOR solves single-number problem

## Round 2: Whiteboard coding
Problems:
1. Prime range
2. First non-repeating character
3. Binary search
4. Pair sum
5. Count set bits

## Round 3: Optimization follow-up
For each brute-force answer, ask:
- Can we do better?
- What is repeated work?
- What extra space can we use?
- Can sorting help?
- Can hashing help?

## Final Trainer Notes
- Do not let students hide behind syntax
- Ask for intuition before code
- Ask for edge cases before complexity
- Reward structured explanation as much as correctness
- Build the habit: brute force first, optimize second
