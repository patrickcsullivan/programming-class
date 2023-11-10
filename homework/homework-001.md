# Homework 1

## Section 0

Each problem in this section describes a function for you to implement. Define each new function in your `main.hs` file. Be sure to include a type signature in the definition of each function. 

You should also test your function in `ghci` with a variety of inputs to make sure it works. Many of the problems include examples that you can use to test your functions. You will also want to test the functions with additional inputs.

Problem 0 is solved for you to demonstrate what a solution would look like.

### Problem 0

Write a function named `biggest_end` that takes a list of `Int`s, called `xs`. The function should return either the first or the last element in the list depending on which is larger.

**Examples:**

- `biggest_end [3, 2, 1]` should return `3`.
- `biggest_end [4, 10, 6]` should return `6`.

**Solution:**

This code would go inside `main.hs`.
```
biggest_end :: [Int] -> Int
biggest_end xs = max (head xs) (last xs)
```

### Problem 1

Write a function named `my_last` that takes a list, `xs`. The function should return the last element in the `list`. You are not allowed to use the built-in `last` function. Instead, you must use the built-in `length` and `(!!)` functions.

**Examples:**
- `last [1, 2, 3]` should return `3`.

**Hint:**
The type signature will be `my_last :: [a] -> a`.

### Problem 2

Write a function named `second_half` that takes a list, `xs`. The function should return the second half of the list.

If the list has an odd length, meaning it can't be evenly divided into two, then the output should include the middle element of the list.

**Examples:** 
- `second_half [1, 2, 3, 4]` should return `[3, 4]`.
- `second_half [1, 2, 3, 4, 5]` should return `[2, 3, 4]`.

**Hint:**
The type signature will be `second_half :: [a] -> [a]`.

### Problem 3

Write a function named `second_half_product` that takes a list of `Int`s, called `xs`. The function should return the product of multiplying all elements in the second half of the list. Use the `second_half` function that you wrote in the previous problem to solve this problem.

**Examples:** 
- `second_half_product [1, 2, 3, 4, 5]` should return `60` because 3 * 4 * 5 equals 60.

### Problem 4

Write a function named `neither_empty` that takes two lists, `xs` and `ys`. The function should return `True` if neither list is empty (has zero elements) and `False` otherwise.

**Examples:**
- `neither_empty [1, 2] [3, 4]` should return `True`.
- `neither_empty [], [3, 4]` should return `False`.

### Problem 5

Write a function named `longer` that takes two lists, `xs` and `ys`. The function should return the length of the longest list. 

**Examples:**
- `longer [1, 2] [3, 4, 5]` should return `3`.

### Problem 6

Write a function named `sum_n` that takes an `Int`, `n`, and returns the sum of adding all numbers 1 through `n`.

**Examples:**
- `sum_n 5` should return `15` because 1 + 2 + 3 + 4 + 5 is equal to 15.

### Problem 7

Write a function named `mean` that takes a list of `Float`s, called `xs`, and that returns the mean (or average) of all elements in the list. We can find the mean by calculating the sum of all elements in a list and dividing by total number of elements in the list.

**Examples:**
- `mean [3.4, 8.0, 0.0, -2.2]` should return `2.3`.

### Problem 8

Write a function named `nand` that takes two Boolean arguments, `x` and `y`. The function should return `False` if `x` and `y` are both `True`, and it should return `True` otherwise.

**Examples:**
- `nand True True` should return `False`.
- `nand True False` should return `True`.
- `nand False True` should return `True`.
- `nand False False` should return `True`.

**Note:**
"nand" is short for "not and". The Haskell Prelude library does not contain a built-in `nand` function, but ["nand"](https://en.wikipedia.org/wiki/NAND_gate) is a common operation in logic, electronics, and computer science.

### Problem 9

Write a function named `xor` that takes two Boolean arguments, `x` and `y`. The function should return `True` if exactly one of the arguments is `True`, and it should return `False` otherwise.

Be aware that the behavior of this `xor` function is different from the behavior of the built-in "or" function `(||)`. `(||)` returns `True` if one or both of its arguments are `True`. But `xor` should only return `True` if exactly one of its arguments is `True`.

**Examples:**
- `xor True True` should return `False`.
- `xor True False` should return `True`.
- `xor False True` should return `True`.
- `xor False False` should return `False`.

**Notes:**
"xor" is short for "exclusive or". The Haskell Prelude library does not contain a built-in `xor` function, but ["xor"](https://en.wikipedia.org/wiki/Exclusive_or) is a common operation in logic, electronics, and computer science.

### Problem 10

Write a function called `implies` that two three Boolean arguments, `p` and `q`. The function should implement the following truth table.

| p | q | output |
| - | - | - |
| True` | True | True |
| True` | False | False |
| False` | True | True |
| False` | False | True |

## Section 1

Determine the types of the given expressions. (Feel free to use `ghci` and the `:t` command to determine the answers.) You can write the answers to these problems in any text file.

1. ``"Hello"``
2. `[[], [1.0, 2.0, 3.0], [], [-2.0]]`
3. `(True, ['a'])`
4. `(3.0, 1.2, 4.6)`
5. `(False, False)`

## Section 2

For each of the types listed below, write out 4 different expressions that each have that type. You can write the answers to these problems in any text file.

1. `Int`
2. `[Char]`
3. `(Bool, Bool)`
4. `[(Float, Float, Float)]`
5. `[[Int]]`