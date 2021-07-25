# Logic and Bit Operations in Python

## Computer Logic

### `and`

- A logical conjunction operator

- A binary operator with a priority that is lower than the one expressed by the comparison operators

### `or`

- A disjunction operator

- A binary operator with a lower priority than `and`

### `not`

- A unary operator performing a logical negation

- `not` turns truth into falsehood and falsehood into truth

- A very high priority operator

## Logical Values

Logical operators take their arguments as a whole regardless of how many bits they contain.

- A value is `True` if it is not zero (when at least one bit is set)

- A value of `False` if it is zero (when all the bits are reset)

## Bitwise Operators

- `&` (ampersand) - bitwise conjunction

- `|` (bar) - bitwise disjunction

- `~` (tilde) - bitwise negation

- `^` (caret) - bitwise exclusive or (xor)