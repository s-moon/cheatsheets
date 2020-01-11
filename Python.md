# Python

## Variables
* Start with letter, underscore
* May contain number (but see above)

## Mutable v Immutable
### Mutable
* Set
* Dictionary
* List
### Immutable
* None
* bool
* int
* float
* str
* tuple

## Comments
```
# Like this
```

## Zen of Python
In interpreter:

```import this```

## Strings
```
name = 'Stephen'
name = "Stephen"
owner = "Stephen's"
```

### F Strings
```
full_name = f"{first_name} {last_name}"
```

### Format method <= Python 3.5
```
full_name = "{} {}".format(first_name, last_name)
```

### Printing
```
print('Hello ' + name)
print('\tHello\n')
```

### Trimming
```
name.strip()
name.lstrip()
name.rstrip()
```

### Case
```
name.lower()
name.upper()
name.title()
```

## Lists
```
sports = []
sports = ['running', 'football']
sports[0] # running
sports[-1] # football
sports[0] = 'swimming'
```

### Length of list
```
len(sports)
```

### Sorted, not stored
```
sorted(sports)
```

### Reverse sorted, not stored
```
sorted(sports, reverse=True)
```

### Reverse order, permanent
```
sports.reverse()
```

### Sort, permanent
```
sports.sort()
sports.sort(reverse=True)
```

### List from range
```
numbers = list(range(1,6))
    print(numbers)
[1, 2, 3, 4, 5] 
```

### List Comprehension
Allows you to combine a for...loop and set in one
```
squares = [value**2 for value in range(1,11)]
print(squares)
```

### Insert
```
sports.insert(0, 'Inserted at front of list')
```

### Append
```
sports.append('Item at end added')
```

### Pop from stack
```
item = sports.pop() # removed but extracted from end
item = sports.pop(2) # removed from position 2
```

### Delete item
```
del sports[1] # remove item at 1
```

### Delete named item
```
sports.remove('item to remove')

pets = ['cat', 'dog', 'cat', 'cat']
print(pets)
while 'cat' in pets:
    pets.remove('cat')
print(pets)
```

### Slices
```
names = ['bill', 'john', 'peter', 'phil']
names[:1] # ['bill']
names[-2:] # ['peter', 'phil']
names[2:3] # ['peter']
```

### Copying list
```
names = ['john']
new_names = names[:]
```

### Testing list is empty
```
names = []
if names: # test that there is something at least, in list
```

## Tuples
Lists that can't be changed. Use round brackets.
```
drinks = ('vodka', 'water', 'wine')
```
Behave exactly like lists, otherwise

## Dictionaries 
* Use curly braces instead of square (like lists)
* Comma separated
* Can use comma on last entry in dictionary

### Dictionaries in dictionaries
```
users = {
    'aeinstein': {
        'first': 'albert',
        'last': 'einstein',
        'location': 'princeton',
        },
    'mcurie': {
        'first': 'marie',
        'last': 'curie',
        'location': 'paris',
        },
    }
```

### Lists in dictionaries
```
fruit = {
    'sam': ['apple', 'strawberry'],
    }
```

### Keys, Values and Items
```
for key in languages.keys():

for value in languages.values():

for key,value in languages.items():
```

## If
```
age = 5

if age == 5:
    # do something
elif age == 6:
    # do something
else:
    # do something
```

## Operators
```
%   # modulo
+
-
/
*
**   # to the power of
```

## Comparisons
```
>
<
>=
<=
!=
==
not
in
```

## For loop
```
people = ['alice', 'david', 'carolina']
for person in people:
    print(person)
```

## Range
```
for value in range(1,5):
    print(value)
1
2
3
4
```
Even numbers
```
even_numbers = list(range(2,11,2))
print(even_numbers)
[2, 4, 6, 8, 10]
```

## Min, Max, Sum
```
>>> digits = [1, 2, 3, 4, 5, 6, 7, 8, 9, 0]
>>> min(digits)
0
>>> max(digits)
9
>>> sum(digits)
45
```

## References
[PEP 8 - Style Guide](https://www.python.org/dev/peps/pep-0008/)
[Python Crash Course 2e - Eric Matthes](https://nostarch.com/pythoncrashcourse2e)