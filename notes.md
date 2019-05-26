

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




## Notes from Learn Python 3 the Hard Way - by Zed Shaw 

1. The first interesting thing I noted was in the exercise 5. Here, Zed talks about format strings. Example: 

```python
name = "Abhijit"
print(f"Hello, My name is {name}");
```

This will print: ```Hello, My name is Abhijit```

2. Unpacking from the script input. 
```python
from sys import argv

script, user_name = argv # this will take two arguments on the command line wherwe run the script.

prompt = '> ' # We can use this variable with the input() function to ask for their answer. 
.
.
.
```

3. Multiline print string 
```python 
print(f"""
    Hey, this looks really cool. 
    And your hat looks cool too.
    """)
```
4. Problem Solving Methodology
    1. Write or draw about the problem.
    2. Describe each scene if it's a game. 
    3. Extract key concepts and research them. Identify classes etc. 
    4. Code the classes and a test to run them
    
5. ```dedent``` is used to strip the whitespaces at the beginning of a mulitline string. It can be imported from ```textwrap``` module.


6. Introduction to flask 
    - We write our code in app.py. The html files are kept in 'templates' folder.
    - We need to include render_template() function, and pass it the html file and any variables. 
```python
    def index():
        return render_template('index.html', username=username)
```
    - All the html files in the templates folder can have two special types of tags. {% %} is used to add keywords like if else etc. {{ }} is used for variable names. 

    
