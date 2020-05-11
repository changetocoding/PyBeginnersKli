# Intro
In this lesson we will go over what we have covered so far and cover functions


# Homework review
- Go through udacity course and any questions
- Phonebook part I

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

We didn't cover break but that allows you to terminate the loop prematurely (aka jump out of it)

### Code from the class
```python
# 
#int  - 7
#float  - 7.1, 7.0
#string - "hello" 'hello "dhdhd"'
#boolean - True or False

list = [ "apple", "pear"] # Mutable. Can change
tuple =  "apple", "pear", "bananna"
set = { "apple", "pear", "pear" }  

dict = { "apple":1}
#print("apple" in dict)

#print(set)

#a1, b, c = tuple

#print(a1)
#print(b)
#print(c)


dimensions = 52, 40, 100
length, width, height = dimensions
#print("The dimensions are {} x {} x {}".format(length, width, height))
#print("The dimensions are " + length + " x " + width + " x " + height)

day = "today"
#print("hello {}, it is nice to see you {}.".format("peter", day))
#print("hello " + "peter" + ", it is nice to see you " + day + ".")


a = "pillow"  # Sets a variable
#"hello" == "hello" # Checks
#print(a)
#print("Hello" == "hello")

b = "hello"
if a == "hello":
  b = "test"
  c = "dog"
  print("Hello is A")

#if a == "hello":
#  print(b)  
#  print(c)
#  print("A is an object")
#elif a == "case":
#  print("A is a case")
#else:
#  print(b)  
#  print("A is not hello")

for i in range(0,10):
  print("Hello world" + str(i))

print()

i = 0
while i < 10:
  print("Hello world" + str(i))
  i = i + 2
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

Additional Homework for Nic is phonebook homework from last week
