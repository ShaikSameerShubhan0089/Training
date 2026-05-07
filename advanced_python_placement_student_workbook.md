# Advanced Python Placement Training Program

Student Workbook

Audience: Third-year engineering students preparing for coding rounds and technical interviews.

Rules for this workbook:
- No solutions are provided
- No hints are provided beyond difficulty level
- Use this for timed practice, revision, and self-evaluation

Use this workbook with:
[advanced_python_placement_trainer_manual.md](C:/Users/S Sameer/Desktop/training/advanced_python_placement_trainer_manual.md)

---

# How to Use This Workbook

## Recommended problem-solving template
For every problem, fill:
1. Problem understanding
2. Input/Output
3. Constraints
4. Brute force idea
5. Better idea
6. Final approach
7. Time complexity
8. Space complexity

## Notes Area

Name: ______________________

Branch: _____________________

College: ____________________

Practice Start Date: ____________________

---

# DAY 1 — Core Programming Logic

## Topic Notes

Input/Output Notes:
____________________________________________________
____________________________________________________

Operators and Expressions Notes:
____________________________________________________
____________________________________________________

Loop Patterns I Noticed:
____________________________________________________
____________________________________________________

Number Theory Observations:
____________________________________________________
____________________________________________________

---

## Easy Problems

1. Count digits in a number
```python



```

2. Sum of digits of a number
```python



```

3. Product of digits of a number
```python



```

4. Reverse a number
```python



```

5. Check whether a number is palindrome
```python



```

## Medium Problems

1. Check whether a number is prime
```python



```

2. Print all primes in a range
```python



```

3. Check whether a number is Armstrong
```python



```

4. Compute factorial iteratively
```python



```

5. Find nth Fibonacci number iteratively
```python



```

## Interview-Level Problems

1. Count prime numbers in a range
```python



```

2. Print all Armstrong numbers in a range
```python



```

3. Sum of prime digits in a number
```python



```

4. Compare iterative and recursive factorial in notes
```text



```

5. Compare recursive and iterative Fibonacci in notes
```text



```

## Mini Assignment

Build a number utility program that supports:
- reverse
- palindrome check
- prime check
- Armstrong check
- factorial
- Fibonacci

Code:
```python





```

## Timed Coding Test

Solve in 25 minutes:
1. Prime check
2. Reverse number
3. nth Fibonacci

Work area:
```python






```

## Debugging Exercises

1. Find the bug:
```python
def is_prime(n):
    for i in range(2, n):
        if n % i == 0:
            return False
    return True
```

Bug notes:
____________________________________________________

2. Find the bug:
```python
def reverse_number(n):
    rev = 0
    while n > 0:
        digit = n % 10
        rev = rev + digit
        n //= 10
    return rev
```

Bug notes:
____________________________________________________

3. Find the bug:
```python
def factorial(n):
    result = 0
    for i in range(1, n + 1):
        result *= i
    return result
```

Bug notes:
____________________________________________________

---

# DAY 2 — Patterns, Arrays, Strings

## Topic Notes

Pattern Derivation Notes:
____________________________________________________
____________________________________________________

Row/Column Observations:
____________________________________________________
____________________________________________________

String Pattern Observations:
____________________________________________________
____________________________________________________

Matrix Traversal Notes:
____________________________________________________
____________________________________________________

---

## Easy Problems

1. Increasing triangle pattern
```python



```

2. Decreasing triangle pattern
```python



```

3. Sum of list elements
```python



```

4. Reverse a string
```python



```

5. Row sums of a matrix
```python



```

## Medium Problems

1. Centered pyramid pattern
```python



```

2. Find second largest distinct element in a list
```python



```

3. Character frequency in a string
```python



```

4. First non-repeating character
```python



```

5. Primary diagonal sum
```python



```

## Interview-Level Problems

1. Longest substring without repeating characters
```python



```

2. Spiral traversal of a matrix
```python



```

3. Check whether two strings are anagrams
```python



```

4. Matrix transpose
```python



```

5. Concept notes: how to rotate a matrix by 90 degrees
```text



```

## Mini Assignment

Build:
1. A pattern notebook with 6 patterns
2. A string utility with:
   - frequency count
   - reverse
   - palindrome check
   - first non-repeating character
3. A matrix utility with:
   - row sum
   - diagonal sum
   - transpose

Code area:
```python





```

## Timed Coding Test

Solve in 30 minutes:
1. Centered pyramid
2. Second largest element
3. First non-repeating character

Work area:
```python





```

## Debugging Exercises

1. Find the bug:
```python
for i in range(1, n + 1):
    print(" " * i + "*" * (2 * i - 1))
```

Bug notes:
____________________________________________________

2. Find the bug:
```python
def frequency_map(s):
    freq = {}
    for ch in s:
        freq[ch] = 1
    return freq
```

Bug notes:
____________________________________________________

3. Find the bug:
```python
def diagonal_sum(matrix):
    total = 0
    for i in range(len(matrix)):
        total += matrix[i][0]
    return total
```

Bug notes:
____________________________________________________

---

# DAY 3 — Searching, Sorting, Functions, Recursion

## Topic Notes

Binary Search Notes:
____________________________________________________
____________________________________________________

Sorting Comparison Notes:
____________________________________________________
____________________________________________________

Function Design Notes:
____________________________________________________
____________________________________________________

Recursion Notes:
____________________________________________________
____________________________________________________

---

## Easy Problems

1. Linear search
```python



```

2. Standard binary search
```python



```

3. Bubble sort
```python



```

4. Write a function to compute GCD
```python



```

5. Recursive sum of first n numbers
```python



```

## Medium Problems

1. First occurrence using binary search
```python



```

2. Selection sort
```python



```

3. Insertion sort
```python



```

4. Function to check prime
```python



```

5. Recursive factorial
```python



```

## Interview-Level Problems

1. Return insertion position using binary search
```python



```

2. Compare bubble, selection, insertion sort in notes
```text



```

3. Recursive Fibonacci
```python



```

4. Explain recursion tree for Fibonacci in notes
```text



```

5. Write helper functions to modularize a larger problem
```python



```

## Mini Assignment

Build a searching and sorting lab file containing:
- linear search
- binary search
- bubble sort
- selection sort
- insertion sort
- helper functions for testing

Code area:
```python





```

## Timed Coding Test

Solve in 30 minutes:
1. Binary search
2. Insertion sort
3. Recursive factorial

Work area:
```python





```

## Debugging Exercises

1. Find the bug:
```python
while left < right:
    mid = (left + right) // 2
    if nums[mid] < target:
        left = mid
    else:
        right = mid - 1
```

Bug notes:
____________________________________________________

2. Find the bug:
```python
for j in range(len(nums)):
    if nums[j] > nums[j + 1]:
        nums[j], nums[j + 1] = nums[j + 1], nums[j]
```

Bug notes:
____________________________________________________

3. Find the bug:
```python
def factorial(n):
    return n * factorial(n - 1)
```

Bug notes:
____________________________________________________

---

# DAY 4 — Advanced Python for Placements

## Topic Notes

Memory Model Notes:
____________________________________________________
____________________________________________________

Mutable vs Immutable Notes:
____________________________________________________
____________________________________________________

Hashing Notes:
____________________________________________________
____________________________________________________

Collections Notes:
____________________________________________________
____________________________________________________

---

## Easy Problems

1. Remove duplicates from a list
```python



```

2. Build frequency map using dictionary
```python



```

3. Find common elements using set operations
```python



```

4. Compute GCD
```python



```

5. Compute LCM
```python



```

## Medium Problems

1. Detect duplicates efficiently
```python



```

2. Pair sum existence
```python



```

3. Character frequency using Counter
```python



```

4. Group indices using defaultdict
```python



```

5. Fast exponentiation
```python



```

## Interview-Level Problems

1. Two-sum returning indices
```python



```

2. Top-k frequent elements
```python



```

3. Longest consecutive sequence
```python



```

4. Modular exponentiation notes
```text



```

5. Detect duplicates within distance k
```python



```

## Mini Assignment

Build a hashing practice file containing:
- duplicate detection
- frequency map
- pair sum
- two-sum indices
- common elements
- fast exponentiation

Code area:
```python





```

## Timed Coding Test

Solve in 30 minutes:
1. Duplicate detection
2. Pair sum existence
3. Fast exponentiation

Work area:
```python





```

## Debugging Exercises

1. Find the bug:
```python
def has_duplicate(nums):
    seen = set()
    for x in nums:
        seen.add(x)
        if x in seen:
            return True
    return False
```

Bug notes:
____________________________________________________

2. Find the bug:
```python
freq = {}
for x in nums:
    freq[x] += 1
```

Bug notes:
____________________________________________________

3. Find the bug:
```python
def fast_power(a, b):
    result = 1
    while b > 0:
        if b % 2 == 1:
            result += a
        a *= a
        b //= 2
    return result
```

Bug notes:
____________________________________________________

---

# DAY 5 — Optimization and Interview Thinking

## Topic Notes

Time Complexity Notes:
____________________________________________________
____________________________________________________

Space Complexity Notes:
____________________________________________________
____________________________________________________

Optimization Triggers:
____________________________________________________
____________________________________________________

Bit Manipulation Notes:
____________________________________________________
____________________________________________________

---

## Easy Problems

1. Explain `O(1)` with one example
```text


```

2. Explain `O(n)` with one example
```text


```

3. Explain `O(log n)` with one example
```text


```

4. Check even/odd using bit operation
```python



```

5. Count set bits
```python



```

## Medium Problems

1. Check whether a number is power of 2
```python



```

2. Find unique number using XOR
```python



```

3. Compare brute force vs optimized duplicate detection
```text



```

4. Compare recursive vs iterative Fibonacci
```text



```

5. Check kth bit
```python



```

## Interview-Level Problems

1. Count set bits efficiently
```python



```

2. Swap two numbers without temp
```python



```

3. Two non-repeating numbers
```python



```

4. Bit masking notes for set/clear/check kth bit
```text



```

5. Build a "brute force to optimized" explanation for any one problem
```text



```

## Mini Assignment

Build an optimization notebook containing:
- one brute force and one optimized version for 5 problems
- time complexity comparison
- space complexity comparison
- final preferred approach

Work area:
```text





```

## Timed Coding Test

Solve in 30 minutes:
1. Unique number using XOR
2. Power of 2
3. Count set bits efficiently

Work area:
```python





```

## Debugging Exercises

1. Find the bug:
```python
def is_power_of_two(n):
    return (n & (n - 1)) == 0
```

Bug notes:
____________________________________________________

2. Find the bug:
```python
def count_bits(n):
    count = 0
    while n:
        n = n & (n - 1)
    return count
```

Bug notes:
____________________________________________________

3. Find the bug:
```python
def single_number(nums):
    result = 1
    for x in nums:
        result ^= x
    return result
```

Bug notes:
____________________________________________________

---

# Final Revision Section

## Topic Self-Rating

Rate yourself from 1 to 5:

| Topic | Rating |
|---|---|
| Number problems | _____ |
| Patterns | _____ |
| Strings | _____ |
| Matrices | _____ |
| Searching | _____ |
| Sorting | _____ |
| Functions | _____ |
| Recursion | _____ |
| Hashing | _____ |
| Complexity | _____ |
| Bit manipulation | _____ |

## My strongest topics
____________________________________________________
____________________________________________________

## My weakest topics
____________________________________________________
____________________________________________________

## Problems I must revise again
____________________________________________________
____________________________________________________

## My next 7-day practice plan

Day 1:
____________________________________________________

Day 2:
____________________________________________________

Day 3:
____________________________________________________

Day 4:
____________________________________________________

Day 5:
____________________________________________________

Day 6:
____________________________________________________

Day 7:
____________________________________________________

