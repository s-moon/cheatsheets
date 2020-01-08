# Python

# Variables
* Start with letter, underscore
* May contain number (but see above)

# Comments
```
# Like this
```

# Types
* int
* float
* string

## Zen of Python
In interpreter:

```import this```

## Strings
```
name = 'Stephen'
name = "Stephen"
owner = "Stephen's"
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
```