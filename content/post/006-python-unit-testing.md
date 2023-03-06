---
title: "Unit Tests in Python"
date: 2023-02-27T14:14:08-05:00
draft: true
slug: python-unit-testing
toc: true
tags: ["Python"]
---

### What are unit tests?

A unit is a small piece of code - **a method** or **a function** in a Python class or module that needs to be tested. A unit test is **an automated** test written to verify the functionality of a small piece of code. 
Unit tests try to verify the functionality of the code by supplying different inputs and checking to see whether the execution of the code results in expected outputs.


### Benefits of automated tests

There are several benefits to writing automated unit tests.

Automated unit tests:
- help in coming up with a collective understanding of what needs to be built - during the test development process, developers work closely with the other project stakeholders in understanding the business rules.
- enable better code design - tests written during the development process help in designing cleaner modules and classes with a lower number of dependencies.
- serve as excellent documentation resulting in easier onboarding of new developers to the project.
- help in regression protection - automated tests help identify regressions during the new feature development.


### Types of unit test modules

There are several modules available for writing unit tests in Python. Some of the most popular options are **unittest**, **pytest**, and **doctest**.

- Python comes with a standard module called **unittest** for writing automated tests. The Unittest module is based on a popular Java testing framework called JUnit.
- **Pytest** is a popular alternative to the unittest module. It follows pythonic convention and has no boilerplate code. As pytest is not part of Python's standard module, it needs to be installed separately.  
- **Doctest** is part of the standard python modules and helps with the maintenance of documentation using python docstring. Docstrings are comments in the source code that show how to use a module or a function. When the module is executed with the doctest function, the test cases in docstrings are verified.  


### Unit test example

Let's walk through the implementation of different types of unit tests for the classic FizzBuzz game where the function returns the word **Fizz** for the multiples of 3, **Buzz** for the multiples of 5, and **FizzBuzz** for the multiples of 3 and 5.

```Python
import numbers

def fizzbuzz(input):
    """
    Given a number return Fizz if the number is divisible by 3, 
    return Buzz if the number is divisible by 5, 
    FizzBuzz if the number is divisible by both 3 and 5
    else return the input

    :param input: the number to tested for the Fizz Buzz game
    :return: a string converted based on FizzBuzz game logic
    """
    if not isinstance(input, numbers.Number):
        raise Exception("Invalid input")
    
    output = ""
    game_rules = {3: "Fizz", 5: "Buzz"}
    for num in game_rules.keys():
        if input % num == 0:
            output += game_rules[num]
    
    if not output:
        output = str(input)
    
    return output
```

### Tests with Unittest

Here is the unit tests implementation for the above FizzBuzz function using the **Unittest** module:

```Python
import unittest

from fizz_buzz import *


class FizzBuzzTest(unittest.TestCase):
    def test_divisible_by_3(self):
        return_value = fizzbuzz(9)
        self.assertEqual("Fizz", return_value)

    def test_divisible_by_5(self):
        return_value = fizzbuzz(10)
        self.assertEqual("Buzz", return_value)

    def test_divisible_by_3_and_5(self):
        return_value = fizzbuzz(15)
        self.assertEqual("FizzBuzz", return_value)

    def test_not_divisible_by_3_and_5(self):
        return_value = fizzbuzz(17)
        self.assertEqual("17", return_value)    

    def test_fails_for_invalid_number_input(self):
        with self.assertRaises(Exception) as context:
            fizzbuzz("invalid")
            self.assertTrue("Invalid input" in str(context.exception))


if __name__ == '__main__':
    unittest.main()
```
Unittests can be executed using the command `python -m unittest -v` from the command line.


### Tests with Pytest

Here is the implementation using the **Pytest** module. This implementation is using parameterized tests to avoid duplication.

```Python
import pytest

from fizz_buzz import *


@pytest.mark.parametrize("input,expected_output", 
                         [(9, "Fizz"),
                          (10, "Buzz"),
                          (15, "FizzBuzz"),
                          (23, "23") ])
def test_fizzbuzz_valid_inputs(input,expected_output):
    return_value = fizzbuzz(input)
    assert return_value == expected_output


def test_fizzbuzz_invalid_input():
    with pytest.raises(Exception) as context:
        fizzbuzz("invalid")
        assert str(context.value) == "Invalid Input"
```
Pytests can be executed using the command `python -m pytest -v` from the command line.

### Tests with Doctest

Here is an example doctest implementation for the same:

```Python
import numbers


def fizzbuzz(input):
    """
    Given a number return Fizz if the number is divisible by 3, 
    return Buzz if the number is divisible by 5, 
    FizzBuzz if the number is divisible by both 3 and 5
    else return the input

    :param input: the number to tested for the Fizz Buzz game
    :return: a string converted based on FizzBuzz game logic

    >>> fizzbuzz(9)
    'Fizz'
    >>> fizzbuzz(10)
    'Buzz'
    >>> fizzbuzz(15)
    'FizzBuzz'
    >>> fizzbuzz(23)
    '23'
    >>> fizzbuzz("invalid")
    Traceback (most recent call last):
    ...
    Exception: Invalid input
    """
    if not isinstance(input, numbers.Number):
        raise Exception("Invalid input")
    
    output = ""
    game_rules = {3: "Fizz", 5: "Buzz"}
    for num in game_rules.keys():
        if input % num == 0:
            output += game_rules[num]
    
    if not output:
        output = str(input)
    
    return output


if __name__ == "__main__":
    import doctest
    doctest.testmod()
```
Doctests can be executed using the command `python <module name> -v` from the command line.

### Conclusion

In today's cloud-native / microservices world with reducing time to market being a primary goal of every business, it is important for the project teams to adopt to practices such as test automation for deploying changes frequently and reliably. 