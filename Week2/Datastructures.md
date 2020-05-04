# Lesson 2: Grouping things

### Homework review
- Udacity course
- Bart simpson
- Homework difficulty
- Where does the name 'Python' come from?

### Overview
In this lesson we will cover how to get help and datastructures for grouping things:


### Documentation/Getting help
- [official python docs](https://docs.python.org/3/tutorial/index.html)
- [Stackoverflow](https://stackoverflow.com/questions/tagged/python) Q&A site
- Just [google](https://lmgtfy.com/?q=python+for+loop) (or your favourite search engine) it 
- Ask fellow classmates  

### Lists
Collection of objects. Flexible size

```python
a = [12, 14, 56, 60]
```

Index | Value
--- | ---
a[0] | 12
a[1] | 14
a[2] | 56
a[3] | 60

A list is indexed starting at 0.

To add an item use the append method

To delete use del keyword. Note this rearranges the array to fill in the space

```python
my_list = [1, 3, 4]
del my_list[1]
print(my_list) # [1, 4]
```

The len keyword gives you the size of the list
```python
len(my_list)
```

Lists are iterable (more on iterable in a later course). Iterable basically means that you can use a for loop on them
```python
basket = ['apple', 'orange', 'apple', 'pear', 'orange', 'banana']
for item in basket:
    print(item)
```


Little aside: range() from lesson 1 is also iterable. To get range as a list use the list keyword: 
```python
list(range(0,10))
```

### Sets
List but makes sure items are unique

```python
basket = {'apple', 'orange', 'apple', 'pear', 'orange', 'banana'}
# {'pear', 'banana', 'orange', 'apple'}
```

### Tuples 
List but immuatable: Can't change once created. Very useful for other stuff


```python
# To create
places = ('1st', '2nd', '3rd')
# to deconstruct it
first, second, third = places
print(third) # 3rd
```


### Dictionaries
A way to map a key to a value. Similar to a real life dictionary.
It is really fast (fetching is as fast as fetching in an array using index)

```python
my_dict = { 'David' : 30, 'Paul' : 45 }

david_age = my_dict['David'] # 30

# add a new item
my_dict['mynewkey'] = 50
```


### Code from the class
```python
#https://github.com/changetocoding/PyBeginnersKli/blob/master/Week2/Datastructures.md

#print('Welcome to class')

animal = 'dog'
name = 'pete'
action = 'run'

#print('Does your {} named {} {}?'.format(animal, name, action))
#print('Does your ' + animal + ' named ' + name + ' run?')


#for i in range(100):
#  print('I will not get very far with this attitude.')


#a = 1
#while a < 101:
#  print('I will not draw naked ladies in class.')
#  a = a + 1

#letters_list = ['a', 'b', 'c']
#print(letters_list)
var_list = [animal, name, action]
#print(var_list)
#no_list = [14, 67, 89, 88, 23]
#print(no_list)

#print(no_list[1])
#print(var_list[2])
#print(letters_list[0])

#print(var_list[1])


var_list.append('Does your')
#print('After append:')
#print(var_list)

#del var_list[1]
#print('After delete:')
#print(var_list)


#print(var_list)

size_of_list = len(var_list)

# Dont do this
#for i in range(0, size_of_list):
#  print(var_list[i])

# Do this instead
#for item in var_list:
#  print(item)

# list []
# set {}
# tuple ()
#basket = {'apple', 'orange', 'apple', 'pear', 'orange', 'banana', 'kiwi'}

# Use add instead of append for sets
#basket.add('lemon')
#basket.add('pear')



# You can upack tuples into variables
#basket_tuple = ('apple', 'orange', 'apple')
#first_fruit, second_fruit, third_fruit = basket_tuple

#print(first_fruit)
#print(second_fruit)
#print(third_fruit)


#address_dict = {'David' : 5655665, 'Paul' : animal }
#address_dict['Sarah'] = 838383

#print(address_dict['Sarah'])

#name = input('Enter a name: \n')
#print(name)

#if name == 'david':
#  for i in range(30):
#    print('Happy birthday')
#elif name == 'alice':
#  print('its not your birthay')
#else:
#  print('hello {}'.format(name))


months = [ 'Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun']

#for i in range(0, len(months)):
#  print(months[i])

month = input('Enter a month: \n')
months_dict = { 'Jan' : 1, 'Feb' : 2, 'Mar' : 3, 'Apr' : 4, 'May' : 5, 'Jun' : 6 }
month_no = months_dict[month]
print('The month number is: ' + str(month_no))
```

# Homework
HW: [Udacity Course](https://classroom.udacity.com/courses/ud1110) Lesson 3 (Data Structures. Apx 3 hours)  
HW: Phonebook Part 1:
The task is to create a simple phonebook.

1. Use a dictionary. Initialise it with some names and numbers
2. Add a name and a number to the dictionary
3. Add more names to the dictionary
4. Fetch a number from the dictionary using a name. Print it on the screen
5. Delete a name/number pair from the dictionary.

You should store the number as a string (becase of the leading 0's in a telephone number)



Optional: [lists](https://www.learnpython.org/en/Lists)  
Optional: [Conditionals](https://www.learnpython.org/en/Conditions)  
