[Main Page](../README.md)
# Testing and Modules

## [In Tests We Trust - TDD with Python](https://code.likeagirl.io/in-tests-we-trust-tdd-with-python-af69f47e6932)

> Test-Driven Development is a strategy to think (and write!) tests first.

Seems like writing unit tests first attempts to anticipate different inputs and outputs needed before the code is actually written.
Test names can be extremely descriptive, particularly in comparison to variable name. Should define what is expected and what is being tested.

> The test file name should follow the same name of module name. For instance, if our module is gender.py, our test name should be test_gender.py 
>> A convention widely used is the AAA: Arrange, Act and Assert.
Arrange: you need to organize the data needed to execute that piece of code (input);
Act: here you will execute the code being tested (exercise the behaviour);
Assert: after executing the code, you will check if the result (output) is the same as you were expecting.

**Keep test folder separate from production code**

### Cycle

- Write unit test = FAIL
- Write Feature = PASS
- Refactor code

*Ultimately TDD is thinking about software design first*

## [If __name__ equals __main__](https://www.geeksforgeeks.org/what-does-the-if-__name__-__main__-do/)

> If you import this script as a module in another script, the __name__ is set to the name of the script/module.
> Python files can act as either reusable modules, or as standalone programs.
> if __name__ == “__main__”: is used to execute some code only if the file was run directly, and not imported.

Essentially, if__name__==“__main__” allows us to modularize or run programs on their own.

## Recursion

Recursion is a process in which a function calls itself as a subroutine

This code was the easiest for me to understand:
approach(2) – Recursive adding 

```javascript
f(n) = 1                  n=1

f(n) = n + f(n-1)    n>1
```


* one of the main reasons recursion is used is for simplicity and readability of code.