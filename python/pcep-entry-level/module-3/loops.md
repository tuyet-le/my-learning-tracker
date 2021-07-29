# Loops

## Types of loops in Python

There are two types of loops in python: `while` and `for`.

- The `while` loop executes a statement or a set of statments as long as a specifed boolean condition is true.

- The `for` loop executes a set of statements many times; you can use it to iterate over a sequence (e.g. a list, dictionary, tuple or a set).

## Loop control in Python

`break` - exit a loop

```
text = "I'm learning Python."

for letter in text:
    if letter == "p":
        break
    print(letter)
```

`continue` - skip the current block, and continue with the next iteration

```
text = "I'm learning Python w!"

for letter in text:
    if letter == "w":
        continue
    print(letter)
```

`range(start, stop, step)` - generates a sequence of numbers

- `start` is an optional parameter specifying the starting number of the sequence (`0` by default)
- `stop` is an optional parameter specifying the end number of the sequence generated (it is not included)
- `step` is an optional parameter specifying the difference between the numbers in the sequence (`1` by default)

```
for i in range(3):
    print(i, end=" ") # Outputs: 0 1 2

for i in range(6, 1, -2):
    print(i, end=" ") # Outputs 6 4 2
```