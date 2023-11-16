# Homework 2

Each problem in this assignment, except for Problem 5, describes a function for you to implement. Define each new function in your `main.hs` file. Be sure to include a type signature in the definition of each function. 

You should also test your function in `ghci` with a variety of inputs to make sure it works. Many of the problems include examples that you can use to teAst your functions. You will also want to test the functions with additional inputs.

### Problem 0

Write a function named `num_sign` that takes an `Int`, `x`. The function should return the string `"POSITIVE"` if `x` is positive, `"NEGATIVE"` if `x` is negative, and `"ZERO"` if `x` is zero.

### Problem 1

Write a function named `num_parity` that takes an `Int`, `x`. The function should return the string `"ODD"` if `x` is an odd integer and `"EVEN"` if `x` is an even integer.

### Problem 2

Write a function named `describe_list` that takes a list, `xs`. The function should return the string `"EMPTY"` if the list is empty, `"SINGLETON"` if the list contains a single element, and `"LONGER"` if the contains more than one element.

### Problem 3

Write a function named `middle_element` that takes a list of integers named `xs`. The function should return the middle element in the list. 

If the list contains 5 elements then the function should return the element at index 2 (the third element). If the list contains 4 elements then the function should return the element at index 1 (the second element). 

**Examples:**

- `middle_element [1, 2, 3, 4, 5]` should return `3`.
- `middle_element [1, 2, 3, 4]` should return `2`.

<!-- ### The concept of "partial functions" and "total functions".

What happens if we call the function above, passing in an empty list like so `middle_element []`. Try it in ghci!

You should get a message that says `*Exception`. In Haskell an "exception" is an error that interrupts the execution of a program. It will cause your program to crash and stop running. Ideally, we want to write our programs so that once the program starts running, exceptions can never occur.

Recall that the type signature of each function controls what types of values can be passed into a function. For example, if a function has the type `[Int] -> Int` then the compiler will make it impossible to ever pass in a value to the function that is not a list of integers; your program simply will not compile if you ever try to pass in a value that is not a list of integers.

However, when we executed `middle_element []`, we called the function and passed in an empty list of integers. We obeyed the type signature of the function but an exception still occured. -->

### Problem 4

What happens if we call the function above, passing in an empty list like so `middle_element []`. Try it in `ghci`!

You should get a message that says `*Exception`. In Haskell an "exception" is an error that interrupts the execution of a program. It will cause your program to crash and stop running. Ideally, we want to write our programs so that once the program starts running, exceptions can never occur.

Fix this by writing a new function called, `middle_element_or_zero`. Like the function from Problem 3, this function should take a list of integers named `xs`, and it should return the middle element in the list. However, if `xs` is an empty list then the function should return `0`.

**Examples:**

- `middle_element_or_zero [1, 2, 3, 4, 5]` should return `3`.
- `middle_element_or_zero [1, 2, 3, 4]` should return `2`.
- `middle_element_or_zero []` should return `0`.

### Problem 5

We were able to raise an exception and crash our program by calling the `middle_element` function and passing in the value `[]`. Is there any way that raise an exception by calling `middle_element_or_zero`?

The answer is no, and this is great! For every possible list of integers that we could pass to `middle_element_or_zero` we will never raise an exception. `middle_element_or_zero` is called a **total function** because it works on **all** possible input values. `middle_element` is called a **partial function** because there are some possible values that cause it to crash.

Ideally, we want to implement our functions such that they are total functions instead of partial functions, because total functions will not raise exceptions and cause our programs to crash.

Identify two functions from the [Chapter 2 references](../references/chapter-02.md) that are partial functions. Write down one value for each of the functions that will cause the function to raise an exception when we pass that value to the function. (For example, `middle_element` is a partial function and it raises an exception when we pass in the value `[]`.)

### Problem 6

Write a function named `is_first_even` that takes a list of integers named `xs`. The function should return `True` if the first element of the list is even.

Make sure that your function is a **total function** and that it works even when `xs` is the empty list. Your function should return `False` if `xs` is the empty list.

**Examples:**

- `is_first_even [3, 8, 9]` should return `False`.
- `is_first_even [2, 8, 9]` should return `True`.
- `is_first_even []` should return `False`.

### Problem 7

Pretend there are three friends named Alice, Bob, and Carol. Alice is 42, Bob is 35, and Carol is 28.

Write a function named `get_age_by_name` that takes a `String` named `name` and that returns an `Int`. 

The argument `name` will be a `String` that represents the name of one of the friends. Depending on which name is passed into the function, we should return the age of the person with that name. 

Make sure that your function is a **total function** and that it works even when `name` is a name that we don't recognize. Your function should return `0` if `name` is an unrecognized name.

**Examples:**

- `get_age_by_name "Alice"` should return `42`.
- `get_age_by_name "David"` should return `0`.

### Problem 8

Write a function named `abs_val` that takes an `Int` named `x` and returns the absolute value of `x`.

**Examples:**

- `abs_val 4` should return `4`.
- `abs_val -1` should return `1`.

### Problem 9

Write a function named `command_description` that takes a `Char` named `c` and returns a `String`. The argument `c` represents a GHCI command. The `String` that is returned should be a description of the command.

- If `c` is `'q'` the function should return `"quit"`.
- If `c` is `'r'` the function should return `"reload"`.
- If `c` is `'t'` the function should return `"type"`.
- If `c` is anything else the function should return `"unknown"`.

### Problem 10

Write a function named `four_elements` that takes a list named `xs`. If `xs` contains 10 or more elements then the function should simply return the first 10 elements of the list. Otherwise, if the list contains less than 10 elements, the function should return a list that repeats the elements of the original list and that contains exactly 10 elements.

**Examples**

- `ten_elements [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12]` should return `[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]`.
- `ten_elements [1, 2, 3]` should return `[1, 2, 3, 1, 2, 3, 1, 2, 3, 1]`.