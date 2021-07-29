# Bubble Sort

There are many sorting algorithms that differ a lot in speed and complexity.

The bubble sort is a very simple algorithm and easy to understand but it is not efficient to use for very large and extensive lists.

The bubble sort is done by comparing adjacent elements in a list and swapping some of them.

## Sorting a list

```
my_list = [8, 10, 6, 2, 4]  # list to sort
swapped = True  # It's a little fake, we need it to enter the while loop.

while swapped:
    swapped = False  # no swaps so far
    for i in range(len(my_list) - 1):
        if my_list[i] > my_list[i + 1]:
            swapped = True  # a swap occurred!
            my_list[i], my_list[i + 1] = my_list[i + 1], my_list[i]

print(my_list)
```

## `sort`

There is a simpler way to sort a list in Python - the `sort` method.

```
my_list = [8, 10, 6, 2, 4]
my_list.sort()
print(my_list)  # Outputs [2, 4, 6, 8, 10]
```

## `reverse`

Use `reverse` to reverse a list.

```
lst = [5, 3, 1, 2, 4]
print(lst)

lst.reverse()
print(lst)  # Outputs: [4, 2, 1, 3, 5]
```