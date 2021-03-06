# Functions II
### Functions you already know
```python
print('it')  # takes in one argument. No return
input() # String argument. Returns string
len('string') # one argument. Returns number
```

We can use input to get user input from the console. useful for homework
```python
users_name = input('Please enter your name\n') 
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
    name = input('Please enter a name')
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


# Recursion. Better example.

### Finding all files on your computer
Its either a file or directory. if its a directory call the method recursively with that directory

### Org chart
```python
org_chart = { sales: { employees: ['Tom', 'Peter'] }, it: { dev: [ 'James', 'Jane' ], support: [ 'Sarah' ] }}
```

# Class notes
```python
#d(n) = -2 * d(n-1)
#d(1) is always -1


def david_rec(n):
  if n == 1:
    return -1

  return -2 * david_rec(n-1)


# For loop
def david_for(n):
  last_no = -1
  if n == 1:
    return last_no

  for i in range (1, n):
    last_no = -2 * last_no 

  return last_no


def david_for_list(n):
  prev_nos = [-1]
  if n == 1:
    return prev_nos[0]

  for i in range (1, n):
    current = -2 * prev_nos[-1]
    prev_nos.append(current)

  return prev_nos


# While loop
def david_while(n):
  last_no = -1
  if n == 1:
    return last_no

  # index= 1 then last_no = -1. We stop at n
  # n = 3
  index = 2
  while index <= n:
    last_no = -2 * last_no
    index = index + 1

  return last_no


def david_while_list(n):
  prev_nos = [0, -1]
  if n == 1:
    return prev_nos

  # index= 1 then last_no = -1. We stop at n
  # n = 3
  index = 2
  while index <= n:
    current = -2 * prev_nos[index - 1]
    print('prev_nos {}. Index {}. Current {}'.format(prev_nos, index, current))
    prev_nos.append(current)
    index = index + 1

  return prev_nos


print(david_while(1))
print(david_while(2))
print(david_while(3))
print(david_while(6))
```


# Homework:
### Phonebook part II
We are going to extend phonebook to take in user input & store the number as an int

Write a new script that takes 2 commands
- Add: the user can enter name and a number. e.g David 345678901
- Query: the user can query the phone book using a name: given a name it returns the number of the person. Return a useful error message if the person does not exist.
IMPORTANT The user will always enter the correct commands and input (e.g. the number will not have any letters in it) so dont need to write code to check. The user will enter first name only and will always begin with a capital letter.

E.g. sample input/output
```
>Please enter an instruction:  # This is outputted by your script
Add David 2345678901           # This is what the user entered
>Please enter an instruction:   
Add Tom 12345678900  
>Please enter an instruction:   
Query David   
>David's number is 2345678901
>Please enter an instruction:
Add Peter 12345678911
>Please enter an instruction:
Query Thomas   
>No Thomas found
>Please enter an instruction:
```

Where > is used to indicate the system responses from your script

**Now convert the adding & querying into functions**
```python
def add_number(name, number):
    ...
    
def query_number(name):
    ...
```

**Bonus points**
Uk Telephone numbers are 11 numbers. But normally start with a 0. E.g. 02081114444 or 0771234444
How can you store this as an int, but be able to correctly print the number with the leading 0s?


### Additional reading (optional):
https://realpython.com/defining-your-own-python-function/
