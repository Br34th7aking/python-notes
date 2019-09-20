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


#### The main app.py file 
This file contains the code for different views. We can display different pages by using routes. 

Example code:
```python

from flask import Flask, render_template 

@app.route('/') # decorator
def index():
    return render_template('index.html')

```

Where do these html files go? They reside in a special folder named `templates`.

#### The base.html file.
We can use this file to keep common code and then use templating to get this file's contents into other files. 
Example: 

`base.html`
------------

```html 
<!DOCTYPE html>
...
..
...
{% block content %}

{% endblock %}

```

`index.html`
------------
```flask
{% extends 'base.html %}

{% block content %}
    <h1>This is the index file.</h1>
{% endblock %}
```


#### Where do the css and js files go? 
These files are again stored in a special folder named 'static'. 

And then we can include a css file as follows: 
`<link rel="stylesheet" href="{{ url_for('static', filename = 'css/style.css') }}">`

This way of linking can be used for any other resource file. For example: 
{{ url_for('static', filename='image.jpg') }}


#### How to get a custom 404 page?
@app.errorhandler(404) # app.route ke jagah app.errorhandler
def page_not_found(e):
    return render_template('404.html'), 404



**Finished the book Flask by Example. It was a great read.**

#### Notes from Building Web Applications with Flask

* Flask is not an MVC framework, as it does not implement the model layer. You are free to choose to create it anyway you want. 

* Unlike Django,it does not enforce a specific project architecture. 
* It only provides minimal functionality. For example, if you want database integration, admin interface or migration tools, you can have those via flask extensions. 
* So when is it a good idea to use Flask? 
    - Doing something simple
    - want to implement own project architecture
    - need granular control over components in the project 

