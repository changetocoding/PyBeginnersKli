# Lesson 2: Grouping things

### Homework review
- Udacity course
- Bart simpson
- Where does the name 'Python' come from?

### Overview
In this lesson we will cover how to get help and datastructures for grouping things:
Help:
- Documentation
- Stackoverflow

Datastructures:
- Lists  
- Sets  
- Tuples  
- Dictionaries

### Documentation
[official python docs](https://docs.python.org/3/tutorial/index.html)
[Stackoverflow](https://stackoverflow.com/questions/tagged/python) Q&A site
Just (google)[https://lmgtfy.com/?q=python+for+loop] (or your favourite search engine) it 

### Lists
Collection of objects. Flexible size

```python
my_list = [12, 14, 56, 60]
```

Index | Value
--- | ---
my_list[0] | 12
my_list[1] | 14
my_list[2] | 56
my_list[3] | 60

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

Little aside: range() from lesson 1 is also iterable. To get range as a list use the list keyword: list(range(0,10))

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
d['mynewkey'] = 50
```
