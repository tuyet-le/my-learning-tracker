# Multidimensional Arrays

## List Comprehension

List comprehensions offers a shorter and consise syntax when you want to create new lists from existing ones.

```
[expression for element in list if conditional]
```

The above is equivalent to:

```
for element in list:
    if conditional:
        expression
```

Examples of using list comprehension:

The following code creates a five-element list filled with the first five natural numbers raised to the power of 3:

```
cubed = [num ** 3 for num in range(5)]
print(cubed)    # Outputs: [0, 1, 8, 27, 64]
```

## Nested Lists

You can create two-dimensional lists (i.e. matrices) using nested lists.

```
# A four-column/four-row table - a two dimensional array (4x4)

table = [[":(", ":)", ":(", ":)"],
         [":)", ":(", ":)", ":)"],
         [":(", ":)", ":)", ":("],
         [":)", ":)", ":)", ":("]]

print(table)
print(table[0][0])   # Outputs: ':('
print(table[0][3])   # Outputs: ':)'
```

You can nest as many lists in lists as you want and therefore create n-dimensional lists.