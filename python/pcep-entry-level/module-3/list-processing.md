# Operations on lists

## Slice

A slice is a Python element that allows you to make **a brand new copy of a list or parts of a list**. It copies the contents of the list and not the list's name.

Different types of slice notations:

```
my_list[start:end]   # slice begins from first index to end end-1
my_list[:end]        # slice begins at element 0 through to end-1
my_list[start:]      # slice begins from first element through to the rest of the list
my_list[:]           # copies the whole list
```

- `start` is the index of the first element included in the slice

- `end` is the index of the first element not included in the slice


Examples:

```
my_list = [10, 8, 6, 4, 2]
new_list = my_list[1:-1]
print(new_list)  # Outputs: [8, 6, 4]
```

```
my_list = [10, 8, 6, 4, 2]
new_list = my_list[:]
print(new_list)  # Outputs: [10, 8, 6, 4, 2]
```

If the `start` specifies an element lying further than the one described by the `end` (from the list's beginning point of view), the slice is **empty**.

```
my_list = [10, 8, 6, 4, 2]
new_list = my_list[-1:1]
print(new_list)  # Outputs: []
```

`del` can be used to delete slices.

```
my_list = [10, 9, 8, 4, 2]
del my_list[1:3]
print(my_list)  # Outputs: [10, 4, 2]
```

**Important**: the above example doesn't produce a new list.

## `in` and `not in` operators

The `in` and `not in` are two powerful Python operators to look through the list to check whether a specfic value exist inside a list or not.

```
elem in my_list       # returns True if element is in my_list
elem not in my_list   # returns True if element is not in my_list
```

Lab: remove duplicates in a list

```
my_list = [1, 2, 4, 4, 1, 4, 2, 6, 2, 9]
unique_list = []

for i in my_list:
    if i not in unique_list:
        unique_list.append(i)
    
print(f"The list with unique elements only: {unique_list}")
```