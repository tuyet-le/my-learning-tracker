# Lists

The list is a data type in Python that stores multiple objects. It's an ordered and mutable collection of comma-separated items between square brackets e.g.:

```
favourite_colors = ["yellow", "green", "orange"]
```

Lists can be:
- indexed and updated
- nested
- deleted through using the `del` object
- iterated through using the `for` loop

## Functions vs Methods

A method is owned by the data it works for, while a function is owned by the whole code. Some examples of methods owned by lists:

- `list.append(value)` - the append method adds a new element to the end of an existing list

- `list.insert(location, value)` - the insert method adds a new element at any place in the list

Examples of list functions:

- `len` - return the total number of elements in a list

## Exercises
```
lst = []
del lst
print(lst)

# NameError: name 'lst' is not defined
```

```
lst = [1, [2, 3], 4]
print(lst[1])
print(len(lst))

# [2, 3]
# 3
```