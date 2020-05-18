Next week is last week in course. Course continuation

# Homework review
- Fizz buzz
- Udacity course
- Indentation. Should use spaces (instead of tabs) and use 4 (recommended & everyone does this). The online repl uses 2 and can't change it

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


# Recursion
This is when a function calls itself.

```python
# Summing numbers recursively

def sum(list):
    if len(list) == 1:
        return list[0]
    else:
        return list[0] + sum(list[1:])

print(sum([5,7,3,8,10]))

```

  
Recursion happens a lot languages. An example:
> Every human's mother and father is a human.

So lets rewrite it as a function:

is_human(person) = is_human(person.Father) && is_human(person.Mother)

So would look like
```python
def is_human(alien): 
   return is_human(alien.father) && is_human(alien.mother)
```
So now I'm like is John a human?
Well to know that I need to know if Johns parents are human. To know that I need to know if thier parents (john's grandparents) are human.

Limit of recursion. Python stops the function calls after a depth of 1000 calls.

Very important: Every recursive function can be rewritten as a for or a while loop!


### Fibonacci numbers

Fibonacci numbers are a sequence that is got by adding the previous two numbers.

The sequence looks like this: 0, 1, 1, 2, 3, 5, 8, 13, 21, 34  
https://www.mathsisfun.com/numbers/fibonacci-sequence.html (Stop reading after section The Rule)

There are several ways to solve this.

Solve it using 3 different ways:
1. For loop
2. While loop
3. Recursion

# Lamadas:
Shorthand for writing a function

# Code from the class
```python
books = ['The wind in the willows', 'Harry potter', 'Lord of the rings']
authors = ['No idea', 'JK Rowling', 'JR Tolkien']

# zip
#for i in range(3):
#  author = input('Enter the author\n')
#  authors.append(author)
#
#  book = input('Enter the book\n')
#  books.append(book)
#
#for book, author in zip(books, authors):
#    print("{} was written by {}".format(book, author))

# enumerate
#for book in books:
#  print(book)

#for i in range(0, len(books)):
#  print(books[i])

#for i in range(0, len(books)):
#  book = books[i]
#  print('The {}th book is {}'.format(i, book))

#for i, book in enumerate(books):
#  print('The {}th book is {}'.format(i, book))


def fizz_buzz(last_no):
  for count in range(last_no):
    if (count % 15 == 0):
      print('fizz buzz')
    elif (count % 3 == 0):
      print('fizz')
    elif (count % 5 == 0):
      print('buzz')
    else:
      print('This is {} out of {}'.format(count, last_no))


def increment_by_ten(count):
   count = count + 10
   return count

p = 20
b = increment_by_ten(p)

# What do you think value of b is?
# What do you think value of p is?
#print(b) # 30
#print(p) # 20


def fib_rec(no):
  if no == 1 or no == 2:
    return 1

  return fib_rec(no - 1) + fib_rec(no - 2)

def fib_for(no):
  if no == 1 or no == 2:
    return 1

  nminus1 = 1 
  nminus2 = 1 
  total = 0
  for i in range(3, no + 1):
    total = nminus1 + nminus2
    nminus2 = nminus1
    nminus1 = total

  return total

def fib_arr(no):
  arr = [1, 1]
  if no == 1 or no == 2:
    return 1

  latest = 0
  for i in range(2, no):
    latest = arr[i - 1] + arr[i - 2]
    arr.append(latest)

  return arr


print(fib_arr(10))
```


# Homework
## David's funky numbers

David's funky numbers are defined as:
> d(n) = -2 * d(n-1)  
> d(1) is always -1

The first 10 numbers are -1, 2, -4, 8, -16, 32, -64, 128, -256, 512

Pick recursion and one other way of writing it from below and write a method (for each way) that calculates the value of the number at n.
- For Loop
- Do while loop
- Recursively

E.g:
```python
david_funky_no_for_loop(3) // returns -4
david_funky_no_while_loop(5) // returns -16
david_funky_no_recursion(10) // returns 512
```

## Course book
HW: https://classroom.udacity.com/courses/ud1110 Lesson 5 Functions). (Functions, variable scope, default arguments, lamda functions).
