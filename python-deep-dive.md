### Multiple line strings 

Physical line of code may be different from logical line of code.
Sometimes, physical newlines are ignored in order to combine them into one logical line of code. 

*IMPLICIT LINE CONTINUATION*

For example: it is okay to write a list as: 
```python
l = [1, 
     2, 
     3
    ]
```
Python will automatically remove the physical newlines. We can do this for functions as well. 
```python 
def my_fun(a, 
           b, # a comment
           c):
    # other stuff here 

```

*EXPLICIT LINE CONTINUATION*

Multi-line statements are not implicitly converted to a single line. Do it explicitly, by using the \ (backslash) character. 

(Can not put comments after the \ on the same line)

Example: 
```
if a \ # this is a comment 
   and b: 
    some stuff
```
The above will not work.

Multi line strings

Use triple delimiters (''' or """)

Example: 
'''This is a 
   multi-line literal'''

* We don't have the *switch* statement in Python. 


