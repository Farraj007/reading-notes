[Main Page](../README.md)

# Reading Notes 08

## List Comprehensions
[List Comprehension](https://www.pythonforbeginners.com/basics/list-comprehensions-in-python)

### Syntax
- Example of a list:
```
my_new_list = [ expression for item in list ]
```
1. Left hand side is the expression to be carried out. 
2. Then there is the object that has an *item* in the square brackets.
3. Thne there needs to be an **iterable** list of objects to build the new list. This is the *list* in the brackets.

- List comprehensions are a lot more stream-lined than other froms of python code.
- More compact as well.

### Creating a list with range() method
- Example from Reading:
```
# construct a basic list using range() and list comprehensions
# syntax
# [ expression for item in list ]
digits = [x for x in range(10)]

print(digits)
```
Output:
```
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
```
- First 'x' is the expression just record the number. Second one will rep each value in the list, which is created by the range() method.

### List Using Loops and Lsit Comprehensions
- Example from reading: 
```
# create a list using a for loop
squares = []

for x in range(10):
    # raise x to the power of 2
    squares.append(x**2)

print(squares)
```
```
[0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
```

- Example with **list Comprehensions**:
```
# create a list using list comprehension
squares = [x**2 for x in range(10)]

print(squares)
```