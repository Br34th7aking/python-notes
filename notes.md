

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


