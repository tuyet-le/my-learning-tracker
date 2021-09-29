# Dictionaries

A dictionary is a Python data structure that is not a sequence type but can easily be adapated for sequence processing, is mutable and unordered. It is a key-value set. Note:
* each key must be unique - it's not possible to have more than one key of the same value;
* a key may be any immutable type of object: it can be a number (integer or float), or a string, but not a list;
* a dictionary is not a list - a list contains a set of numbered values, while a dictionary holds pairs of values;
* the `len()` function works for dictionaries - it returns the numbers of key-value elements in the dictionary;
* a dictionary is a one-way tool - if you have an English-French dictionary, you can look for French equivalents of English terms, but not vice versa.
* dictionaries don't preserve the order of their data like lists (in Python 3.6x dictionaries have become ordered collections by default so your results may vary depending on what Python version you are using).

The following is the syntax to creating a dictionary:
```
my_dictionary = {
    key1: value1,
    key2: value2,
    key3: value3,
    }
```

## Useful dictionary methods:
* `keys()` - returns an iterable object consisting of all the keys gathered within the dictionary
```
dictionary = {"cat": "chat", "dog": "chien", "horse": "cheval"}

for key in dictionary.keys():
    print(key, "->", dictionary[key]

# Output:
horse -> cheval
dog -> chien
cat -> chat
```

* `sorted()` - sort the dictionary
```
for key in sorted(dictionary.keys()):
```

* `items()` - returns tuples where each tuple is a key-value pair. This is how it works:
```
dictionary = {"cat": "chat", "dog": "chien", "horse": "cheval"}

for english, french in dictionary.items():
    print(english, "->", french)

# Outputs:
cat -> chat
dog -> chien
horse -> cheval
```

* `values()` - this works similarly to `keys()`, but returns values. This is how it works:
```
dictionary = {"cat": "chat", "dog": "chien", "horse": "cheval"}

for french in dictionary.values():
    print(french)

# Outputs:
chat
chein
cheval
```

* `update()` - insert an item into a dictionary.
```
dictionary = {"cat": "chat", "dog": "chien", "horse": "cheval"}

dictionary.update({"duck": "canard"})
print(dictionary)

# Outputs:
{'cat': 'chat', 'dog': 'chien', 'horse': 'cheval', 'duck': 'canard'}
```

* `del` - remove a key and its associated value in a dictionary. (Note: deleting a non-existing key will raise an error.)
```
dictionary = {"cat": "chat", "dog": "chien", "horse": "cheval"}

del dictionary['dog']
print(dictionary)

# Outputs
{"cat": "chat", "horse": "cheval"}
```

* `get()` - to access a dictionary item.

* `copy()` - to copy a dictionary.

* `dict()` - convert a list into a dictionary.