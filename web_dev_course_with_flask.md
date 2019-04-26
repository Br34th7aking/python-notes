### Complete Python Web Course with Flask - Udemy

#### Unit 1

The course starts with an introduction to Python. 

The first interesting thing I found here was the ```format()``` method.

It formats the **string** and puts placeholder values in the string. 

Example: 
```python
randomString = "This is species {}".format(8472)
```

#### Unit 2

Virtual environments: This allows us to keep our dependencies(libraries etc.) separate for each project. 
This helps when two different projects depend on different versions of a dependency. (Ex: Django 1.9 and Django 2.1)

To create a virtual environment, first check if **pipenv** is installed.
If yes, **cd** into your project, and then, run
```pipenv install <package_name>```

To activate the pipenv shell, use ```pipenv shell```

**JSON format example**
```json
{
	"students": [ ... ],
	"courses": [ {..}],
}
```

* We can use the **requests** library to make a get request.
Example: 
```python
import requests

request = requests.get(url)
print(request.content)
```

