# Notes from the book Serious Python 

## Chapter 1 
#### Which version of Python should the project support? 
Each minor version has bug-fix support for 18 months and security support for 5 years. 

#### How to layout the project? 
*What to do?*
Standard name for python installation: setup.py
It comes with setup.cfg that has configuration details.

README.rst has important information 
docs contain the package's documentation in reSTructructuredText format,
which is consumed by Sphinx.


*What not to do?*
Do not create modules based on the type of code they will store. Fre exampel: functions.py

Avoid unncessary nesting, such as a module directory that contains only __init__.py

#### Version numbering 
PEP 440 recommendation:
N[.N]+[{a|b|c|rc}N][.postN][.devN]
- Versions matching N[.N]+ are final releases.

#### Time for some PEP8
* Use 4 spaces per indentation level 
* Limit all lines to a max. of 79 characters.
* Seperate top-level function and class definitions with two blank lines.
* Encode files using ASCII or UTF-8
* Use one module import per import statement and per line.
* Class name in CamelCase. Suffix Exceptions with Error, and name functions in lowercase with words and underscores. Use a leading underscore for priveate attributes or methods. 

Can use pep8 tool to check.
pip install pep8

Use flake8 for code style verification.

Flycheck plugin for vim - can run flake8 in code buffer. 

## Chapter 2
"import" keyword is actually a wrapper around a function named "__import__"


#### sys module 
You can retrieve a list of modules currently imported using the sys.modules variable.
```python
import sys 
import os
sys.modules['os']
```

Useful standard libraries: 
* atexit: allows to register functions for program to call when it exits
* argparse: provides functions for parsing command line arguments. 
* bisect: provides bisection algorithms for sorting lists
* calendar: provides a number of date-related functions
* codecs: provides functions for encoding and decoding data.
* collections: provides a variety of useful data structures
* copy: provides functions for copying data. 
* csv: provides functions for reading and writing csv files.
* datetime provides classes for handling dates and times.
* fnmatch provides functions for matching Unix-style filename patterns.
* concurrent provides asynchronous computation (native in Python 3, available for Python 2 via PyPI).
* glob provides functions for matching Unix-style path patterns.
* io provides functions for handling I/O streams. In Python 3, it also contains StringIO (inside the module of the same name in Python 2), which allows you to treat strings as files.
* json provides functions for reading and writing data in JSON format.
* logging provides access to Python’s own built-in logging functionality.
* multiprocessing allows you to run multiple subprocesses from your appli- cation, while providing an API that makes them look like threads.
* operator provides functions implementing the basic Python operators, which you can use instead of having to write your own lambda expres- sions (see Chapter 10).
* os provides access to basic OS functions.
* random provides functions for generating pseudorandom numbers.
* re provides regular expression functionality.
* sched provides an event scheduler without using multithreading.
* select provides access to the select() and poll() functions for creating event loops.
* shutil provides access to high-level file functions.
* signal provides functions for handling POSIX signals.
* tempfile provides functions for creating temporary files and directories.
* threading provides access to high-level threading functionality.
* urllib (and urllib2 and urlparse in Python 2.x) provides functions for handling and parsing URLs.
* uuid allows you to generate Universally Unique Identifiers (UUIDs).

#### Using and choosing frameworks
Difference between frameworks and external libraries is that the application uses frameworks by building on top of them, i.e., by extending them rather than vice versa. 
A library extends the appliation, a framework forms the chassis of your code. 


#### Doug Hellman Interview
Create some code and run it. Have the basic functionality working and then write tests to make sure you've covered all the edge cases. 
