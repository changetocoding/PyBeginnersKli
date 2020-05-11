# Intro
In this lesson we will go over what we have covered so far and cover functions


# Data types
### Basic types
List all basic types you know

### Lists 
Briefly cover sets and tuples

### Dictionary

# Control statements

### If

### For/While Loops
- For loop
- Range
- While Loop
- break


# Functions

Functions group together logic & code. Scope of variables only within function too.
```python
def increment_by_one(count):
	new_count = count + 1
	return new_count
```

What do you think happens in this scenario
```python
p = 20

def increment_by_one(count):
	count = count + 10
	return count
	
b = inc(p)

# What do you think value of b is?
# What do you think value of p is?

```

# Homework

HW https://classroom.udacity.com/courses/ud1110 Lesson 4
( Covers Dictionaries, if, for, while loops, enumerate, zip)

HW Fizz Buzz -Fun drinking game and teaching tool for division for kids.  
Count from 1 to 100. For each number output "This is X out of 100"  
Any number divisible by three is replaced by the word fizz and any number divisible by five by the word buzz. Numbers divisible by 3 and 5 become fizz buzz.

Sample output:
> This is 1 out of 100  
> This is 2 out of 100  
> Fizz  
> This is 4 out of 100  
> Buzz  
> Fizz  
> This is 7 out of 100  
> ...  

Additional Homework: https://realpython.com/python-dicts/
