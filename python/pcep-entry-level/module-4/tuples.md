# Tuples

## Sequence types and mutability

A sequence type is a type of data in Python which stores more than one value (or less than one, as a sequence may be empty), and these values can be sequentially browsed element by element. The list is a classic example of a Python sequence.

## What is a tuple?

A tuple is an ordered and immutable sequence type that behaves like a list but it cannot be modified in situ. An `AttributeError` exception will be raised if you try to modify a tuple's content.

Tuples use parenthesis whereas lists use brackets, although it's possible to create a tuple just from a set of values separated by commas. Each tuple element can be of a different type and can also be variables (not just strictly literals).

```
tuple_1 = (1, 2, 4, 8)
tuple_2 = 1., .5, .52, .125

print(tuple_1)  # outputs: (1, 2, 4, 8)
print(tuple_2)  # outputs: (1., .5, .52, .125)
```
A one-element tuple can be created as follow:
```
tuple_1 = ("one",)  # Brackets and a comma
tuple_2 = "one",    # No brackets and a comma

Note: if you remove the comma, you will tell Python to create a variable and not a tuple
```

The following can also be used with tuples:
* `len()` function accepts tuples and returns the number of elements contained inside;
* `+` operator can join tuples together;
* `*` operator can multiply tuples just like lists;
* `in` and `not in` operators work in the same way as in lists.

```
my_tuple = (1, 10, 100)

t1 = my_tuple + (1000, 10000)
t2 = my_tuple * 3

print(len(t2))  # outputs: 9
print(t1)  # outputs: (1, 10, 100, 1000, 10000)
print(t2)  # outputs: (1, 10, 100, 1, 10, 100, 1, 10, 100)
print(10 in my_tuple)  # outputs: True
print(-10 not in my_tuple)  # outputs: True
```
