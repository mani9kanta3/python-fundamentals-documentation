# Python Fundamentals

A collection of Python fundamentals notes and practice programs, covering core data types and control structures.

## Table of Contents

- [What is Python?](#what-is-python)
- [Why Python?](#why-python)
- [Variables](#variables)
- [Primitive Data Types](#primitive-data-types)
- [Statically Typed vs Dynamically Typed](#statically-typed-vs-dynamically-typed)
- [Type Conversion](#type-conversion)
- [Operators](#operators)
- [Strings](#strings)
- [Lists](#lists)
- [Tuples](#tuples)
- [Sets](#sets)
- [Dictionaries](#dictionaries)
- [Conditionals](#conditionals)
- [Loops](#loops)

---

## What is Python?

Python is a high-level, general-purpose, interpreted programming language known for its simple and readable syntax. It supports multiple programming paradigms, including procedural, object-oriented, and functional programming, and comes with a large standard library that makes it suitable for a wide range of applications.

```python
print("Hello, World!")
```

---

## Why Python?

| Reason | Description |
|---|---|
| Easy to Learn | Simple, English-like syntax that is beginner friendly |
| Readable & Maintainable | Clean syntax improves code readability and reduces maintenance effort |
| Versatile | Used in web development, data science, AI/ML, automation, scripting, and more |
| Large Community & Libraries | Huge ecosystem of third-party packages (NumPy, Pandas, Django, Flask, etc.) |
| Cross-Platform | Runs on Windows, macOS, Linux without modification |
| Interpreted Language | No separate compilation step; code runs line by line |

---

## Variables

A variable is a name used to store a reference to a value in memory. In Python, variables do not need explicit declaration of type — the type is determined automatically based on the assigned value.

### Syntax

```python
name = "Mani"
age = 22
height = 5.9
is_student = True
```

### Rules for Naming Variables

| Rule | Description |
|---|---|
| Must start with a letter or underscore | Cannot start with a digit (`1name` is invalid) |
| Can contain letters, digits, underscores | No spaces or special characters allowed |
| Case-sensitive | `age` and `Age` are different variables |
| Cannot use reserved keywords | e.g., `for`, `if`, `class` cannot be variable names |

---

## Primitive Data Types

Primitive data types are the basic built-in data types provided by Python to store simple values.

| Data Type | Description | Example |
|---|---|---|
| `int` | Whole numbers, positive or negative | `age = 22` |
| `float` | Numbers with decimal points | `height = 5.9` |
| `str` | Sequence of characters (text) | `name = "Mani"` |
| `bool` | Represents `True` or `False` | `is_active = True` |
| `complex` | Numbers with a real and imaginary part | `c = 2 + 3j` |

---

## Statically Typed vs Dynamically Typed

| Point | Statically Typed | Dynamically Typed |
|---|---|---|
| Type Checking | Variable types are checked at compile time | Variable types are checked at runtime |
| Type Declaration | Type must be explicitly declared when creating a variable | Type is inferred automatically from the assigned value |
| Type Change | Type of a variable cannot change once declared | A variable's type can change when reassigned |
| Example | `int age = 22;` (Java/C) — type fixed forever | `age = 22` then `age = "twenty-two"` is valid in Python |

---

## Type Conversion

Type conversion is the process of converting one data type into another. It can happen automatically (implicit) or manually (explicit).

### Implicit Type Conversion

Python automatically converts a smaller data type to a larger data type to avoid data loss, without the programmer's intervention.

```python
num_int = 10
num_float = 2.5

result = num_int + num_float
print(result)        # 12.5
print(type(result))  # <class 'float'>
```

### Explicit Type Conversion

The programmer manually converts one data type into another using built-in functions.

```python
num_str = "100"
num_int = int(num_str)

print(num_int)        # 100
print(type(num_int))  # <class 'int'>
```

### Type Conversion Functions

| Function | Description |
|---|---|
| `int(x)` | Converts `x` to an integer |
| `float(x)` | Converts `x` to a float |
| `str(x)` | Converts `x` to a string |
| `bool(x)` | Converts `x` to a boolean |
| `list(x)` | Converts an iterable to a list |
| `tuple(x)` | Converts an iterable to a tuple |
| `set(x)` | Converts an iterable to a set |
| `dict(x)` | Converts a sequence of key-value pairs to a dictionary |

---

## Operators

Operators are special symbols used to perform operations on variables and values.

| Category | Operators | Description |
|---|---|---|
| Arithmetic | `+`, `-`, `*`, `/`, `%`, `//`, `**` | Perform mathematical operations (addition, subtraction, modulus, floor division, exponent, etc.) |
| Assignment | `=`, `+=`, `-=`, `*=`, `/=`, `//=`, `%=`, `**=` | Assign and update values of variables |
| Comparison | `==`, `!=`, `>`, `<`, `>=`, `<=` | Compare two values and return a boolean |
| Logical | `and`, `or`, `not` | Combine or invert conditional statements |
| Identity | `is`, `is not` | Check if two variables refer to the same object in memory |
| Membership | `in`, `not in` | Check if a value exists within a sequence |
| Bitwise | `&`, `\|`, `^`, `~`, `<<`, `>>` | Perform operations at the binary bit level |

---

## Strings

A string is a sequence of characters enclosed in single, double, or triple quotes. Strings are immutable, meaning their contents cannot be changed after creation.

### Syntax

```python
s = "Hello, World!"
s = 'Python'
s = """Multi-line string"""
```

### Basic Operations

| Operation | Description |
|---|---|
| `s[index]` | Access a character at a given index |
| `s[start:end]` | Slice a substring |
| `s[::-1]` | Reverse a string |
| `len(s)` | Return the length of the string |
| `s + s2` | Concatenate two strings |
| `s * n` | Repeat a string `n` times |
| `sub in s` | Check if a substring exists in the string |

### Case Conversion Methods

| Method | Description |
|---|---|
| `.upper()` | Converts to UPPERCASE |
| `.lower()` | Converts to lowercase |
| `.title()` | Capitalizes first letter of each word |
| `.capitalize()` | Capitalizes the first letter only |
| `.swapcase()` | Swaps uppercase ↔ lowercase |

### Character Type Checking Methods

| Method | Checks if string... |
|---|---|
| `.isalpha()` | Contains only letters |
| `.isdigit()` | Contains only digits |
| `.isspace()` | Contains only spaces |
| `.islower()` | Is it all lowercase? |
| `.isupper()` | Is it all uppercase? |
| `.istitle()` | Is it in the title case? |
| `.isalnum()` | Checks if all characters are alphanumeric (letters + digits) |
| `.isnumeric()` | Checks if all characters are numeric (includes digits, subscripts, fractions) |
| `.isdecimal()` | Checks if all characters are decimals (digits only, no fractions) |
| `.isprintable()` | Checks if all characters are printable (not control characters) |

### Difference between `.isdigit()`, `.isnumeric()`, and `.isdecimal()`

| Method | Description | Example |
|---|---|---|
| `.isdigit()` | Checks if all characters are Unicode digits (including superscripts) | `'12345'`, `'²³'` |
| `.isnumeric()` | Checks if all characters are numeric (digits, fractions, subscripts, Roman numerals) | `'12345'`, `'½'`, `'⅕'`, `'Ⅴ'`, `'²³'` |
| `.isdecimal()` | Checks if all characters are decimal digits (0–9 only) | `'12345'` |

### Searching & Checking Methods

| Method | Description | Example |
|---|---|---|
| `find(val)` | Returns index of first occurrence, else returns -1 if not found | `"apple".find('p')` → `1` |
| `rfind(val)` | Finds last index of val | `'hello'.rfind('l')` → `3` |
| `index(val)` | Same as `find()`, but raises an error if not found | `"apple".index('p')` → `1` |
| `startswith()` | Checks if string starts with val | `"hello".startswith('he')` → `True` |
| `endswith()` | Checks if string ends with val | `"hello".endswith('lo')` → `True` |
| `count()` | Counts occurrences of val | `"banana".count('a')` → `3` |

### Modification Methods

| Method | Description | Example |
|---|---|---|
| `strip()` | Removes leading/trailing spaces | `" hello ".strip()` → `'hello'` |
| `lstrip()` | Removes leading spaces | `" hello".lstrip()` → `'hello'` |
| `rstrip()` | Removes trailing spaces | `"hello ".rstrip()` → `'hello'` |
| `replace(old, new)` | Replaces all occurrences | `"hello".replace('l', 'L')` → `'heLLo'` |

### Splitting & Joining Methods

| Method | Description | Example |
|---|---|---|
| `split(sep)` | Splits into a list | `"a,b,c".split(',')` → `['a', 'b', 'c']` |
| `join(iterable)` | Joins list elements | `'-'.join(['a', 'b', 'c'])` → `'a-b-c'` |

### Advanced Formatting

| Method | Description | Example | Output |
|---|---|---|---|
| `.zfill(width)` | Fills string with leading zeros to match width | `'6'.zfill(3)` | `'006'` |
| `.rjust(width[, fillchar])` | Right-justifies the string in a field of given width using optional fill character | `"hi".rjust(5, "*")` | `'***hi'` |
| `.ljust(width[, fillchar])` | Left-justifies the string in a field of given width using optional fill character | `"hello".ljust(8, "-")` | `'hello---'` |
| `.center(width)` | Centers the string, adds padding spaces to both sides | `'hi'.center(6)` | `'  hi  '` |
| `.casefold()` | Converts string to lowercase (more aggressive than `.lower()`) | `'WHAT'.casefold()` | `'what'` |
| `.partition(sep)` | Splits into 3 parts: before, separator, after | `'key:value'.partition(':')` | `('key', ':', 'value')` |

📂 See examples & practice code: [`Strings.ipynb`](./Strings.ipynb)


---

## Lists

A list is an ordered, mutable collection of items that can hold elements of different data types.

### Syntax

```python
my_list = [10, 20, 30, 40]
```

### Methods & Operations

| Method / Operation | Description |
|---|---|
| `my_list[index]` | Access an element at a given index |
| `my_list[start:end]` | Slice a sublist |
| `len(my_list)` | Return the number of elements |
| `my_list.append(x)` | Add an element to the end |
| `my_list.extend(iterable)` | Add multiple elements to the end |
| `my_list.insert(i, x)` | Insert an element at a specific position |
| `my_list.remove(x)` | Remove the first occurrence of a value |
| `my_list.pop()` | Remove and return the last element |
| `my_list.pop(i)` | Remove and return the element at index `i` |
| `del my_list[i]` | Delete an element by index |
| `del my_list` | Delete the entire list |
| `my_list.clear()` | Remove all elements |
| `my_list.count(x)` | Count occurrences of a value |
| `my_list.index(x)` | Return the index of the first occurrence |
| `my_list.sort()` | Sort the list in ascending order |
| `my_list.sort(reverse=True)` | Sort the list in descending order |
| `my_list.sort(key=len)` | Sort using a custom key function |
| `my_list.reverse()` | Reverse the list in place |
| `my_list.copy()` | Return a shallow copy of the list |
| `min(my_list)` | Return the smallest element |
| `max(my_list)` | Return the largest element |
| `sum(my_list)` | Return the sum of all elements |
| `x in my_list` | Check if an element exists |
| `list1 + list2` | Concatenate two lists |
| `my_list * n` | Repeat a list `n` times |
| `list(set(my_list))` | Remove duplicates from a list |

📂 See examples & practice code: [`Lists.ipynb`](./Lists.ipynb)

---

## Tuples

A tuple is an ordered, immutable collection of items. Once created, its elements cannot be changed.

### Syntax

```python
t = (10, "Python", 3.14)
```

### Methods & Operations

| Method / Operation | Description |
|---|---|
| `t[index]` | Access an element at a given index |
| `t[start:end]` | Slice a subtuple |
| `t[i][j]` | Access an element inside a nested tuple |
| `len(t)` | Return the number of elements |
| `t.count(x)` | Count occurrences of a value |
| `t.index(x)` | Return the index of the first occurrence |
| `t1 + t2` | Concatenate two tuples |
| `t * n` | Repeat a tuple `n` times |
| `x in t` | Check if an element exists |
| `del t` | Delete the entire tuple |

📂 See examples & practice code: [`Tuple.ipynb`](./Tuple.ipynb)

---

## Sets

A set is an unordered collection of unique elements. Sets do not allow duplicate values and support mathematical set operations.

### Syntax

```python
s = {10, 20, 30, 40}
```

### Methods & Operations

| Method / Operation | Description |
|---|---|
| `s.add(x)` | Add a single element |
| `s.update(iterable)` | Add multiple elements |
| `s.remove(x)` | Remove an element (raises error if not found) |
| `s.discard(x)` | Remove an element (no error if not found) |
| `s.pop()` | Remove and return a random element |
| `s.clear()` | Remove all elements |
| `del s` | Delete the entire set |
| `len(s)` | Return the number of elements |
| `x in s` | Check if an element exists |
| `s.copy()` | Return a shallow copy of the set |
| `s1.union(s2)` | Return all elements from both sets |
| `s1.intersection(s2)` | Return elements common to both sets |
| `s1.difference(s2)` | Return elements in `s1` but not in `s2` |
| `s1.symmetric_difference(s2)` | Return elements not common to both sets |
| `s1.issubset(s2)` | Check if `s1` is a subset of `s2` |
| `s1.issuperset(s2)` | Check if `s1` is a superset of `s2` |
| `s1.isdisjoint(s2)` | Check if two sets have no common elements |
| `s1.update(s2)` | Add all elements of `s2` into `s1` |
| `s1.difference_update(s2)` | Remove elements found in `s2` from `s1` |
| `s1.intersection_update(s2)` | Keep only elements common to both sets |
| `set(my_list)` | Convert a list to a set (removes duplicates) |
| `min(s)` / `max(s)` / `sum(s)` | Minimum, maximum, and sum of elements |

📂 See examples & practice code: [`Sets.ipynb`](./Sets.ipynb)

---

## Dictionaries

A dictionary is an unordered, mutable collection of key-value pairs. Each key must be unique.

### Syntax

```python
student = {
    "name": "Mani",
    "age": 22,
    "course": "Python"
}
```

### Methods & Operations

| Method / Operation | Description |
|---|---|
| `d[key]` | Access the value for a given key |
| `d[key] = value` | Add a new key-value pair or update an existing key |
| `del d[key]` | Delete a key-value pair |
| `key in d` | Check if a key exists |
| `d.keys()` | Return all keys |
| `d.values()` | Return all values |
| `d.items()` | Return all key-value pairs |
| `for k, v in d.items()` | Iterate over key-value pairs |

📂 See examples & practice code: [`Dictionary.ipynb`](./Dictionary.ipynb)

---

## Conditionals

Conditional statements allow a program to make decisions and execute different blocks of code based on whether a condition is `True` or `False`.

### Syntax

```python
if condition:
    # code block
elif another_condition:
    # code block
else:
    # code block

# Nested conditional
if condition1:
    if condition2:
        # code block
```

### Operators

| Operator / Keyword | Description |
|---|---|
| `==`, `!=` | Equal to, not equal to |
| `>`, `<`, `>=`, `<=` | Comparison operators |
| `and` | True if both conditions are true |
| `or` | True if at least one condition is true |
| `not` | Reverses the boolean value |
| `if` | Executes a block if condition is true |
| `elif` | Checks another condition if previous ones are false |
| `else` | Executes a block if no condition is true |
| Nested `if` | An `if` statement inside another `if` block |

📂 See examples & practice code: [`Conditional.ipynb`](./Conditional.ipynb)

---

## Loops

Loops are used to execute a block of code repeatedly, either a fixed number of times or until a condition is met.

### Syntax

```python
# for loop
for i in range(1, 11):
    print(i)

# while loop
i = 10
while i >= 1:
    print(i)
    i -= 1

# break and continue
for i in range(10):
    if i == 5:
        break
    if i % 2 == 0:
        continue
```

### Keywords & Operations

| Keyword / Operation | Description |
|---|---|
| `for` | Iterates over a sequence (list, range, string, etc.) |
| `while` | Repeats a block while a condition is true |
| `range(start, stop)` | Generates a sequence of numbers |
| `break` | Exits the loop immediately |
| `continue` | Skips to the next iteration |
| `%` | Modulus operator, used to check divisibility (even/odd) |
| `//` | Floor division, used to extract digits |

📂 See examples & practice code: [`Loops.ipynb`](./Loops.ipynb)