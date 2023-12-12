# Chapter 2 references

For your convenience this section contains a list of some of the functions that were introduced in [Chapter 2](http://learnyouahaskell.com/starting-out). You will want to use some of these functions to complete the problems in this homework assignment.

## Functions that work on lists

| Name | Type signature | Description |
| --- | ----------- | - |
| `(++)` | `[a] -> [a] -> [a]` | Takes two lists and concatoeates them into one list. |
| `(:)` | `a -> [a] -> [a]` | The "cons" operator (short for "constructor"). Takes an element and a list and adds the element to the front of the list. |
| `(!!)` | `[a] -> Int -> a` | Takes a list and an index and returns the element at that index. |
| `head` | `[a] -> a` | Takes a list and returns its "head", the first element. |
| `tail` | `[a] -> [a]` | Takes a list and returns its "tail", everything except for the "head". |
| `last` | `[a] -> a` | Takes a list and returns its last element. |
| `init` | `[a] -> [a]` | Takes a list and returns everything except its last element. |
| `length` | `[a] -> Int` | Takes a list and returns its length. |
| `null` | `[a] -> Bool` | Checks if a list is empty. If it is, it returns `True`, otherwise it returns `False`. |
| `reverse` | `[a] -> [a]` | Reverses a list. |
| `take` | `Int -> [a] -> [a]` | Takes number and a list. It extracts that many elements from the beginning of the list. |
| `drop` | `Int -> [a] -> [a]` | Takes number and a list. It drops that many elements from the beginning of the list. |
| `maximum` | `Ord a => [a] -> a` | Takes a list of stuff that can be put in some kind of order and returns the biggest element. |
| `minimum` | `Ord a => [a] -> a` | Takes a list of stuff that can be put in some kind of order and returns the smallest element. |
| `sum` | `Num a => [a] -> a` | Takes a list of numbers and returns their sum. |
| `product` | `Num a => [a] -> a` | Takes a list of numbers and returns their product. |
| `elem` | `Eq a => a -> [a] -> Bool` | Takes a thing and a list of things and tells us if that thing is an element of the list. |
| `cycle` | `[a] -> [a]` | Takes a list and cycles it into an infinite list. |
| `repeat` | `a -> [a]` | Takes an element and produces an infinite list of just that element. |
| `replicate` | `Int -> a -> [a]` | Takes a number and an element and produces a list of just that element and with a length equal to the number. |

## Comparison functions

| Name | Type signature | Description |
| --- | ----------- | - |
| `(==)` | `Eq a => a -> a -> Bool` | Returns `True` if the two arguments are the same, otherwise it returns `False`. |
| `(\=)` | `Eq a => a -> a -> Bool` | Returns `True` if the two arguments are NOT equal, otherwise it returns `False`. |
| `(<)` | `Ord a => a -> a -> Bool` | Returns `True` if the first argument is less than the second argument, otherwise it returns `False`. |
| `(>)` | `Ord a => a -> a -> Bool` | Returns `True` if the first argument is greater than the second argument, otherwise it returns `False`. |
| `(<=)` | `Ord a => a -> a -> Bool` | Returns `True` if the first argument is less than or equal to the second argument, otherwise it returns `False`. |
| `(>=)` | `Ord a => a -> a -> Bool` | Returns `True` if the first argument is greater than or equal to the second argument, otherwise it returns `False`. |
| `min` | `Ord a => a -> a -> a` | Takes two arguments are returns the smaller one. |
| `max` | `Ord a => a -> a -> a` | Takes two arguments and returns the larger one. |

## Boolean operators

| Name | Type signature | Description |
| --- | ----------- | - |
| `not` | `Bool -> Bool` | Takes a Boolean and returns the opposite. |
| `(&&)` | `Bool -> Bool -> Bool` | Returns `True` if both arguments are `True` and returns `False` otherwise. |
| `(\|\|)` | `Bool -> Bool -> Bool` | Returns `True` if one or both arguments are `True` and returns `False` otherwise. |

