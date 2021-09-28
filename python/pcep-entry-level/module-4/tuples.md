# Tuples

## Sequence types and mutability

A sequence type is a type of data in Python which stores more than one value (or less than one, as a sequence may be empty), and these values can be sequentially browsed, element by element. The list is classic example of a Python sequence.

## What is a tuple?

A tuple is an immutable sequence type that behaves like a list, but it cannot be modified in situ. An `AttributeError` exception will be raised if you try to modify a tuple's content.

Tuples use parenthesis whereas lists use brackets, although it's possible to create a tuple just from a set of values separated by commas. Each tuple element can be of a different type.

```
tuple_1 = (1, 2, 4, 8)
tuple_2 = 1., .5, .52, .125

print(tuple_1)  # outputs: (1, 2, 4, 8)
print(tuple_2)  # outputs: (1., .5, .52, .125)