# Functions

A function is a block of code that performs a specific task when the function is called (invoked). You can use functions to make your code reusable, better organised and more readable.

There are at least **four** types of functions in Python:

* built-in functions e.g. `print()`, `input()`
* pre-installed modules
* user-defined functions
* `lambda` functions

## Parameterized Functions

Information can be passed to functions by using parameters. It can have as many parameters as you need.

* **Positional parameter passing** - the order of arguments passed matters

* **Keyword argument passing** - the order of arguments passed doesn't matter

* a mix of positional and keyword parameters can be combined. (Note: positional arguments must not follow keyword arguments)

## `return` from a function

To get functions to return a value, use the `return` keyword.

Important notes:
* If a function doesn't return a certain value using a `return` expression clause, it is assumed that it implicitly returns `None`. See example below:

```
def strange_function(n):
    if (n % 2 == 0):
        return True

print(strange_function(2))   # outputs: True
print(strange_function(1))   # outputs: None
```

## Functions and Scopes

The scope of a name (e.g. a variable name) is the part of a code where the name is properly recognisable. For example, the scope of a function's parameter is the function itself. The parameter can't be accessed outside of the function.

Things to remember:

* A variable existing outside a function has a scope inside the functions' bodies, excluding those of them with the same variable name.

* `global` keyword extends a variable's scope in a way which includes the functions' bodies. It becomes a global scope. For example:

```
def my_function():
    global var
    var = 2
    print("Do I know that variable?", var)


var = 1
my_function()
print(var)

# outputs:
# Do I know that variable? 2
# 2
```

* Changing the parameter's value doesn't propagate outside the function. The function receives the argument's value, not the argument itself. For example:

```
# Example 1:
def my_function(n):
    print("I got", n)
    n += 1
    print("I have", n)


var = 1
my_function(var)
print(var)

# Outputs:
# I got 1
# I have 2
# 1

# Example 2:
def my_function(my_list_1):
    print("Print #1:", my_list_1)
    print("Print #2:", my_list_2)
    my_list_1 = [0, 1]
    print("Print #3:", my_list_1)
    print("Print #4:", my_list_2)


my_list_2 = [2, 3]
my_function(my_list_2)
print("Print #5:", my_list_2)

# Outputs:
# Print #1: [2, 3]
# Print #2: [2, 3]
# Print #3: [0, 1]
# Print #4: [2, 3]
# Print #5: [2, 3]
```

* When the argument is a list, remember that variables containing lists are stored in a different way than scalars. When changing a list identified by the parameter (note: the list)

## Simple Functions Examples

### Two-parameter functions

```
def bmi(weight, height):
    if height < 1.0 or height > 2.5 or \
    weight < 20 or weight > 200:
        return None

    return weight / height ** 2

print(bmi(3, 1.65))
```

### Three-parameter functions

```
def is_a_triangle(a, b, c):
    if a + b <= c:
        return False
    if b + c <= a:
        return False
    if c + a <= b:
        return False
    return True

print(is_a_triangle(1, 1, 1))
print(is_a_triangle(1, 1, 3))
```

The above can be simplified by using a universal expression for testing triangles:

```
def is_a_triangle(a, b, c):
    return a + b > 3 and b + c > a and c + a > b


print(is_a_triangle(1, 1, 1))
print(is_a_triangle(1, 1, 3))
```

### Factorials

A factorial number is equal to the product of all natural numbers from one up to its argument.
```
0! = 1 (yes! it's true)
1! = 1
2! = 1 * 2
3! = 1 * 2 * 3
4! = 1 * 2 * 3 * 4
:
:
n! = 1 * 2 ** 3 * 4 * ... * n-1 * n
```

```
def factorial_function(n):
    if n < 0:
        return None
    if n < 2:
        return 1
    
    product = 1
    for i in range(2, n + 1):
        product *= i
    return product

for n in range(1, 6):  # testing
    print(n, factorial_function(n))
```

### Fibonacci

Fibonacci numbers are a sequence of integer numbers built using a the following simple rules:
* the first element of the sequence is equal to one
* the second element is also equal to one
* every subsequent number is the sum of the two preceding numbers

```
fib_1 = 1
fib_2 = 1
fib_3 = 1 + 1 = 2
fib_4 = 1 + 2 = 3
fib_5 = 2 + 3 = 5
fib_6 = 3 + 5 = 8
fib_7 = 5 + 8 = 13
```

```
def fib(n):
    if n < 1:
        return None
    if n < 3:
        return 1

    elem_1 = elem_2 = 1
    the_sum = 0
    for i in range(3, n + 1):
        the_sum = elem_1 + elem_2
        elem_1, elem_2 = elem_2, the_sum
    return the_sum


for n in range(1, 10):  # testing
    print(n, "->", fib(n))

```

### Recursions

A recursion is a technique where the function invokes itself. Factorials and fibonacci numbers are two cases that illustrate this best.

There is a risk with recursions. If you forget to consider the conditions which can stop the chain of recursive invocations, the program may enter an infinite loop. Recursive calls also consume a lot of memory and therefore may sometimes be inefficient.

```
def factorial_function(n):
    if n < 0:
        return None
    if n < 2:
        return 1
    return n * factorial_function(n - 1)
```