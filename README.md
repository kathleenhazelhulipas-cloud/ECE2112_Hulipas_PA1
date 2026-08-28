# ECE2112_PA1 
#### EXPERIMENT 1: INTRODUCTION TO PYTHON PROGRAMMING<br>**Submitted By: Kathleen Hazel L. Hulipas | 2ECE-A**
The content of this repository contains the _**Programming Assignment 1**_ for ECE2112 Advanced Computer Programming course A.Y. 2026 - 2027 which covers python problems from _**Module 1 - Base Computing with Python**_.

Objectives
---
At the end of this laboratory activity, the student should be able to:
  1. use basic Python functions, operators, and string operations;
  2. manipulate strings using indexing, slicing, and built-in string methods;
  3. apply sequence unpacking to manipulate the elements of a list; and
  4. construct simple Python functions that return a specified result.

A. WORD ROTATION PROBLEM
---
Create a function named rotate_word() that accepts a non-empty string. Move the first character of the string to the end while keeping all remaining characters in their original order. Preserve the capitalization of every character. 
<br>**Function format:** rotate_word(text)

The following function and methods were used in this problem:
- `len()` - a string method used to count the total amount of characters

  Example:
  <br> `w = "Advanced Programming"`
  <br> `len(w)` --> 20
   
- `text[index of first element : number of characters : increment]` - a string method to slice given string into parts
  - index of first element - the index where the slicing begins
  - number of characters - the index where the slicing stops
  - increment - the number of index to move between characters

  Example:
  <br> `w[0:20:3]` --> "AaePgmn"

- `text[index]` - a string method used to get the value of a specific index

  Example:
  <br> `w[0]` --> "A"

These methods were used to create a single function that rotates the word while keeping the remaining characters in order:
```python
def rotate_word(text):
    w = text[1:len(text):1] + text[0]
    print ("Rotated word: " + w)

text = str(input("Enter a word:"))
rotate_word(text)
```
### Examples:
```python
rotate_word("python") --> "ythonp"
rotate_word("logic") --> "ogicl"
rotate_word("Code") --> "odeC"
rotate_word("A") --> "A"
```

B. USERNAME BUILDER PROBLEM
---
Create a function named make_username() that accepts two strings: first name and last name. The function must:
  1. convert all letters to lowercase;
  2. remove all spaces from the first name;
  3. remove all spaces from the last name; and
  4. join the processed first and last names using one period (.).

**Function format:** make username(first_name, last_name)

The following function and methods were used in this problem:
- `.lower()` - a string method used to change all characters into lowercase

  Example:
  <br> `w.lower()` --> "advanced programming"
  
- `.replace("","")` - a string method used to change selected character to another character

  Example:
  <br> `w.replace("m", "*")` --> "Advanced progra**ing"

These methods were used to create a single function that generates a username by combining the first and last name, separated by a period, in all lowercase characters:
```python
def make_username(first_name, last_name):
    fn_low = first_name.lower()
    ln_low = last_name.lower()
    fn = fn_low.replace(" ", "")
    ln = ln_low.replace(" ", "")
    return fn + "." + ln

first_name = str(input("Enter your First Name:"))
last_name = str(input("Enter your Last Name:"))
print(make_username(first_name,last_name))
```

### Examples:
```python
make_username("Ada", "Lovelace") --> "ada.lovelace"
make_username("Alan", "Turing") --> "alan.turing"
make_username("Ana Maria", "De Leon") --> "anamaria.deleon"
```

C. BOOKEND SWAP PROBLEM
---
Create a function named swap_bookends() that accepts a list containing at least two elements. Unpack the list into three variables:
- first – the first element;
- middle – a list containing everything between the first and last elements; and
- last – the last element.

Using these variables, return a new list in which the first and last elements have exchanged positions. The elements in middle must remain in their original order. Do not modify the input list.
<br>**Function format:** swap_bookends(items)

The following function and methods were used in this problem:

These methods were used to create a single function that interchanges the position of the first and last index while the remaining characters stay the same:
```python
def swap_bookends(items):
    first, *middle, last = items
    return [last] + middle + [first]

str(input("enter numbers:")

print(swap_bookends([1, 2, 3, 4, 5, 6]))
print(swap_bookends(["red", "green", "blue"]))
print(swap_bookends([8, 3]))
```

### Examples
```python
swap_bookends([1, 2, 3, 4, 5, 6]) --> [6, 2, 3, 4, 5, 1]
swap_bookends(["red", "green", "blue"]) --> ["blue", "green", "red"]
swap_bookends([8, 3]) --> [3, 8]
```

Code that accepts string values and prints as a bookend swap:
```python
def swap_bookends(items):
    first, *middle, last = items
    return [last] + middle + [first]

num = int(input("enter number of inputs: "))
i = 0
y = []
while i < num:
    x = input("enter a string: ")
    y.append(x)
    i += 1

print(swap_bookends(y))
```

### Example
```python
enter number of inputs:  7
enter a string:  red
enter a string:  orange
enter a string:  yellow
enter a string:  green
enter a string:  blue
enter a string:  indigo
enter a string:  violet
['violet', 'orange', 'yellow', 'green', 'blue', 'indigo', 'red']
```

## **README file Version History:**
- August 28, 2026 - Initial README Content uploaded
