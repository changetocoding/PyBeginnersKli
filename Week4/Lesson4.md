# Homework review
- Fizz buzz
- Udacity course
- Talk about indentation. Use spaces and use 4 (recommended & everyone does this). The online repl uses 2 and can't change it

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


# Homework
## David's funky numbers

David's funky numbers are defined as:
> d(n) = k * -1 * d(n-1)
> d(1) is always -1
Where k is a constant given to you

Write 3 methods that calculates the david funky number at n (given k) 3 different ways
- For Loop
- Do while loop
- Recursively

```python
// called method with positional arguments:
david_funky_no_for_loop(n = 4, k = 10) // prints 1000

// for the next two n is the first parameter, and k is the second parameter
david_funky_no_while_loop(5, 2) // prints -16. n is 5, k is 2
david_funky_no_recursion(9, 10) // prints -100000000. n is 9, k is 10
```

If you are struggling with it, do it without the K
> d(n) = -1 * d(n-1)
> d(1) is always -1

Then add in the k afterwards


## Course book
HW: https://classroom.udacity.com/courses/ud1110 Lesson 5 Functions). (Functions, variable scope, default arguments, lamda functions).
