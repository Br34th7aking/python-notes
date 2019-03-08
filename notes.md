

### Chapter 18 
This is the final chapter on Object-oriented programming in this book. Here, Allen takes an example of a card game, and talks about inheritance. 

#### Inheritance
Again, I like the way he defines inheritance - a way to define a new class that is a modified version of an existing class. 


#### Class attributes
Next, I learned about class attributes. These attributes are common across all the instances of a class. They are accessed using '.' notation, with the class name as prefix. 

Example: `Card.suit` where card is a class. 


#### An interesting use for tuples
Tuples can be used to compare objects where two or more properties are used for comparison. For example
```python
def __lt__(self, other):
    t1 = self.suit, self.rank
    t2 = other.suit, other.rank

    return t1 < t2

```

Python  has an MRO(Method Resolution Order) which it uses to determine which method to call.


### Chapter 19

Here, Allen mentions some other niceties that are available in Python. 

**Conditional Expressions**

These expressions can be used to simplify writing small conditional statements. 

For example: Look at the code below
```python
if x > 0:
    y = math.log(x)
else:
    y = float('nan')
```

This can be simplified using a conditional expression as below: 

```python
y = math.log(x) if x > 0 else float('nan')
```

**List Comprehensions**

One of the most wonderful things I've seen in Python.
Example: 
```python
words = [word for word in data.readline().split()]
```

**Generator Expressions**
Generator expressions are like list comprehensions but with two differences: 

1. They have parantheses instead of square brackets.
2. They do not generate the entire sequence at once. Instead, they wait till asked. 

Example: 
```python
g = (x**2 for xx in range(5))
```

This creates a generator object which knows how to access the elements. We access the elements using the `next()` function. Example: `next(g)`


**any and all**

*any* takes a sequence of booleans and returns True if any of the values are True.

Example: 

```python
any( letter == 't' for letter in 'monty')

```
*all* returns True only if all the elements of the sequence are True.

**collections**
He also talks briefly about the `collections` module and mentions some important ones like Counter, defaultdict, namedtuples.

Wonderful Book, overall!


