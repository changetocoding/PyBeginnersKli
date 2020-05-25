# Functions II
### Functions you already know
```python
print('it')  # takes in one argument. No return
input() # no argument. Returns string
len('string') # one argument. Returns number
```

# Why functions:
1. Reusablility - Copy and pasting, only need to change in one place - Don't repeat yourseilf
2. Modularity - Small building bricks build a house:
Say we want to extend the phone book example so it loads the telephone numbers from a saved file
```python
# Code to read the file in
...

# Code to copy the contents of the file to the dictionary
...

# Code to get the name form the user and query the dictionary
...
```
Can structure it using functions
```python
def read_file():
    # Code to read the file in
    ...
    
def update_dictionary():
    # Code to copy the contents of the file to the dictionary
    ...

def query_dictionary(name):
    # Code to get the name form the user and query the dictionary
    ...
    
read_file()
update_dictionary()
while True:
    name = input('Please enter a name)
    no = query_dictionary(name)
    print('The number is: ' + str(no))
```

# Syntax
```python
def <function_name>(<parameters>):
    <statement(s)>
    return ...
```
parameters & return statement are optional
```python
<function_name>(<arguments>)
```
To use it is the function name with parameters in brackets. Arguments are optional
```python
def my_func(no):
    return no + 10

my_func(19)
```

# An example
```python
from random import choice

def random_name_generator(first, second, no_of_random_names):
    """
        Generates random names.
        Arguments:
         - list of first names
         - list of last names
         - number of random names
    """
    names = []
    for i in range(no_of_random_names):
        names.append("{0} {1}".format(choice(first), choice(second)))
    return set(names)


first_names = ["Drew", "Mike", "Landon", "Jeremy", "Tyler", "Tom", "Avery"]
last_names = ["Smith", "Jones", "Brighton", "Taylor"]
names = random_name_generator(first_names, last_names, 5)

print('\n'.join(names))
```


# Recursion. A better example.

### Finding all files on your computer

### Org chart
```python
{ sales: { employees: ['Tom', 'Peter'] }, it: { dev: [ 'James', 'Jane' ], support: [ 'Sarah' ] }}
```

# Homework:

### Read:
https://realpython.com/defining-your-own-python-function/
