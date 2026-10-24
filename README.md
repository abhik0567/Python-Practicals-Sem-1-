# assignment
## 👤 Student Details

| | |
|---|---|
| **Name** | Your Name |
| **Roll No.** | ______ |
| **Class / Course** | ______ |
| **Subject** | Python Programming |
| **Submitted To** | ______ |

---

## ⚙️ How to Run

```bash
git clone https://github.com/<your-username>/python-practical.git
cd python-practical
python q01_quadratic_roots.py
```

Replace `q01_quadratic_roots.py` with any program file listed below.

---

## 📑 Table of Contents

| Q.No | Topic | Code File |
|:---:|---|---|
| 1 | [Quadratic Equation Roots](#question-1-quadratic-equation-roots) | [`q01_quadratic_roots.py`](q01_quadratic_roots.py) |
| 2 | [Prime Numbers](#question-2-prime-numbers) | [`q02_prime_numbers.py`](q02_prime_numbers.py) |
| 3 | [Pyramid and Reverse Pyramid](#question-3-pyramid-and-reverse-pyramid) | [`q03_pyramids.py`](q03_pyramids.py) |
| 4 | [Character Checker](#question-4-character-checker) | [`q04_character_check.py`](q04_character_check.py) |
| 5 | [String Operations](#question-5-string-operations) | [`q05_string_operations.py`](q05_string_operations.py) |
| 6 | [Swap First n Characters](#question-6-swap-first-n-characters) | [`q06_swap_first_n.py`](q06_swap_first_n.py) |
| 7 | [Indices of All Occurrences](#question-7-indices-of-all-occurrences) | [`q07_find_indices.py`](q07_find_indices.py) |
| 8 | [Cubes of Even Integers](#question-8-cubes-of-even-integers) | [`q08_cubes_of_evens.py`](q08_cubes_of_evens.py) |
| 9 | [File Handling](#question-9-file-handling) | [`q09_file_handling.py`](q09_file_handling.py) |
| 10 | [Dictionary of Cubes](#question-10-dictionary-of-cubes) | [`q10_cube_dictionary.py`](q10_cube_dictionary.py) |
| 11 | [Tuple Operations](#question-11-tuple-operations) | [`q11_tuple_operations.py`](q11_tuple_operations.py) |
| 12 | [Employee Class](#question-12-employee-class) | [`q12_employee_class.py`](q12_employee_class.py) |
| 13 | [2D Point Class](#question-13-2d-point-class) | [`q13_point2d.py`](q13_point2d.py) |
| 14 | [3D Point Class (Inheritance)](#question-14-3d-point-class-inheritance) | [`q14_point3d.py`](q14_point3d.py) |
| 15 | [Name Validation with Exceptions](#question-15-name-validation-with-exceptions) | [`q15_name_exception.py`](q15_name_exception.py) |

---

## Question 1: Quadratic Equation Roots

### 📝 Problem Statement

Write a program to find the roots of a quadratic equation.

### 💻 Code

📄 File: [`q01_quadratic_roots.py`](q01_quadratic_roots.py)

```python
"""Q1: Find the roots of a quadratic equation  ax^2 + bx + c = 0"""

a = float(input("Enter a: "))
b = float(input("Enter b: "))
c = float(input("Enter c: "))

if a == 0:
    print("This is not a quadratic equation ('a' cannot be 0).")
else:
    d = b * b - 4 * a * c          # discriminant
    if d > 0:
        r1 = (-b + d ** 0.5) / (2 * a)
        r2 = (-b - d ** 0.5) / (2 * a)
        print("Two different real roots:", r1, "and", r2)
    elif d == 0:
        print("Two equal real roots:", -b / (2 * a))
    else:
        real = -b / (2 * a)
        imag = (-d) ** 0.5 / (2 * a)
        print(f"Complex roots: {real} + {imag}i and {real} - {imag}i")
```

### 🖥️ Output

*Suggested test input: `1 -5 6`*

<!-- Replace the file name below with your screenshot -->

![Output of Question 1](screenshots/q01_output.png)

**Text output (optional):**

```text
(paste your output here)
```

[⬆ Back to top](#-table-of-contents)

---

## Question 2: Prime Numbers

### 📝 Problem Statement

Write a program to accept a number 'n' and

a. Check if 'n' is prime

b. Generate all prime numbers till 'n'

c. Generate first 'n' prime numbers

*This program may be done using functions.*

### 💻 Code

📄 File: [`q02_prime_numbers.py`](q02_prime_numbers.py)

```python
"""Q2: Prime number operations using functions"""


def is_prime(n):
    """Return True if n is prime."""
    if n < 2:
        return False
    for i in range(2, int(n ** 0.5) + 1):
        if n % i == 0:
            return False
    return True


def primes_till(n):
    """Return all primes from 2 to n."""
    return [i for i in range(2, n + 1) if is_prime(i)]


def first_n_primes(n):
    """Return the first n prime numbers."""
    result = []
    num = 2
    while len(result) < n:
        if is_prime(num):
            result.append(num)
        num += 1
    return result


n = int(input("Enter a number n: "))
print(f"a. Is {n} prime?", "Yes" if is_prime(n) else "No")
print(f"b. Primes till {n}:", primes_till(n))
print(f"c. First {n} primes:", first_n_primes(n))
```

### 🖥️ Output

*Suggested test input: `10`*

<!-- Replace the file name below with your screenshot -->

![Output of Question 2](screenshots/q02_output.png)

**Text output (optional):**

```text
(paste your output here)
```

[⬆ Back to top](#-table-of-contents)

---

## Question 3: Pyramid and Reverse Pyramid

### 📝 Problem Statement

Write a program to create a pyramid of the character '*' and a reverse pyramid.

### 💻 Code

📄 File: [`q03_pyramids.py`](q03_pyramids.py)

```python
"""Q3: Pyramid and reverse pyramid of '*'"""

n = int(input("Enter number of rows: "))

print("\nPyramid:")
for i in range(1, n + 1):
    print(" " * (n - i) + "* " * i)

print("\nReverse pyramid:")
for i in range(n, 0, -1):
    print(" " * (n - i) + "* " * i)
```

### 🖥️ Output

*Suggested test input: `5`*

<!-- Replace the file name below with your screenshot -->

![Output of Question 3](screenshots/q03_output.png)

**Text output (optional):**

```text
(paste your output here)
```

[⬆ Back to top](#-table-of-contents)

---

## Question 4: Character Checker

### 📝 Problem Statement

Write a program that accepts a character and performs the following:

a. Print whether the character is a letter or numeric digit or a special character.

b. If the character is a letter, print whether the letter is uppercase or lowercase.

c. If the character is a numeric digit, print its name in text (e.g., if input is 9, output is NINE).

### 💻 Code

📄 File: [`q04_character_check.py`](q04_character_check.py)

```python
"""Q4: Check the type of a character"""

ch = input("Enter a single character: ")

if len(ch) != 1:
    print("Please enter exactly one character.")
elif ch.isalpha():
    print("It is a letter.")
    print("It is UPPERCASE." if ch.isupper() else "It is lowercase.")
elif ch.isdigit():
    names = ["ZERO", "ONE", "TWO", "THREE", "FOUR",
             "FIVE", "SIX", "SEVEN", "EIGHT", "NINE"]
    print("It is a numeric digit.")
    print("In words:", names[int(ch)])
else:
    print("It is a special character.")
```

### 🖥️ Output

*Suggested test input: `9`*

<!-- Replace the file name below with your screenshot -->

![Output of Question 4](screenshots/q04_output.png)

**Text output (optional):**

```text
(paste your output here)
```

[⬆ Back to top](#-table-of-contents)

---

## Question 5: String Operations

### 📝 Problem Statement

Write a program to perform the following operations on a string:

a. Find the frequency of a character in a string.

b. Replace a character by another character in a string.

c. Remove the first occurrence of a character from a string.

d. Remove all occurrences of a character from a string.

### 💻 Code

📄 File: [`q05_string_operations.py`](q05_string_operations.py)

```python
"""Q5: Operations on a string"""

s = input("Enter a string: ")
ch = input("Enter a character to work with: ")

# a. Frequency
count = 0
for c in s:
    if c == ch:
        count += 1
print(f"a. '{ch}' appears {count} time(s).")

# b. Replace a character by another
new = input("Enter the new character to replace it with: ")
print("b. After replacing:", s.replace(ch, new))

# c. Remove first occurrence
pos = s.find(ch)
if pos == -1:
    print("c. Character not found.")
else:
    print("c. After removing first occurrence:", s[:pos] + s[pos + 1:])

# d. Remove all occurrences
print("d. After removing all occurrences:", s.replace(ch, ""))
```

### 🖥️ Output

*Suggested test input: `banana, a, x`*

<!-- Replace the file name below with your screenshot -->

![Output of Question 5](screenshots/q05_output.png)

**Text output (optional):**

```text
(paste your output here)
```

[⬆ Back to top](#-table-of-contents)

---

## Question 6: Swap First n Characters

### 📝 Problem Statement

Write a program to swap the first n characters of two strings.

### 💻 Code

📄 File: [`q06_swap_first_n.py`](q06_swap_first_n.py)

```python
"""Q6: Swap the first n characters of two strings"""

s1 = input("Enter first string: ")
s2 = input("Enter second string: ")
n = int(input("Enter n: "))

new1 = s2[:n] + s1[n:]
new2 = s1[:n] + s2[n:]

print("First string now :", new1)
print("Second string now:", new2)
```

### 🖥️ Output

*Suggested test input: `hello, world, 2`*

<!-- Replace the file name below with your screenshot -->

![Output of Question 6](screenshots/q06_output.png)

**Text output (optional):**

```text
(paste your output here)
```

[⬆ Back to top](#-table-of-contents)

---

## Question 7: Indices of All Occurrences

### 📝 Problem Statement

Write a function that accepts two strings and returns the indices of all the occurrences of the second string in the first string as a list. If the second string is not present in the first string then it should return -1.

### 💻 Code

📄 File: [`q07_find_indices.py`](q07_find_indices.py)

```python
"""Q7: Indices of all occurrences of one string inside another"""


def find_all(main, sub):
    """Return a list of start positions of sub in main, or -1 if absent."""
    indices = []
    start = main.find(sub)
    while start != -1 and sub != "":
        indices.append(start)
        start = main.find(sub, start + 1)   # keep searching after this spot
    return indices if indices else -1


a = input("Enter the main string: ")
b = input("Enter the string to search: ")
print("Result:", find_all(a, b))
```

### 🖥️ Output

*Suggested test input: `abababa, aba`*

<!-- Replace the file name below with your screenshot -->

![Output of Question 7](screenshots/q07_output.png)

**Text output (optional):**

```text
(paste your output here)
```

[⬆ Back to top](#-table-of-contents)

---

## Question 8: Cubes of Even Integers

### 📝 Problem Statement

Write a program to create a list of the cubes of only the even integers appearing in the input list (may have elements of other types also) using the following:

a. 'for' loop

b. list comprehension

### 💻 Code

📄 File: [`q08_cubes_of_evens.py`](q08_cubes_of_evens.py)

```python
"""Q8: Cubes of only the even integers in a mixed list"""

# Turn the typed words into ints / floats / text
items = []
for word in input("Enter list items separated by spaces: ").split():
    try:
        items.append(int(word))
    except ValueError:
        try:
            items.append(float(word))
        except ValueError:
            items.append(word)

print("Your list:", items)

# a. Using a 'for' loop
cubes1 = []
for x in items:
    if type(x) == int and x % 2 == 0:
        cubes1.append(x ** 3)
print("a. Using for loop          :", cubes1)

# b. Using list comprehension
cubes2 = [x ** 3 for x in items if type(x) == int and x % 2 == 0]
print("b. Using list comprehension:", cubes2)
```

### 🖥️ Output

*Suggested test input: `1 2 4 a 6.0 7 8`*

<!-- Replace the file name below with your screenshot -->

![Output of Question 8](screenshots/q08_output.png)

**Text output (optional):**

```text
(paste your output here)
```

[⬆ Back to top](#-table-of-contents)

---

## Question 9: File Handling

### 📝 Problem Statement

Write a program to read a file and

a. Print the total number of characters, words and lines in the file.

b. Calculate the frequency of each character in the file. Use a variable of dictionary type to maintain the count.

c. Print the words in reverse order.

d. Copy even lines of the file to a file named 'File1' and odd lines to another file named 'File2'.

### 💻 Code

📄 File: [`q09_file_handling.py`](q09_file_handling.py)

```python
"""Q9: File handling operations"""

filename = input("Enter file name (press Enter for sample.txt): ") or "sample.txt"

with open(filename, "r") as f:
    text = f.read()
with open(filename, "r") as f:
    lines = f.readlines()

# a. Count characters, words, lines
print("a. Characters:", len(text))
print("   Words     :", len(text.split()))
print("   Lines     :", len(lines))

# b. Frequency of each character (dictionary)
freq = {}
for ch in text:
    freq[ch] = freq.get(ch, 0) + 1
print("b. Character frequency:")
for ch, n in freq.items():
    print(f"   {ch!r}: {n}")

# c. Words in reverse order
print("c. Words in reverse order:")
print("  ", " ".join(reversed(text.split())))

# d. Even lines -> File1, odd lines -> File2
with open("File1", "w") as f1, open("File2", "w") as f2:
    for number, line in enumerate(lines, start=1):
        if number % 2 == 0:
            f1.write(line)
        else:
            f2.write(line)
print("d. Even lines saved in 'File1', odd lines saved in 'File2'.")
```

### 🖥️ Output

*Suggested test input: `press Enter to use sample.txt`*

<!-- Replace the file name below with your screenshot -->

![Output of Question 9](screenshots/q09_output.png)

**Text output (optional):**

```text
(paste your output here)
```

[⬆ Back to top](#-table-of-contents)

---

## Question 10: Dictionary of Cubes

### 📝 Problem Statement

Write a function that prints a dictionary where the keys are numbers between 1 and 5 and the values are cubes of the keys.

### 💻 Code

📄 File: [`q10_cube_dictionary.py`](q10_cube_dictionary.py)

```python
"""Q10: Dictionary of numbers 1-5 and their cubes"""


def print_cubes():
    cubes = {}
    for i in range(1, 6):
        cubes[i] = i ** 3
    print(cubes)


print_cubes()
```

### 🖥️ Output

*Suggested test input: `no input needed`*

<!-- Replace the file name below with your screenshot -->

![Output of Question 10](screenshots/q10_output.png)

**Text output (optional):**

```text
(paste your output here)
```

[⬆ Back to top](#-table-of-contents)

---

## Question 11: Tuple Operations

### 📝 Problem Statement

Consider a tuple t1=(1, 2, 5, 7, 9, 2, 4, 6, 8, 10). Write a program to perform following operations:

a. Print half the values of the tuple in one line and the other half in the next line.

b. Print another tuple whose values are even numbers in the given tuple.

c. Concatenate a tuple t2=(11,13,15) with t1.

d. Return maximum and minimum value from this tuple.

### 💻 Code

📄 File: [`q11_tuple_operations.py`](q11_tuple_operations.py)

```python
"""Q11: Tuple operations"""

t1 = (1, 2, 5, 7, 9, 2, 4, 6, 8, 10)
t2 = (11, 13, 15)

# a. Half in one line, half in the next
mid = len(t1) // 2
print("a. First half :", *t1[:mid])
print("   Second half:", *t1[mid:])

# b. Tuple of even numbers
evens = tuple(x for x in t1 if x % 2 == 0)
print("b. Even numbers:", evens)

# c. Concatenate t2 with t1
print("c. t1 + t2:", t1 + t2)

# d. Maximum and minimum
print("d. Maximum:", max(t1), "| Minimum:", min(t1))
```

### 🖥️ Output

*Suggested test input: `no input needed`*

<!-- Replace the file name below with your screenshot -->

![Output of Question 11](screenshots/q11_output.png)

**Text output (optional):**

```text
(paste your output here)
```

[⬆ Back to top](#-table-of-contents)

---

## Question 12: Employee Class

### 📝 Problem Statement

Define a class Employee that stores information about employees in the company. The class should contain the following:

**(i) Data members** - count (to keep a record of all the objects being created for this class) and for every employee: an employee number, Name, Dept, Basic, DA and HRA.

**(ii) Function members:**

a. `__init__` method to initialize and/or update the members. Add statements to ensure that the program is terminated if any of Basic, DA and HRA is set to a negative value.

b. function `salary`, that returns salary as the sum of Basic, DA and HRA.

c. `__del__` function to decrease the number of objects created for the class.

d. `__str__` function to display the details of an employee along with the salary of an employee in a proper format.

### 💻 Code

📄 File: [`q12_employee_class.py`](q12_employee_class.py)

```python
"""Q12: Employee class"""

import sys


class Employee:
    count = 0   # number of Employee objects alive

    def __init__(self, emp_no, name, dept, basic, da, hra):
        if basic < 0 or da < 0 or hra < 0:
            print("Error: Basic, DA and HRA cannot be negative. Exiting...")
            sys.exit()
        self.emp_no = emp_no
        self.name = name
        self.dept = dept
        self.basic = basic
        self.da = da
        self.hra = hra
        Employee.count += 1

    def salary(self):
        return self.basic + self.da + self.hra

    def __del__(self):
        Employee.count -= 1

    def __str__(self):
        return (f"Employee No : {self.emp_no}\n"
                f"Name        : {self.name}\n"
                f"Department  : {self.dept}\n"
                f"Basic       : {self.basic}\n"
                f"DA          : {self.da}\n"
                f"HRA         : {self.hra}\n"
                f"Salary      : {self.salary()}")


e1 = Employee(101, "Asha", "Sales", 30000, 5000, 8000)
e2 = Employee(102, "Ravi", "IT", 40000, 6000, 10000)
print(e1, "\n")
print(e2, "\n")
print("Employees now:", Employee.count)

del e2
print("After deleting one employee:", Employee.count)

print("\nTrying a negative value...")
Employee(103, "Test", "HR", -100, 500, 500)
```

### 🖥️ Output

*Suggested test input: `no input needed`*

<!-- Replace the file name below with your screenshot -->

![Output of Question 12](screenshots/q12_output.png)

**Text output (optional):**

```text
(paste your output here)
```

[⬆ Back to top](#-table-of-contents)

---

## Question 13: 2D Point Class

### 📝 Problem Statement

Write a program to define a class "2DPoint" with coordinates x and y as attributes. Create relevant methods and print the objects. Also define a method distance to calculate the distance between any two point objects.

> Python names cannot start with a digit, so the class is named `Point2D`.

### 💻 Code

📄 File: [`q13_point2d.py`](q13_point2d.py)

```python
"""Q13: 2D point class (named Point2D because names can't start with a digit)"""


class Point2D:
    def __init__(self, x=0, y=0):
        self.x = x
        self.y = y

    def __str__(self):
        return f"({self.x}, {self.y})"

    def distance(self, other):
        return ((self.x - other.x) ** 2 + (self.y - other.y) ** 2) ** 0.5


if __name__ == "__main__":
    p1 = Point2D(1, 2)
    p2 = Point2D(4, 6)
    print("Point 1:", p1)
    print("Point 2:", p2)
    print("Distance:", p1.distance(p2))
```

### 🖥️ Output

*Suggested test input: `no input needed`*

<!-- Replace the file name below with your screenshot -->

![Output of Question 13](screenshots/q13_output.png)

**Text output (optional):**

```text
(paste your output here)
```

[⬆ Back to top](#-table-of-contents)

---

## Question 14: 3D Point Class (Inheritance)

### 📝 Problem Statement

Inherit the above class to create a "3DPoint" with additional attribute z. Override the method defined in "2DPoint" class, to calculate distance between two points of the "3DPoint" class.

> The class is named `Point3D`. Keep `q13_point2d.py` in the same folder.

### 💻 Code

📄 File: [`q14_point3d.py`](q14_point3d.py)

```python
"""Q14: 3D point class inherited from Point2D"""

from q13_point2d import Point2D


class Point3D(Point2D):
    def __init__(self, x=0, y=0, z=0):
        super().__init__(x, y)
        self.z = z

    def __str__(self):
        return f"({self.x}, {self.y}, {self.z})"

    def distance(self, other):      # overrides Point2D.distance
        return ((self.x - other.x) ** 2 +
                (self.y - other.y) ** 2 +
                (self.z - other.z) ** 2) ** 0.5


p1 = Point3D(1, 2, 3)
p2 = Point3D(4, 6, 8)
print("Point 1:", p1)
print("Point 2:", p2)
print("Distance:", p1.distance(p2))
```

### 🖥️ Output

*Suggested test input: `no input needed`*

<!-- Replace the file name below with your screenshot -->

![Output of Question 14](screenshots/q14_output.png)

**Text output (optional):**

```text
(paste your output here)
```

[⬆ Back to top](#-table-of-contents)

---

## Question 15: Name Validation with Exceptions

### 📝 Problem Statement

Write a program to accept a name from a user. Raise and handle appropriate exception(s) if the text entered by the user contains digits and/or special characters.

### 💻 Code

📄 File: [`q15_name_exception.py`](q15_name_exception.py)

```python
"""Q15: Validate a name using exceptions"""


class InvalidNameError(Exception):
    """Raised when a name has digits or special characters."""


def check_name(name):
    for ch in name:
        if ch.isdigit():
            raise InvalidNameError("Name must not contain digits.")
        if not ch.isalpha() and ch != " ":
            raise InvalidNameError("Name must not contain special characters.")
    if name.strip() == "":
        raise InvalidNameError("Name cannot be empty.")


try:
    name = input("Enter your name: ")
    check_name(name)
    print("Hello,", name, "- valid name!")
except InvalidNameError as e:
    print("Invalid name:", e)
```

### 🖥️ Output

*Suggested test input: `Ravi Kumar  /  Ra#vi2`*

<!-- Replace the file name below with your screenshot -->

![Output of Question 15](screenshots/q15_output.png)

**Text output (optional):**

```text
(paste your output here)
```

[⬆ Back to top](#-table-of-contents)

---

## 📁 Repository Structure

```
python-practical/
├── README.md
├── sample.txt                 # input file used in Q9
├── screenshots/               # put output screenshots here (q01_output.png ... q15_output.png)
├── q01_quadratic_roots.py
├── q02_prime_numbers.py
├── q03_pyramids.py
├── q04_character_check.py
├── q05_string_operations.py
├── q06_swap_first_n.py
├── q07_find_indices.py
├── q08_cubes_of_evens.py
├── q09_file_handling.py
├── q10_cube_dictionary.py
├── q11_tuple_operations.py
├── q12_employee_class.py
├── q13_point2d.py
├── q14_point3d.py
└── q15_name_exception.py
```

## 📸 How to Add Your Output Screenshots

1. Run the program and take a screenshot of the output.
2. Save it inside the `screenshots/` folder as `q01_output.png`, `q02_output.png` ... `q15_output.png`.
3. Commit and push. The images appear automatically in this README.

---

<p align="center">Made with ❤️ using Python · ⭐ Star this repo if it helped you!</p>
