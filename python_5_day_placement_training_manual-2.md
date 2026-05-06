# Complete 5-Day Python Placement Training Manual

For third-year university students, including non-IT students and absolute beginners

Use this manual directly in class. It is written so an instructor can teach from it line by line.

---

# Table of Contents

1. Course Purpose
2. Teaching Method
3. Day 1: Basics, Decisions, Loops, Number Problems
4. Day 2: Patterns, Lists, Strings, Matrices
5. Day 3: Searching, Sorting, Functions, Recursion
6. Day 4: Python Memory, Math Problems, Built-in Data Structures
7. Day 5: Time Complexity, Optimization, Bit Manipulation
8. Final Placement Preparation Plan

---

# Course Purpose

## Who is this course for?
- Students with zero coding background
- Students who are scared of programming
- Students who feel they are weak in logic
- Students preparing for coding rounds and technical interviews

## What is the goal?
By the end of 5 days, students should be able to:
- Read and write simple Python programs
- Understand how to think before coding
- Solve common placement-style beginner and intermediate problems
- Explain their logic in interviews
- Avoid common mistakes

## Important Message for Students
Programming is not magic.
Programming is simply:
- taking input
- thinking step by step
- writing those steps in Python
- checking the output

If a student can explain the steps in plain English, they can slowly learn to code those steps too.

---

# Teaching Method

## Instructor Rule 1
Always explain in this order:
1. Idea in simple words
2. Real-life example
3. Dry run on board
4. Code
5. Output
6. Common mistakes

## Instructor Rule 2
Before every code, ask:
- What is the input?
- What is the output?
- What should happen first?
- What should repeat?
- What decision should be made?

## Instructor Rule 3
Do not rush.
If students cannot dry run, they are not ready to code that problem.

## Instructor Rule 4
Repeat these lines often:
- Small steps are enough
- Logic first, code next
- Mistakes are normal
- Dry run is your best friend

---

# DAY 1

## Topics
- Input/Output
- Variables
- Data Types
- Type Casting
- Operators
- Conditional Statements
- Loops
- Number Problems

## Day Goal
Students should understand how to:
- store data
- take input
- print output
- make decisions
- repeat actions
- solve simple number-based logic problems

---

## Morning Session

### Teaching Flow

#### Part 1: Reduce fear
What to say:
- "Today we are not learning difficult coding."
- "We are learning how a computer listens to instructions."
- "A program is just a list of small instructions."

Questions to ask:
- If I ask you to make tea, do you do all steps at once or one by one?
- If a machine follows instructions, should instructions be clear or vague?

Expected student response:
- One by one
- Clear

Connect to programming:
- Programming is also one-by-one instruction giving.

#### Part 2: Input, output, variables
What to say:
- "If the user gives data to the program, that is input."
- "If the program shows a result, that is output."
- "A variable is a named box used to store data."

#### Part 3: Conditions and loops
What to say:
- "If you decide based on a situation, that is a condition."
- "If you repeat something many times, that is a loop."

#### Part 4: Number problems
What to say:
- "Most beginner interview problems are just loops plus conditions."

---

## Concept 1: Variables

### 1. What is this?
A variable is a name used to store a value.

### 2. Real-life analogy
Think of a labeled container in a kitchen.
- Label: `sugar_box`
- Inside value: sugar

In Python:
- variable name = label
- stored value = data inside

### 3. Why do we need it?
Without variables:
- we cannot store user input
- we cannot reuse values
- we cannot do calculations easily

### 4. How it works
When we write:
```python
age = 20
```
Python does this:
1. Creates the value `20`
2. Gives it the name `age`
3. Lets us use `age` later

### 5. Syntax explanation
```python
age = 20
```
- `age` is the variable name
- `=` means "store the value on the right into the name on the left"
- `20` is the value

Important:
Here `=` does not mean mathematical equality.
It means assignment.

### 6. Dry run
```python
name = "Ravi"
marks = 85
print(name)
print(marks)
```

Step by step:
1. `name = "Ravi"` stores text `"Ravi"` in `name`
2. `marks = 85` stores `85` in `marks`
3. `print(name)` prints `Ravi`
4. `print(marks)` prints `85`

### 7. Multiple Python examples

#### Easy
```python
# storing a number
x = 10
print(x)
```

#### Medium
```python
# storing two values and adding them
a = 5
b = 7
sum_value = a + b
print(sum_value)
```

#### Interview style
```python
# swapping two values using a third variable
a = 10
b = 20

temp = a
a = b
b = temp

print("a =", a)
print("b =", b)
```

### 8. Common mistakes students make
- Using spaces in variable names
- Using number at the beginning like `2age`
- Thinking `=` means comparison
- Forgetting that variable names are case-sensitive

### 9. Tips to remember
- Variable = named box
- `=` means store
- Use meaningful names like `total`, `name`, `marks`

### 10. Variations
- Store integer
- Store decimal
- Store text
- Store true/false

---

## Concept 2: Input and Output

### 1. What is this?
- Input: data given to the program
- Output: result shown by the program

### 2. Real-life analogy
ATM machine:
- you enter PIN and amount -> input
- machine shows balance or gives cash -> output

### 3. Why do we need it?
Without input and output, a program cannot interact with users.

### 4. How it works
1. `input()` takes data from user
2. `print()` shows data on screen

### 5. Syntax explanation
```python
name = input("Enter your name: ")
print("Hello", name)
```
- `input()` waits for the user to type something
- text inside quotes is message shown to user
- returned value is stored in `name`
- `print()` displays output

Important:
`input()` usually gives text, not number.

### 6. Dry run
If user enters `Rani`:
1. `input()` reads `Rani`
2. It gets stored in `name`
3. `print("Hello", name)` prints `Hello Rani`

### 7. Multiple examples

#### Easy
```python
name = input("Enter your name: ")
print("Welcome", name)
```

#### Medium
```python
a = int(input("Enter first number: "))
b = int(input("Enter second number: "))
print("Sum =", a + b)
```

#### Interview style
```python
# taking three numbers and printing their average
a = int(input("Enter first number: "))
b = int(input("Enter second number: "))
c = int(input("Enter third number: "))

average = (a + b + c) / 3
print("Average =", average)
```

### 8. Common mistakes
- Forgetting `int()` for numeric input
- Writing `print(a + "b")` for numbers and strings incorrectly
- Expecting `input()` to return number directly

### 9. Tips to remember
- `input()` takes text
- `int()` converts text to integer
- `print()` is used to show result

### 10. Variations
- take one value
- take multiple values
- print labels with values

---

## Concept 3: Data Types

### 1. What is this?
Data type tells us what kind of value we are storing.

### 2. Real-life analogy
Different containers hold different things:
- bottle for water
- bag for rice
- file for papers

Similarly, different data types store different kinds of data.

### 3. Why do we need it?
Because numbers and text are handled differently.

### 4. How it works
Common Python types:
- `int` for whole numbers
- `float` for decimal numbers
- `str` for text
- `bool` for `True` or `False`

### 5. Syntax explanation
```python
age = 20        # int
price = 99.5    # float
name = "Asha"   # str
is_passed = True  # bool
```

### 6. Dry run
```python
x = 10
y = 2.5
z = "hi"
```
- `x` is whole number
- `y` is decimal number
- `z` is text

### 7. Multiple examples
```python
age = 21
print(type(age))

weight = 52.4
print(type(weight))

city = "Delhi"
print(type(city))
```

### 8. Common mistakes
- Putting numbers in quotes by mistake
- Forgetting that `"10"` and `10` are different

### 9. Tips to remember
- Quotes mean string
- No quotes usually means number or boolean

### 10. Variations
- check type using `type()`
- convert type using casting

---

## Concept 4: Type Casting

### 1. What is this?
Type casting means converting one data type into another.

### 2. Real-life analogy
Changing currency:
- money is same value idea
- form changes

### 3. Why do we need it?
Because input comes as text.
To add numbers, we must convert text into numbers.

### 4. How it works
- `int("5")` becomes `5`
- `float("3.2")` becomes `3.2`
- `str(25)` becomes `"25"`

### 5. Syntax explanation
```python
num = int(input("Enter number: "))
```
- `input()` gives string
- `int()` converts it to integer

### 6. Dry run
User enters `12`
- input gives `"12"`
- `int("12")` gives `12`

### 7. Multiple examples
```python
x = "15"
print(int(x) + 5)

y = 10
print(str(y) + " apples")
```

### 8. Common mistakes
- Trying `int("12.5")`
- Trying to add string and integer directly

### 9. Tips to remember
- input -> string
- math needs number type

### 10. Variations
- string to int
- int to string
- int to float

---

## Concept 5: Operators

### 1. What is this?
Operators are symbols used to perform actions.

### 2. Real-life analogy
A calculator uses buttons like `+`, `-`, `×`.
Those are like operators.

### 3. Why do we need it?
To calculate, compare, and combine conditions.

### 4. How it works
There are 3 important types for beginners:
- arithmetic
- relational/comparison
- logical

### 5. Syntax explanation

#### Arithmetic operators
```python
a + b
a - b
a * b
a / b
a % b
a // b
a ** b
```
- `%` gives remainder
- `//` gives quotient without decimal
- `**` means power

#### Relational operators
```python
a > b
a < b
a == b
a != b
a >= b
a <= b
```
These return `True` or `False`

#### Logical operators
```python
and
or
not
```

### 6. Dry run
If `a = 10`, `b = 3`
- `a + b = 13`
- `a % b = 1`
- `a > b = True`

### 7. Multiple examples

#### Easy
```python
a = 8
b = 2
print(a + b)
print(a * b)
```

#### Medium
```python
age = 20
print(age >= 18)
```

#### Interview style
```python
# checking whether number is between 1 and 100
n = int(input("Enter number: "))
print(n >= 1 and n <= 100)
```

### 8. Common mistakes
- Using `=` instead of `==`
- Confusing `/` and `//`
- Forgetting `%` is remainder

### 9. Tips to remember
- `==` asks "are they equal?"
- `=` stores value

### 10. Variations
- checking range
- checking divisibility
- combining multiple conditions

---

## Concept 6: Conditional Statements

### 1. What is this?
Conditional statements help the program choose between options.

### 2. Real-life analogy
If it rains, carry umbrella.
Else, do not carry umbrella.

### 3. Why do we need it?
Because programs need decision-making ability.

### 4. How it works
1. Check a condition
2. If true, do one action
3. Else, do another

### 5. Syntax explanation
```python
if condition:
    statement
elif another_condition:
    statement
else:
    statement
```
- `if` starts condition check
- `elif` means "else if"
- `else` means if nothing above is true
- `:` starts a block
- indentation shows which lines belong to that block

### 6. Dry run
```python
marks = 75

if marks >= 90:
    print("A")
elif marks >= 60:
    print("B")
else:
    print("C")
```

Step by step:
1. Is `75 >= 90`? No
2. Is `75 >= 60`? Yes
3. Print `B`

### 7. Multiple examples

#### Easy
```python
num = int(input("Enter a number: "))

if num > 0:
    print("Positive")
else:
    print("Not Positive")
```

#### Medium
```python
num = int(input("Enter a number: "))

if num % 2 == 0:
    print("Even")
else:
    print("Odd")
```

#### Interview style
```python
age = int(input("Enter age: "))
citizen = input("Are you a citizen? (yes/no): ")

if age >= 18 and citizen == "yes":
    print("Eligible to vote")
else:
    print("Not eligible")
```

### 8. Common mistakes
- Missing colon `:`
- Wrong indentation
- Writing `if num = 5`
- Using multiple `if` when `if-elif-else` is better

### 9. Tips to remember
- Condition must become `True` or `False`
- Indentation matters in Python

### 10. Variations
- even/odd
- positive/negative/zero
- greatest of 2 or 3 numbers

---

## Concept 7: Loops

### 1. What is this?
Loops repeat a block of code.

### 2. Real-life analogy
If a teacher says "write your name 10 times," you repeat the same action.

### 3. Why do we need it?
To avoid writing the same code again and again.

### 4. How it works
Two main loops:
- `for` loop
- `while` loop

---

## `for` Loop

### 1. What is this?
Used when the number of repetitions is known.

### 2. Real-life analogy
Clapping 5 times.
You know the count already.

### 3. Syntax explanation
```python
for i in range(1, 6):
    print(i)
```
- `for` starts the loop
- `i` is loop variable
- `range(1, 6)` gives `1, 2, 3, 4, 5`
- body runs once for each value

### 4. Dry run
- `i = 1` -> print 1
- `i = 2` -> print 2
- `i = 3` -> print 3
- `i = 4` -> print 4
- `i = 5` -> print 5

### 5. Examples
```python
for i in range(5):
    print("Hello")
```

```python
for i in range(1, 11):
    print(i)
```

---

## `while` Loop

### 1. What is this?
Used when repetition depends on a condition.

### 2. Real-life analogy
Keep filling water until the bucket is full.

### 3. Syntax explanation
```python
i = 1
while i <= 5:
    print(i)
    i += 1
```
- first set starting value
- check condition
- run body
- update value

### 4. Dry run
- `i = 1`, condition true, print 1
- `i = 2`, condition true, print 2
- ...
- `i = 6`, condition false, stop

### 5. Common mistakes
- forgetting update like `i += 1`
- creating infinite loop

---

## Logic Building for Number Problems

### How to think before coding
Ask these questions:
1. Is this a full-number problem or digit-by-digit problem?
2. Do I need loop?
3. Do I need condition?
4. Do I need original number later?
5. Do I need `% 10` and `// 10`?

### Pattern recognition
- Sum/factorial/fibonacci -> repetition
- Reverse/palindrome/Armstrong -> digit extraction
- Prime -> divisibility checking

### Mistake correction thinking
If answer is wrong:
- check loop range
- check update step
- check if original value got lost
- check if condition is correct

---

## Number Problem 1: Sum of First n Numbers

### What is this?
Add numbers from 1 to `n`.

### Real-life analogy
If you climb 5 steps and count total steps covered:
1 + 2 + 3 + 4 + 5

### Why do we need it?
It teaches accumulation.

### How it works
1. Start total as 0
2. Go from 1 to `n`
3. Add each number to total

### Syntax explanation
```python
total = 0
for i in range(1, n + 1):
    total += i
```
- `total += i` means `total = total + i`

### Dry run for `n = 5`
- total = 0
- add 1 -> 1
- add 2 -> 3
- add 3 -> 6
- add 4 -> 10
- add 5 -> 15

### Code
```python
n = int(input("Enter n: "))
total = 0

for i in range(1, n + 1):
    total += i

print("Sum =", total)
```

### Common mistakes
- using `range(1, n)` and missing `n`

### Tip
When total keeps growing, use an accumulator variable.

### Variation
- sum of even numbers
- sum of odd numbers
- sum in a range

---

## Number Problem 2: Factorial

### What is this?
Factorial of `n` means multiplying all numbers from 1 to `n`.

### Real-life analogy
If 4 different shirts can be arranged in order, factorial helps count arrangements.

### Why do we need it?
Common interview problem.

### How it works
1. Start with `fact = 1`
2. Multiply by each number from 1 to `n`

### Dry run for `n = 4`
- fact = 1
- fact = 1 * 1 = 1
- fact = 1 * 2 = 2
- fact = 2 * 3 = 6
- fact = 6 * 4 = 24

### Code
```python
n = int(input("Enter a number: "))
fact = 1

for i in range(1, n + 1):
    fact *= i

print("Factorial =", fact)
```

### Common mistakes
- starting `fact = 0`
- forgetting factorial uses multiplication, not addition

### Variations
- factorial using `while`
- factorial using function

---

## Number Problem 3: Fibonacci Series

### What is this?
A sequence where next number is sum of previous two numbers.

### Real-life analogy
Think of a chain where every new link depends on the previous two links.

### Why do we need it?
Teaches value updating.

### How it works
Start with:
- `a = 0`
- `b = 1`

Then repeat:
- print `a`
- move forward: `a = b`, `b = a + b`

### Dry run for 6 terms
- 0
- 1
- 1
- 2
- 3
- 5

### Code
```python
n = int(input("Enter number of terms: "))
a = 0
b = 1

for _ in range(n):
    print(a, end=" ")
    a, b = b, a + b
```

### Common mistakes
- changing `a` and `b` in wrong order

### Tip
This problem is about tracking two moving values.

### Variations
- nth Fibonacci number
- Fibonacci up to a limit

---

## Number Problem 4: Reverse Number

### What is this?
Change `1234` into `4321`.

### Real-life analogy
Taking books from top of a stack one by one gives reverse order.

### Why do we need it?
Helps learn digit extraction.

### How it works
1. Take last digit using `% 10`
2. Add it to reversed number
3. Remove last digit using `// 10`

### Dry run for `123`
- digit = 3, rev = 3
- digit = 2, rev = 32
- digit = 1, rev = 321

### Code
```python
num = int(input("Enter number: "))
rev = 0

while num > 0:
    digit = num % 10
    rev = rev * 10 + digit
    num = num // 10

print("Reverse =", rev)
```

### Common mistakes
- forgetting `rev = rev * 10 + digit`
- not updating `num`

### Variations
- reverse and compare
- reverse digits and sum them

---

## Number Problem 5: Palindrome Number

### What is this?
A number that reads same from both sides.
Example: `121`, `1331`

### Why do we need it?
Very common interview question.

### How it works
Reverse the number and compare with original.

### Dry run for `121`
- original = 121
- reversed = 121
- both same -> palindrome

### Code
```python
num = int(input("Enter number: "))
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

### Common mistakes
- forgetting to store original number

### Variations
- palindrome string
- palindrome in range

---

## Number Problem 6: Prime Number

### What is this?
A prime number has exactly two factors:
- 1
- itself

### Real-life analogy
It is like a special lock that only opens in two exact ways.

### Why do we need it?
Prime is a classic placement question.

### How it works
1. Numbers less than or equal to 1 are not prime
2. Check if any number from 2 to `n-1` divides `n`
3. If yes, not prime
4. Else, prime

### Dry run for `7`
- check 2 -> no
- check 3 -> no
- check 4 -> no
- check 5 -> no
- check 6 -> no
- so prime

### Code
```python
num = int(input("Enter number: "))

if num <= 1:
    print("Not Prime")
else:
    is_prime = True

    for i in range(2, num):
        if num % i == 0:
            is_prime = False
            break

    if is_prime:
        print("Prime")
    else:
        print("Not Prime")
```

### Common mistakes
- saying 1 is prime
- forgetting `break`

### Tip
Prime means "no exact division except 1 and itself."

### Variations
- primes in range
- count primes

---

## Number Problem 7: Armstrong Number

### What is this?
For a 3-digit number, if sum of cube of digits equals the number, it is an Armstrong number.

Example:
`153 = 1^3 + 5^3 + 3^3`

### Why do we need it?
Tests digit extraction and accumulation.

### How it works
1. Take each digit
2. Cube it
3. Add to total
4. Compare with original

### Dry run for `153`
- 3^3 = 27
- 5^3 = 125
- 1^3 = 1
- total = 153

### Code
```python
num = int(input("Enter a 3-digit number: "))
original = num
total = 0

while num > 0:
    digit = num % 10
    total += digit ** 3
    num //= 10

if total == original:
    print("Armstrong")
else:
    print("Not Armstrong")
```

### Common mistakes
- forgetting power
- not comparing with original

### Variations
- Armstrong in range
- generalized Armstrong using number of digits

---

## Practice Problems

### Easy Problems

#### 1. Check even or odd
```python
num = int(input())

if num % 2 == 0:
    print("Even")
else:
    print("Odd")
```
Explanation:
- if remainder is 0, number is even

#### 2. Check positive, negative, or zero
```python
num = int(input())

if num > 0:
    print("Positive")
elif num < 0:
    print("Negative")
else:
    print("Zero")
```

#### 3. Find greater of two numbers
```python
a = int(input())
b = int(input())

if a > b:
    print(a)
else:
    print(b)
```

#### 4. Print numbers from 1 to n
```python
n = int(input())

for i in range(1, n + 1):
    print(i)
```

#### 5. Sum of digits
```python
num = int(input())
total = 0

while num > 0:
    total += num % 10
    num //= 10

print(total)
```

### Medium Problems

#### 1. Count digits in a number
```python
num = int(input())
count = 0

while num > 0:
    count += 1
    num //= 10

print(count)
```

#### 2. Multiplication table
```python
n = int(input())

for i in range(1, 11):
    print(n, "x", i, "=", n * i)
```

#### 3. Greatest of three numbers
```python
a = int(input())
b = int(input())
c = int(input())

if a >= b and a >= c:
    print(a)
elif b >= a and b >= c:
    print(b)
else:
    print(c)
```

#### 4. Product of digits
```python
num = int(input())
product = 1

while num > 0:
    product *= num % 10
    num //= 10

print(product)
```

#### 5. Factors of a number
```python
n = int(input())

for i in range(1, n + 1):
    if n % i == 0:
        print(i, end=" ")
```

### Challenge Problems

#### 1. Prime numbers in a range
```python
start = int(input())
end = int(input())

for num in range(start, end + 1):
    if num > 1:
        is_prime = True
        for i in range(2, num):
            if num % i == 0:
                is_prime = False
                break
        if is_prime:
            print(num, end=" ")
```

#### 2. Strong number
```python
num = int(input())
original = num
total = 0

while num > 0:
    digit = num % 10
    fact = 1
    for i in range(1, digit + 1):
        fact *= i
    total += fact
    num //= 10

if total == original:
    print("Strong Number")
else:
    print("Not Strong Number")
```

#### 3. Armstrong numbers in a range
```python
start = int(input())
end = int(input())

for num in range(start, end + 1):
    original = num
    temp = num
    total = 0

    while temp > 0:
        digit = temp % 10
        total += digit ** 3
        temp //= 10

    if total == original:
        print(original, end=" ")
```

---

## Afternoon Session

### Guided coding plan
1. Ask students to predict output of 5 tiny programs
2. Write one `if-else` program together
3. Write one `for` loop together
4. Write one digit-extraction problem together
5. Ask students to dry run prime and palindrome on paper

### Independent practice
- even/odd
- sum of digits
- reverse number
- factorial
- prime

### Group exercise
Give each group one problem:
- Group 1: Fibonacci
- Group 2: Palindrome
- Group 3: Armstrong
- Group 4: Prime in range

Ask them to explain:
- input
- process
- output
- loop used
- condition used

---

## Mini Assignment

1. Write a calculator using `if-elif-else`
2. Write a single program menu for:
- factorial
- reverse
- palindrome
- prime

---

## Interview Preparation Tips

- Speak before coding
- Explain variables clearly
- For digit problems, say `% 10` gets last digit
- For removing last digit, say `// 10`
- For loops, mention start, stop, and update

---

## Revision Summary

- Variable stores data
- `input()` takes value
- `print()` shows output
- `int()` converts string to integer
- `if-else` makes decisions
- `for` repeats known number of times
- `while` repeats until condition fails
- `% 10` gets last digit
- `// 10` removes last digit

---

# DAY 2

## Topics
- Pattern Problems
- Lists
- Strings
- 2D Lists / Matrices

## Day Goal
Students should learn:
- how to build logic using rows and columns
- how to store many values using lists
- how strings work like sequences of characters
- how matrices are just lists inside lists

---

## Morning Session

### Teaching Flow

What to say:
- "Today is the logic-building day."
- "Patterns teach your brain how to think in loops."
- "Lists and strings are collections."
- "Matrices are like classroom seating charts."

Questions to ask:
- If I say print 4 rows, what controls rows?
- If each row has stars, what controls stars?
- If a name has many letters, can we access one letter at a time?

---

## Concept 1: Pattern Problems

### 1. What is this?
Pattern problems print stars, numbers, or letters in a shape.

### 2. Real-life analogy
Arranging chairs in rows for an event.
Rows and number of chairs per row matter.

### 3. Why do we need it?
Patterns are not about stars.
They are about:
- nested loops
- counting
- observation
- logic building

### 4. How it works
Pattern problems usually need:
- outer loop for rows
- inner loop for columns/items in each row

### 5. Syntax explanation
```python
for i in range(rows):
    for j in range(columns):
        print("*", end="")
    print()
```
- outer loop: how many lines
- inner loop: what to print in each line
- `end=""` keeps printing on same line
- `print()` moves to next line

### 6. Dry run
For rows = 3, columns = 2
- row 1 -> print `**`
- row 2 -> print `**`
- row 3 -> print `**`

### 7. How to think before coding patterns
Ask:
1. How many rows?
2. What prints in each row?
3. Are stars increasing, decreasing, or fixed?
4. Are spaces needed?
5. Is the pattern left-aligned or right-aligned?

### 8. Common mistakes
- confusing rows and columns
- forgetting `print()` after each row
- wrong `range()`

### 9. Tips to remember
- Outer loop = rows
- Inner loop = columns/items

### 10. Variations
- star patterns
- number patterns
- alphabet patterns

---

## Pattern 1: Square Pattern

```text
****
****
****
****
```

### How to think
- 4 rows
- each row has 4 stars

### Code
```python
rows = 4

for i in range(rows):
    for j in range(rows):
        print("*", end="")
    print()
```

---

## Pattern 2: Increasing Triangle

```text
*
**
***
****
```

### How to think
- 4 rows
- row 1 has 1 star
- row 2 has 2 stars
- row 3 has 3 stars
- row 4 has 4 stars

### Dry run
- `i = 1` -> print 1 star
- `i = 2` -> print 2 stars
- `i = 3` -> print 3 stars

### Code
```python
rows = 4

for i in range(1, rows + 1):
    for j in range(i):
        print("*", end="")
    print()
```

---

## Pattern 3: Decreasing Triangle

```text
****
***
**
*
```

### How to think
- stars decrease row by row

### Code
```python
rows = 4

for i in range(rows, 0, -1):
    for j in range(i):
        print("*", end="")
    print()
```

---

## Pattern 4: Number Triangle

```text
1
12
123
1234
```

### How to think
- row 1 -> print 1
- row 2 -> print 1 to 2
- row 3 -> print 1 to 3

### Code
```python
rows = 4

for i in range(1, rows + 1):
    for j in range(1, i + 1):
        print(j, end="")
    print()
```

---

## Pattern 5: Right-Aligned Triangle

```text
   *
  **
 ***
****
```

### How to think
Each row has:
- some spaces
- some stars

For 4 rows:
- row 1 -> 3 spaces, 1 star
- row 2 -> 2 spaces, 2 stars
- row 3 -> 1 space, 3 stars
- row 4 -> 0 spaces, 4 stars

### Code
```python
rows = 4

for i in range(1, rows + 1):
    spaces = rows - i
    stars = i
    print(" " * spaces + "*" * stars)
```

---

## Logic Building After Pattern Problems

### Pattern recognition explanation
- Fixed rows, fixed columns -> square
- Row number decides count -> triangle
- Spaces + stars -> alignment

### Mistake correction thinking
If pattern is wrong:
- Is row count correct?
- Is inner loop count correct?
- Are spaces printed before stars?
- Is `print()` placed properly?

---

## Concept 2: Lists

### 1. What is this?
A list stores multiple values in one place.

### 2. Real-life analogy
A fruit basket can hold many fruits together.

### 3. Why do we need it?
If we have 100 numbers, making 100 variables is not practical.

### 4. How it works
```python
nums = [10, 20, 30]
```
This stores 3 values in one list.

### 5. Syntax explanation
```python
nums = [10, 20, 30]
```
- square brackets `[]` create list
- elements separated by commas

Indexing:
- `nums[0]` is first element
- `nums[1]` is second
- `nums[-1]` is last

### 6. Dry run
`nums = [5, 8, 2]`
- first element is 5
- second is 8
- third is 2

### 7. Multiple examples

#### Easy
```python
nums = [10, 20, 30]
print(nums)
print(nums[0])
```

#### Medium
```python
nums = [1, 2, 3]
nums.append(4)
print(nums)
```

#### Interview style
```python
nums = [4, 7, 1, 9]
largest = nums[0]

for x in nums:
    if x > largest:
        largest = x

print("Largest =", largest)
```

### 8. Common mistakes
- starting index from 1 instead of 0
- accessing index out of range
- confusing value and index

### 9. Tips to remember
- list index starts at 0
- `append()` adds at end

### 10. Variations
- list of numbers
- list of strings
- nested list

---

## Concept 3: Strings

### 1. What is this?
A string is text.

### 2. Real-life analogy
A word is like a train.
Each letter is a separate coach.

### 3. Why do we need it?
Names, sentences, passwords, emails, and messages are strings.

### 4. How it works
Strings are sequences of characters.

Example:
```python
text = "python"
```

### 5. Syntax explanation
- written inside quotes
- can access by index

```python
text[0]   # 'p'
text[1]   # 'y'
text[-1]  # 'n'
```

### 6. Dry run
For `"cat"`:
- index 0 -> c
- index 1 -> a
- index 2 -> t

---

## String Topic: Indexing

### What is this?
Accessing one character by position.

### Code
```python
text = "hello"
print(text[0])
print(text[4])
```

### Output explanation
- first line prints `h`
- second line prints `o`

---

## String Topic: Slicing

### What is this?
Taking part of a string.

### Syntax explanation
```python
text[start:end]
```
- includes `start`
- excludes `end`

### Example
```python
text = "python"
print(text[0:2])   # py
print(text[2:5])   # tho
print(text[::-1])  # reverse
```

### Dry run
`text[0:2]`
- start at 0 -> `p`
- stop before 2 -> `y`
- result `py`

---

## String Topic: Immutability

### What is this?
Strings cannot be changed directly character by character.

### Real-life analogy
Think of printed text on paper.
You cannot change one letter without making a new version.

### Example
This is wrong:
```python
text = "cat"
# text[0] = "b"
```

Correct way:
```python
text = "cat"
text = "b" + text[1:]
print(text)
```

### Why do we need this idea?
So students understand why some direct changes fail.

---

## String Operations

```python
text = "python"

print(len(text))
print(text.upper())
print(text.lower())
print("th" in text)
print(text.count("o"))
```

---

## String Logic Building

### How to think before coding string problems
Ask:
1. Do I need to compare characters?
2. Do I need to count something?
3. Do I need to build a new string?
4. Can slicing help?

### Common pattern recognition
- reverse string -> build from end
- palindrome -> compare with reverse
- count vowels -> visit each character
- remove spaces -> replace or rebuild

---

## Concept 4: 2D Lists / Matrices

### 1. What is this?
A matrix is a list containing lists.

### 2. Real-life analogy
Think of a classroom seating chart:
- rows
- columns

### 3. Why do we need it?
Used for tables, grids, marksheets, game boards, and tabular data.

### 4. How it works
```python
matrix = [
    [1, 2, 3],
    [4, 5, 6]
]
```

### 5. Syntax explanation
- first list is row 0
- second list is row 1
- `matrix[0][1]` means row 0, column 1

### 6. Dry run
For:
```python
matrix = [
    [1, 2],
    [3, 4]
]
```
- `matrix[0][0] = 1`
- `matrix[0][1] = 2`
- `matrix[1][0] = 3`
- `matrix[1][1] = 4`

### 7. Multiple examples
```python
matrix = [
    [1, 2],
    [3, 4]
]

for row in matrix:
    for value in row:
        print(value, end=" ")
    print()
```

### 8. Common mistakes
- confusing row index and column index
- using wrong nested loop

### 9. Tips to remember
- matrix[row][column]

### 10. Variations
- matrix sum
- row sum
- diagonal sum

---

## Practice Problems

### Easy Problems

#### 1. Print square pattern
```python
for i in range(4):
    for j in range(4):
        print("*", end="")
    print()
```

#### 2. Sum of list elements
```python
nums = [2, 4, 6, 8]
total = 0

for x in nums:
    total += x

print(total)
```

#### 3. Count vowels in string
```python
text = input().lower()
count = 0

for ch in text:
    if ch in "aeiou":
        count += 1

print(count)
```

#### 4. Print first and last character
```python
text = input()
print(text[0], text[-1])
```

#### 5. Print all elements of matrix
```python
matrix = [[1, 2], [3, 4]]

for row in matrix:
    for value in row:
        print(value, end=" ")
    print()
```

### Medium Problems

#### 1. Reverse a list
```python
nums = [1, 2, 3, 4]
print(nums[::-1])
```

#### 2. Find largest element in list
```python
nums = [5, 1, 9, 2]
largest = nums[0]

for x in nums:
    if x > largest:
        largest = x

print(largest)
```

#### 3. Reverse a string without slicing
```python
text = input()
rev = ""

for ch in text:
    rev = ch + rev

print(rev)
```

#### 4. Palindrome string
```python
text = input()

if text == text[::-1]:
    print("Palindrome")
else:
    print("Not Palindrome")
```

#### 5. Row sums in matrix
```python
matrix = [[1, 2], [3, 4]]

for row in matrix:
    total = 0
    for value in row:
        total += value
    print(total)
```

### Challenge Problems

#### 1. Count words in a sentence
```python
text = input()
words = text.split()
print(len(words))
```

#### 2. Anagram check
```python
a = input()
b = input()

if sorted(a) == sorted(b):
    print("Anagram")
else:
    print("Not Anagram")
```

#### 3. Transpose of matrix
```python
matrix = [
    [1, 2, 3],
    [4, 5, 6]
]

rows = len(matrix)
cols = len(matrix[0])

for j in range(cols):
    for i in range(rows):
        print(matrix[i][j], end=" ")
    print()
```

---

## Afternoon Session

### Guided coding
- Build 3 patterns slowly on board
- Ask students to say number of rows and stars per row
- Build one string reverse problem together
- Build one matrix sum together

### Independent practice
- pattern triangle
- list maximum
- string palindrome
- matrix row sum

### Group exercise
Each group gets one pattern and must answer:
- how many rows?
- what changes per row?
- are spaces needed?

---

## Mini Assignment

1. Write 5 patterns
2. Write a program that:
- takes a sentence
- counts vowels
- counts words
- reverses the sentence
3. Write matrix sum and row-sum programs

---

## Interview Preparation Tips

- For patterns, explain rows first
- For strings, mention indexing and slicing
- For list questions, mention index starts at 0
- For matrices, say row and column clearly

---

## Revision Summary

- Pattern = nested loops
- Outer loop controls rows
- Inner loop controls items in row
- List stores many values
- String is text and supports indexing
- Matrix is list of lists

---

# DAY 3

## Topics
- Searching
- Sorting
- Functions
- Recursion

## Day Goal
Students should understand:
- how to find data in a list
- how to arrange data in sorted order
- how to reuse code using functions
- how recursion works step by step

---

## Morning Session

### Teaching Flow

What to say:
- "Searching means finding."
- "Sorting means arranging."
- "Functions help us avoid repeated code."
- "Recursion is scary only until we dry run it."

Questions to ask:
- How do you search for a word in a small notebook?
- How do you search in a dictionary?
- What if one piece of code is needed many times?

---

## Concept 1: Linear Search

### 1. What is this?
Check each element one by one until target is found.

### 2. Real-life analogy
Looking for your key in a bag by checking each item one by one.

### 3. Why do we need it?
Simple and works on any list.

### 4. How it works
1. Start from first element
2. Compare with target
3. If equal, found
4. Else, move to next element

### 5. Syntax explanation
```python
for i in range(len(nums)):
    if nums[i] == target:
        print(i)
```

### 6. Dry run
Find 7 in `[2, 5, 7, 9]`
- check 2 -> no
- check 5 -> no
- check 7 -> yes

### 7. Multiple examples
```python
nums = [2, 5, 7, 9]
target = 7

for i in range(len(nums)):
    if nums[i] == target:
        print("Found at", i)
        break
```

### 8. Common mistakes
- forgetting `break`
- printing not found too early

### 9. Tip
Linear search is easy but slow for very large lists.

### 10. Variation
- count occurrences
- return position

---

## Concept 2: Binary Search

### 1. What is this?
Searches a sorted list by checking middle element.

### 2. Real-life analogy
Searching a word in a dictionary by opening near the middle, not from page 1.

### 3. Why do we need it?
Faster than linear search when data is sorted.

### 4. How it works
1. Find middle
2. Compare target with middle value
3. If equal, found
4. If target is bigger, go right
5. If target is smaller, go left

### 5. Syntax explanation
```python
low = 0
high = len(nums) - 1

while low <= high:
    mid = (low + high) // 2
```

### 6. Dry run
Find 8 in `[2, 4, 6, 8, 10]`
- low = 0, high = 4, mid = 2, value = 6
- 8 > 6, go right
- low = 3, high = 4, mid = 3, value = 8
- found

### 7. Example
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

### 8. Common mistakes
- using binary search on unsorted list
- wrong update of `low` and `high`

### 9. Tip
Always say in interview: binary search requires sorted data.

### 10. Variation
- first occurrence
- insertion position

---

## Searching Comparison

| Method | Needs Sorted Data? | Easy to Understand? | Usually Faster? |
|---|---|---|---|
| Linear Search | No | Yes | No |
| Binary Search | Yes | Medium | Yes |

---

## Concept 3: Bubble Sort

### 1. What is this?
Repeatedly compares neighboring elements and swaps if they are in wrong order.

### 2. Real-life analogy
Like bigger bubbles slowly moving upward.

### 3. Why do we need it?
Easy beginner sorting algorithm.

### 4. Visual explanation
Sort `[5, 3, 1, 4]`

Pass 1:
- compare 5 and 3 -> swap -> `[3, 5, 1, 4]`
- compare 5 and 1 -> swap -> `[3, 1, 5, 4]`
- compare 5 and 4 -> swap -> `[3, 1, 4, 5]`

Pass 2:
- compare 3 and 1 -> swap -> `[1, 3, 4, 5]`
- compare 3 and 4 -> no swap

Pass 3:
- compare 1 and 3 -> no swap

Sorted list:
`[1, 3, 4, 5]`

### 5. Code
```python
nums = [5, 3, 1, 4]
n = len(nums)

for i in range(n):
    for j in range(0, n - i - 1):
        if nums[j] > nums[j + 1]:
            nums[j], nums[j + 1] = nums[j + 1], nums[j]

print(nums)
```

### 6. Common mistakes
- wrong inner loop range
- comparing wrong positions

---

## Concept 4: Selection Sort

### 1. What is this?
Find the smallest element and place it in correct position.

### 2. Real-life analogy
From a pile of books, repeatedly pick the smallest and place it in order.

### 3. How it works
1. Assume current position is minimum
2. Check rest of list
3. Find actual minimum
4. Swap with current position

### 4. Example
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

---

## Concept 5: Insertion Sort

### 1. What is this?
Take one element and insert it into the correct place in already sorted left part.

### 2. Real-life analogy
Arranging playing cards in your hand.

### 3. How it works
1. Start from second element
2. Compare with left side
3. Shift larger elements right
4. Insert current element in correct place

### 4. Example
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

---

## Sorting Comparison

| Algorithm | Main Idea | Beginner Friendly? | Good for Interviews? |
|---|---|---|---|
| Bubble | Swap adjacent wrong values | Yes | Yes |
| Selection | Pick smallest each round | Yes | Yes |
| Insertion | Insert into sorted left part | Yes | Yes |

What to tell students:
- These are not the fastest modern sorts
- But they are very useful for learning logic and interviews

---

## Concept 6: Functions

### 1. What is this?
A function is a reusable block of code.

### 2. Real-life analogy
A mixer grinder has one button that does a repeated job whenever needed.

### 3. Why do we need it?
- avoid repetition
- organize code
- improve readability

### 4. How it works
1. Define function
2. Call function
3. Function performs the task

### 5. Syntax explanation
```python
def greet(name):
    print("Hello", name)
```
- `def` starts function definition
- `greet` is function name
- `name` is parameter
- indented block is function body

### 6. Dry run
```python
def greet(name):
    print("Hello", name)

greet("Ravi")
```
- define function
- call with `"Ravi"`
- `name` becomes `"Ravi"`
- prints `Hello Ravi`

### 7. Multiple examples

#### Easy
```python
def say_hi():
    print("Hi")

say_hi()
```

#### Medium
```python
def add(a, b):
    return a + b

result = add(4, 5)
print(result)
```

#### Interview style
```python
def is_prime(num):
    if num <= 1:
        return False
    for i in range(2, num):
        if num % i == 0:
            return False
    return True

print(is_prime(7))
```

### 8. Common mistakes
- forgetting colon
- forgetting indentation
- using function without calling it
- confusing `print` and `return`

### 9. Tips to remember
- `print()` shows
- `return` sends value back

### 10. Variations
- function with no parameters
- function with parameters
- function with return value

---

## Concept 7: Recursion

### 1. What is this?
Recursion means a function calls itself.

### 2. Real-life analogy
Think of standing between two mirrors.
The same picture appears again and again.

Better analogy:
To reach step 5, you first reach step 4.
To reach step 4, you first reach step 3.
Same problem, smaller version.

### 3. Why do we need it?
Useful when a problem can be broken into smaller similar problems.

### 4. How it works
Recursion needs:
- base case: where to stop
- recursive case: where function calls itself

### 5. Syntax explanation
```python
def func(n):
    if n == 1:
        return 1
    return n * func(n - 1)
```

### 6. Call stack explanation
When a function calls itself:
- Python pauses current call
- starts new smaller call
- keeps doing that
- when base case is reached, calls return back one by one

### 7. Dry run: factorial(4)
- factorial(4) waits for factorial(3)
- factorial(3) waits for factorial(2)
- factorial(2) waits for factorial(1)
- factorial(1) returns 1
- factorial(2) returns 2
- factorial(3) returns 6
- factorial(4) returns 24

### 8. Code
```python
def factorial(n):
    if n == 1:
        return 1
    return n * factorial(n - 1)

print(factorial(4))
```

### 9. Common mistakes
- no base case
- wrong smaller problem
- infinite recursion

### 10. Tips to remember
- recursion = smaller same problem
- always ask: where does it stop?

### 11. Variations
- sum of first n numbers
- power
- Fibonacci

---

## Practice Problems

### Easy Problems

#### 1. Linear search
```python
nums = [3, 8, 1, 7]
target = 1

for i in range(len(nums)):
    if nums[i] == target:
        print(i)
        break
```

#### 2. Function to square a number
```python
def square(n):
    return n * n

print(square(5))
```

#### 3. Function to check even
```python
def is_even(n):
    return n % 2 == 0

print(is_even(8))
```

#### 4. Bubble sort one list
```python
nums = [4, 2, 5, 1]

for i in range(len(nums)):
    for j in range(len(nums) - i - 1):
        if nums[j] > nums[j + 1]:
            nums[j], nums[j + 1] = nums[j + 1], nums[j]

print(nums)
```

#### 5. Recursive sum
```python
def total(n):
    if n == 1:
        return 1
    return n + total(n - 1)

print(total(5))
```

### Medium Problems

#### 1. Binary search
```python
nums = [1, 3, 5, 7, 9]
target = 7
low = 0
high = len(nums) - 1

while low <= high:
    mid = (low + high) // 2
    if nums[mid] == target:
        print(mid)
        break
    elif nums[mid] < target:
        low = mid + 1
    else:
        high = mid - 1
```

#### 2. Selection sort
```python
nums = [9, 3, 6, 1]

for i in range(len(nums)):
    min_index = i
    for j in range(i + 1, len(nums)):
        if nums[j] < nums[min_index]:
            min_index = j
    nums[i], nums[min_index] = nums[min_index], nums[i]

print(nums)
```

#### 3. Insertion sort
```python
nums = [9, 3, 6, 1]

for i in range(1, len(nums)):
    key = nums[i]
    j = i - 1
    while j >= 0 and nums[j] > key:
        nums[j + 1] = nums[j]
        j -= 1
    nums[j + 1] = key

print(nums)
```

#### 4. Function to return largest of three
```python
def largest(a, b, c):
    if a >= b and a >= c:
        return a
    elif b >= a and b >= c:
        return b
    return c

print(largest(3, 9, 5))
```

#### 5. Recursive power
```python
def power(a, b):
    if b == 0:
        return 1
    return a * power(a, b - 1)

print(power(2, 4))
```

### Challenge Problems

#### 1. Recursive Fibonacci
```python
def fib(n):
    if n == 0:
        return 0
    if n == 1:
        return 1
    return fib(n - 1) + fib(n - 2)

print(fib(6))
```

#### 2. Count occurrences using function
```python
def count_occurrences(nums, target):
    count = 0
    for x in nums:
        if x == target:
            count += 1
    return count

print(count_occurrences([1, 2, 2, 3, 2], 2))
```

#### 3. Binary search as function
```python
def binary_search(nums, target):
    low = 0
    high = len(nums) - 1

    while low <= high:
        mid = (low + high) // 2
        if nums[mid] == target:
            return mid
        elif nums[mid] < target:
            low = mid + 1
        else:
            high = mid - 1
    return -1

print(binary_search([1, 2, 4, 7, 9], 7))
```

---

## Afternoon Session

### Guided coding
- perform one full dry run of linear search
- perform one full dry run of binary search
- do bubble sort on board with boxes/arrows
- create one function together
- trace one recursive factorial together

### Independent practice
- binary search
- selection sort
- function for palindrome
- recursive sum

### Group exercise
Each group compares:
- linear vs binary
- bubble vs selection vs insertion

Ask them to answer:
- which is easier?
- which needs sorted data?
- which repeats the most work?

---

## Mini Assignment

1. Write all 3 sorting algorithms
2. Write one function for each:
- even/odd
- prime
- factorial
3. Write recursive sum and recursive power

---

## Interview Preparation Tips

- Say binary search needs sorted data
- Say recursion needs base case
- Explain sorting pass by pass
- Use functions to keep answers clean

---

## Revision Summary

- Linear search checks one by one
- Binary search uses middle
- Bubble sort swaps neighbors
- Selection sort picks smallest
- Insertion sort inserts in correct place
- Function is reusable code
- Recursion calls itself on smaller input

---

# DAY 4

## Topics
- Python Memory Model
- References
- Mathematical Problems
- Built-in Data Structures
- Built-in Functions and Libraries

## Day Goal
Students should understand:
- variables can point to same object
- Python has useful built-in data structures
- sets and dictionaries are powerful for interviews
- built-in tools save time

---

## Morning Session

### Teaching Flow

What to say:
- "Today we learn how Python stores and shares data."
- "Two variables can sometimes point to the same object."
- "Sets and dictionaries are placement super tools."

Questions to ask:
- If two people share the same notebook, what happens when one writes in it?
- If we want unique values only, what structure is useful?
- If we want value counts, what structure is useful?

---

## Concept 1: Python Memory Model and References

### 1. What is this?
In Python, variables refer to objects.

### 2. Real-life analogy
Imagine a house and its address.
- house = actual object
- address written on paper = reference

Two people can write the same address on their paper.
That means both are pointing to same house.

### 3. Why do we need it?
Because beginners get confused when changing one variable changes another list too.

### 4. How it works
```python
a = [1, 2, 3]
b = a
```
Now both `a` and `b` refer to same list.

If you change through `b`, `a` also shows that change.

### 5. Syntax explanation
```python
a = [1, 2, 3]
b = a
b[0] = 99
```

### 6. Dry run
- create list `[1, 2, 3]`
- `a` points to it
- `b = a` means `b` also points to same list
- change first element through `b`
- same object changed

### 7. Code
```python
a = [1, 2, 3]
b = a

b[0] = 99

print("a =", a)
print("b =", b)
```

Expected output:
```python
a = [99, 2, 3]
b = [99, 2, 3]
```

### 8. Common mistakes
- thinking `b = a` creates a fresh copy

### 9. Tip
If you want a separate copy, use `.copy()`

### 10. Variation
```python
a = [1, 2, 3]
b = a.copy()
b[0] = 99

print(a)
print(b)
```

---

## Concept 2: Mathematical Problems

### Problem 1: GCD

#### What is this?
Greatest Common Divisor = biggest number that divides both numbers exactly.

#### Real-life analogy
If 12 chocolates and 18 chocolates must be packed into equal groups of largest possible size, GCD helps.

#### Why do we need it?
Very common in aptitude and coding rounds.

#### How it works
Use Euclid's method:
- replace `(a, b)` with `(b, a % b)`
- repeat until `b = 0`

#### Dry run for 12, 18
- a = 12, b = 18
- a = 18, b = 12
- a = 12, b = 6
- a = 6, b = 0
- answer = 6

#### Code
```python
a = int(input())
b = int(input())

while b != 0:
    a, b = b, a % b

print("GCD =", a)
```

---

### Problem 2: LCM

#### What is this?
Least Common Multiple = smallest number divisible by both numbers.

#### Why do we need it?
Common interview and math logic question.

#### Formula
`LCM = (a * b) // GCD`

#### Code
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

---

### Problem 3: Power

#### What is this?
`2^4` means 2 multiplied by itself 4 times.

#### Code
```python
base = int(input())
exp = int(input())
result = 1

for i in range(exp):
    result *= base

print(result)
```

---

## Concept 3: Built-in Data Structures

## List

### What is this?
Ordered collection. Can contain duplicates.

### When to use?
When order matters and duplicates are allowed.

### Example
```python
nums = [5, 2, 5, 8]
print(nums)
```

---

## Set

### What is this?
Unordered collection of unique values.

### Real-life analogy
A guest list where each name should appear only once.

### Why do we need it?
Great for:
- removing duplicates
- quick membership checking

### Simple hashing explanation
Think of hashing like putting objects into labeled lockers very quickly so Python can find them fast.
You do not need deep math here.
Just remember:
- set and dict use a smart fast storage system
- that is why checking is usually quick

### Example
```python
nums = [1, 2, 2, 3, 3]
unique_nums = set(nums)
print(unique_nums)
```

---

## Dictionary

### What is this?
Stores data in key-value pairs.

### Real-life analogy
A real dictionary:
- word = key
- meaning = value

Or student record:
- roll number = key
- name = value

### Why do we need it?
Useful for:
- counting frequency
- storing mappings
- quick lookup

### Example
```python
student = {
    "name": "Asha",
    "marks": 90
}

print(student["name"])
```

---

## Concept 4: Built-in Functions and Libraries

### Useful built-in functions
```python
nums = [4, 1, 9, 2]

print(len(nums))
print(max(nums))
print(min(nums))
print(sum(nums))
print(sorted(nums))
```

### Useful library: `math`
```python
import math

print(math.sqrt(25))
print(math.ceil(4.2))
print(math.floor(4.9))
```

### Useful library: `collections.Counter`
```python
from collections import Counter

text = "banana"
count = Counter(text)
print(count)
```

### Why these matter in interviews
- They reduce code length
- They show Python comfort
- But students should also know manual logic when asked

---

## Logic Building for Day 4

### How to think
- Need duplicates removed? Use `set`
- Need counts? Use `dict` or `Counter`
- Need ordered storage? Use `list`
- Need pair mapping? Use `dict`

### Mistake correction thinking
- If one list changed unexpectedly, check references
- If duplicate removal is needed, ask if order matters

---

## Practice Problems

### Easy Problems

#### 1. Find GCD
```python
a = int(input())
b = int(input())

while b != 0:
    a, b = b, a % b

print(a)
```

#### 2. Find LCM
```python
def gcd(a, b):
    while b != 0:
        a, b = b, a % b
    return a

a = int(input())
b = int(input())
print((a * b) // gcd(a, b))
```

#### 3. Remove duplicates
```python
nums = [1, 2, 2, 3, 4, 4]
print(list(set(nums)))
```

#### 4. Frequency using dictionary
```python
nums = [1, 2, 2, 3]
freq = {}

for x in nums:
    freq[x] = freq.get(x, 0) + 1

print(freq)
```

#### 5. Sum using built-in
```python
nums = [10, 20, 30]
print(sum(nums))
```

### Medium Problems

#### 1. Perfect number
```python
num = int(input())
total = 0

for i in range(1, num):
    if num % i == 0:
        total += i

if total == num:
    print("Perfect")
else:
    print("Not Perfect")
```

#### 2. Common elements in two lists
```python
a = [1, 2, 3, 4]
b = [3, 4, 5, 6]

print(list(set(a) & set(b)))
```

#### 3. Second largest element
```python
nums = [5, 8, 2, 9, 1]
largest = second = float("-inf")

for x in nums:
    if x > largest:
        second = largest
        largest = x
    elif x > second and x != largest:
        second = x

print(second)
```

#### 4. Word frequency in sentence
```python
text = input().split()
freq = {}

for word in text:
    freq[word] = freq.get(word, 0) + 1

print(freq)
```

#### 5. Count frequency using Counter
```python
from collections import Counter

nums = [1, 1, 2, 3, 3, 3]
print(Counter(nums))
```

### Challenge Problems

#### 1. Check coprime numbers
```python
def gcd(a, b):
    while b != 0:
        a, b = b, a % b
    return a

a = int(input())
b = int(input())

if gcd(a, b) == 1:
    print("Coprime")
else:
    print("Not Coprime")
```

#### 2. Find element with highest frequency
```python
nums = [1, 2, 2, 3, 3, 3, 4]
freq = {}

for x in nums:
    freq[x] = freq.get(x, 0) + 1

best_key = None
best_count = 0

for key in freq:
    if freq[key] > best_count:
        best_count = freq[key]
        best_key = key

print(best_key)
```

#### 3. Separate copy vs shared reference demo
```python
a = [1, 2, 3]
b = a
c = a.copy()

b[0] = 100
c[1] = 200

print("a =", a)
print("b =", b)
print("c =", c)
```

---

## Afternoon Session

### Guided coding
- show shared list reference on board
- show `.copy()`
- solve GCD slowly
- compare dictionary counting and Counter
- solve duplicate removal with set

### Independent practice
- LCM
- perfect number
- second largest
- frequency map

### Group exercise
Give each group one task:
- remove duplicates
- count words
- find common elements
- explain reference and copy

---

## Mini Assignment

1. Write note in your own words:
- list
- set
- dictionary
- reference
2. Solve:
- GCD
- LCM
- frequency of characters
- common elements

---

## Interview Preparation Tips

- Use `set` and `dict` smartly
- Explain why you used them
- Mention `.copy()` when discussing list copies
- For GCD, clearly explain repeated remainder logic

---

## Revision Summary

- Variables refer to objects
- `b = a` may point to same object
- `.copy()` makes a separate list copy
- `set` stores unique values
- `dict` stores key-value pairs
- `Counter` helps count quickly
- built-in functions save time

---

# DAY 5

## Topics
- Time Complexity
- Optimization Techniques
- Bit Manipulation

## Day Goal
Students should understand:
- not all correct code is equally good
- faster thinking matters in interviews
- basic binary and bit tricks

---

## Morning Session

### Teaching Flow

What to say:
- "Today we learn how to write not only correct code, but smarter code."
- "Time complexity is just a way to talk about growth."
- "Bit manipulation is just working with 0 and 1."

Questions to ask:
- If a class has 10 students and then 10,000 students, will same method feel equally fast?
- If you check every pair of students, does work grow quickly?

---

## Concept 1: Time Complexity

### 1. What is this?
Time complexity tells us how the amount of work grows when input size grows.

### 2. Real-life analogy
Checking one ID card takes almost constant time.
Checking every student in a line grows with the number of students.
Checking every student with every other student grows much faster.

### 3. Why do we need it?
In interviews, a working answer may still be rejected if it is too slow.

### 4. How it works
We usually describe growth using Big-O notation.

### 5. Big-O in simple terms
- `O(1)` -> fixed work
- `O(n)` -> work grows linearly
- `O(n^2)` -> work grows much faster because of nested loops

### 6. Examples
```python
print(nums[0])      # O(1)
```

```python
for x in nums:
    print(x)        # O(n)
```

```python
for i in nums:
    for j in nums:
        print(i, j) # O(n^2)
```

### 7. Common mistakes
- thinking Big-O is exact running time in seconds
- getting scared by notation

### 8. Tip
Big-O is only about trend as input grows.

---

## Concept 2: Optimization Techniques

### 1. What is this?
Optimization means improving the solution so it does less unnecessary work.

### 2. Real-life analogy
If you want to find whether a name already exists, checking a well-organized register is faster than checking random papers one by one.

### 3. Why do we need it?
Interviewers often ask:
- "Can you do better?"

### 4. How it works
Common ways:
- avoid repeated checks
- use `set` or `dict`
- sort if helpful
- store results for reuse

---

## Example: Find Duplicate

### Bad version
```python
nums = [1, 2, 3, 2]
found = False

for i in range(len(nums)):
    for j in range(i + 1, len(nums)):
        if nums[i] == nums[j]:
            found = True

print(found)
```

### Why it is slower
It compares many pairs.

### Better version
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

### Why it is better
- we remember seen values
- no need to compare every pair

---

## Concept 3: Binary Basics

### 1. What is this?
Binary uses only 0 and 1.

### 2. Real-life analogy
Like a switch:
- OFF = 0
- ON = 1

### 3. Why do we need it?
Computers store data in binary.
Bit manipulation questions use this idea.

### 4. Example
- decimal 5 = binary 101
- decimal 6 = binary 110

---

## Concept 4: Bit Manipulation

### 1. What is this?
Using bit-level operations on binary values.

### 2. Why do we need it?
Some problems become very fast and short.

### 3. Important operators
- `&` AND
- `|` OR
- `^` XOR
- `<<` left shift
- `>>` right shift

### 4. Simple meaning
- `a & b` -> 1 only where both have 1
- `a | b` -> 1 where at least one has 1
- `a ^ b` -> 1 where bits are different

---

## Bit Problem 1: Even or Odd

### How it works
In binary:
- even number ends with 0
- odd number ends with 1

So:
```python
num & 1
```
checks last bit.

### Code
```python
num = int(input())

if num & 1:
    print("Odd")
else:
    print("Even")
```

---

## Bit Problem 2: Multiply by 2

### How it works
Left shift by 1 means multiply by 2

### Code
```python
n = int(input())
print(n << 1)
```

---

## Bit Problem 3: Divide by 2

### How it works
Right shift by 1 means divide by 2 for positive integers

### Code
```python
n = int(input())
print(n >> 1)
```

---

## Bit Problem 4: Power of 2

### Key idea
A power of 2 has only one set bit.

Examples:
- 1 -> 1
- 2 -> 10
- 4 -> 100
- 8 -> 1000

For such numbers:
```python
n & (n - 1)
```
becomes 0

### Code
```python
num = int(input())

if num > 0 and (num & (num - 1)) == 0:
    print("Power of 2")
else:
    print("Not Power of 2")
```

---

## Bit Problem 5: Count Set Bits

### What is this?
Count how many 1s are present in binary form.

### Example
5 = 101 -> set bits = 2

### Code
```python
num = int(input())
count = 0

while num > 0:
    count += num & 1
    num = num >> 1

print(count)
```

---

## Logic Building for Day 5

### How to think
Ask:
1. Is my code doing repeated unnecessary work?
2. Can I store seen values?
3. Can I replace nested loops?
4. Can binary help in this problem?

### Mistake correction thinking
- If code is slow, check for nested loops
- If checking duplicates, think `set`
- If counting frequencies, think `dict`

---

## Practice Problems

### Easy Problems

#### 1. Explain O(1), O(n), O(n^2) with examples
Instructor task:
- Ask students to give one example each

#### 2. Even or odd using bit
```python
n = int(input())
print("Odd" if n & 1 else "Even")
```

#### 3. Multiply by 2 using shift
```python
n = int(input())
print(n << 1)
```

#### 4. Divide by 2 using shift
```python
n = int(input())
print(n >> 1)
```

#### 5. Count set bits
```python
n = int(input())
count = 0

while n > 0:
    count += n & 1
    n >>= 1

print(count)
```

### Medium Problems

#### 1. Find duplicate using set
```python
nums = [1, 2, 3, 4, 2]
seen = set()
found = False

for x in nums:
    if x in seen:
        found = True
        break
    seen.add(x)

print(found)
```

#### 2. First non-repeating character
```python
from collections import Counter

text = input()
count = Counter(text)

for ch in text:
    if count[ch] == 1:
        print(ch)
        break
```

#### 3. Power of 2 check
```python
n = int(input())

if n > 0 and (n & (n - 1)) == 0:
    print("Yes")
else:
    print("No")
```

#### 4. Compare slow and fast duplicate logic
```python
nums = [1, 2, 3, 2]

# fast approach
seen = set()
for x in nums:
    if x in seen:
        print("Duplicate found")
        break
    seen.add(x)
```

#### 5. Frequency using dictionary
```python
nums = [1, 1, 2, 3, 3]
freq = {}

for x in nums:
    freq[x] = freq.get(x, 0) + 1

print(freq)
```

### Challenge Problems

#### 1. Single number where all others appear twice
```python
nums = [2, 3, 2, 4, 4]
result = 0

for x in nums:
    result ^= x

print(result)
```

Explanation:
- same numbers cancel in XOR
- only unique one remains

#### 2. Optimize pair sum existence
```python
nums = [2, 7, 11, 15]
target = 9
seen = set()
found = False

for x in nums:
    if target - x in seen:
        found = True
        break
    seen.add(x)

print(found)
```

#### 3. Count set bits for all numbers from 1 to n
```python
n = int(input())

for num in range(1, n + 1):
    temp = num
    count = 0
    while temp > 0:
        count += temp & 1
        temp >>= 1
    print(num, "->", count)
```

---

## Afternoon Session

### Guided coding
- compare one slow and one optimized solution
- explain why nested loops can become costly
- demonstrate binary of 5 and 6 on board
- solve even/odd by modulo and by bit

### Independent practice
- power of 2
- count set bits
- find duplicate using set
- first non-repeating character

### Group exercise
Give each group one problem and ask:
- brute-force method
- better method
- what data structure helps
- expected complexity idea

---

## Mini Assignment

1. Write two versions of duplicate detection:
- nested loops
- set-based
2. Write bit programs for:
- even/odd
- power of 2
- count set bits
3. Explain Big-O in your own simple words

---

## Interview Preparation Tips

- First give a correct simple solution
- Then say: "We can optimize this"
- Mention `set` and `dict` when appropriate
- In bit problems, explain binary idea before code

---

## Revision Summary

- Time complexity describes growth of work
- `O(1)` fixed, `O(n)` linear, `O(n^2)` nested-loop style
- Optimization removes repeated work
- `set` helps quick checking
- Bit manipulation uses binary operations

---

# Final Placement Preparation Plan

## Last 30-Minute Revision Drill

Ask students to explain without coding:
- variable
- loop
- list
- string
- function
- recursion
- set
- dictionary
- time complexity
- bit manipulation

## Final Mock Interview Questions

1. Difference between `=` and `==`
2. Difference between `for` and `while`
3. How do you reverse a number?
4. How do you check prime?
5. How do you reverse a string?
6. Difference between linear and binary search
7. Difference between list and set
8. What is dictionary used for?
9. What is recursion?
10. What is time complexity in simple words?

## Final Advice for Instructors

- Never shame slow students
- Make dry run a daily habit
- Let students explain in their own simple language
- Focus on confidence first, speed later
- Celebrate correct thinking, not only correct syntax

## Final Advice for Students

- Coding is learned by practice, not by watching
- Do not fear mistakes
- Solve small problems daily
- Explain logic aloud
- Write, run, debug, repeat

This is enough to build a strong beginner foundation for placement preparation.

