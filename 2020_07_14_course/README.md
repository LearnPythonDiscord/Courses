# 2020 07 14 Weekly Course

Thank you for taking the time to read this write-up on the Python introductory course. This class will go over the basics of setting up and using Python, as well as a small Hello World application to get you started.

## Contents

- [2020 07 14 Weekly Course](#2020-07-14-weekly-course)
  - [Contents](#contents)
  - [Setting up Python](#setting-up-python)
  - [Installing an Editor](#installing-an-editor)
    - [VSCode Extensions](#vscode-extensions)
  - [Downloading Packages](#downloading-packages)
    - [Useful Packages](#useful-packages)
  - [Hello World Application](#hello-world-application)
    - [Data Types](#data-types)
      - [Dictionaries](#dictionaries)
      - [Lists](#lists)
    - [Functions](#functions)
      - [Lambdas](#lambdas)

## Setting up Python

Depending on your OS you will want to install the latest version of Python available from the official [Download Page](https://www.python.org/downloads/). The course will be using Python 3.8 or newer, and while most features work in previous versions it's best to be up-to-date with all the latest updates and security patches.

## Installing an Editor

For beginners we recommend using Microsoft's open-source [VSCode editor](https://code.visualstudio.com/) with a couple of extensions. Other options include [PyCharm Community](https://www.jetbrains.com/pycharm/download/) for more advanced users and [Atom](https://atom.io/) as a lightweight alternative.

### VSCode Extensions

Some extensions we recommend for Python development with VSCode include:

 - [Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python) by Microsoft: Enables Python language support in VSCode and test tools.
 - [Kite](https://marketplace.visualstudio.com/items?itemName=kiteco.kite): A coding assistant that aids with autocompletion and shows docstrings.
 - [Wolf](https://marketplace.visualstudio.com/items?itemName=traBpUkciP.wolf): Live Python scratchpad
 - [Sort Lines](https://tyriar.gallerycdn.vsassets.io/extensions/tyriar/sort-lines/1.9.0/1573941482699/Microsoft.VisualStudio.Services.Icons.Small): Automatically sort lines of long dictionary keys.
 - [Guides](https://marketplace.visualstudio.com/items?itemName=spywhere.guides): Adds extra indentation guides.

## Downloading Packages

Python comes with a built-in package manager called PIP. It lets you install packages directly via the command-line using either GitHub packages or official ones from PyPi.

Packages add a lot of advanced functionalities that would be cumbersome to setup on your own. Some popular packages include `urllib3`, `numpy` and `setuptools`.

To install a package available on PyPi via PIP, you need to use the following command:

```bash
$ pip install [packagename]
```

**Note:** On some systems the PIP for Python 3 might be available under `pip3`, so if packages aren't available after using `pip`, try `pip3`.

### Useful Packages

Depending on what you might want to do with Python, there are a couple packages that will come in handy and aid you with those tasks.

A combination of [Selenium](https://pypi.org/project/selenium/), [BeautifulSoup4](https://pypi.org/project/beautifulsoup4/) and [URLLib3](https://pypistats.org/packages/urllib3) will allow you to open up webpages, read their contents and go over the elements in an organized manner. All the packages are available on PyPi and have good user documentations.

[NumPy](https://pypi.org/project/numpy/) is a very popular library for performing large numerical calculations and tasks and is available on PyPi with a strong documentation as well.

[Dicord.py](https://pypi.org/project/discord.py/), [PRAW](https://pypi.org/project/praw/) and [aPRAW](https://pypi.org/project/aPRAW/) let you write bots for Reddit or Discord respectively, which becomes especially fun when combining aPRAW with Discord.py to make bots that bring those two platforms together.

## Hello World Application

To begin we'll start by creating a small Hello World application that makes use of the `print()` function, as well as some basic data types which will be explained in further detail below.

Before you can create a Python file in VSCode, you want to prepare a folder in which all the files will be stored and then open that folder in VSCode by right-clicking and selecting "Open in Code" or using the command line tools and typing:

```bash
$ cd path/to/project
$ code .
```

Once in VSCode you can right-click in the file browser and select "New File". The filename should use the `.py` extension, so something like `main.py` meets those requirements.

Now that we have created a Python file, it's time to write some actual code!

~~Start by writing `print("Hello world!")`.~~

No, no, no. We aren't doing that here again. While this is a Hello World application, let's see about stringing together those words instead of just printing them and using some built-in functions.

Go ahead and copy this into your script and let's look over it after running it for the first time.

```python
hello_str = "Hello"
world_str = "World"
exclamation = "!"

print_str = f"{hello_str} {world_str}{exclamation}"

print(print_str)
>>> "Hello World!"
```

**So what's going on here?** Well, like any programming language you can declare so-called variables. These are essentially names we give to values in our code, to be able to (re)use them later and even perform calculations or changes to them!

In this example we're using Python's built-in f-strings as well as the `print()` function. Using f-strings we can concatenate the previously declared and assigned `hello_str`, `world_str` and `exclamation` variables into one by the name of `print_str` and then output the result to the console.

### Data Types

The previous example only had us using strings, but what about storing numbers or multiple values in one variable? Types exist for those too!

```python
integer_val = 1
float_val = 1.5
string_val = "test"
bool_val = True
```

Python allows us to declare variables regardless of type the same way. Simply type `val_name = {value}` and Python will assign the given value to that name. Integers and floats, while similar, have the distinction that floats can handle decimal positions, while integers must be full numbers.

Booleans are very important variable types in programming languages. They let us store simple `True` or `False` values which can later be used as conditionals in our logic. More on that later.

#### Dictionaries

Dictionaries are a more advanced built-in type in Python. While the previously mentioned types only store on distinct value, dictionaries store key-value pairs. They're declared by doing the following:

```python
dict_val = {
  "string_val": "test",
  "int_val": 1,
  "float_val": 1.5,
  "bool_val": True
}
```

Accessing values in dictionaries happens a little differently, since they're all encapsulated within that dictionary. i.e. to read the value of `string_val` you'd type the following: `dict_val["string_val"]` (Note the quotes.)

#### Lists

Lists do exactly what the name suggests. They let you store multiple variables in them, and access them via *indices* later on. Indices begin from 0 - being the first element, and progress upwards. Let's take a look at an example:

```python
my_list = [1, 1.5, "test", True]

print(my_list[0])
>>> 1

print(my_list[1])
>>> 1.5

print(my_list[2])
>>> "test"

print(my_list[3])
>>> True
```

For more information on types take a look at W3Schools introduction to [Python Data Types](https://www.w3schools.com/python/python_datatypes.asp).

### Functions

So far our code has simply been executing the logic from top to bottom. This is fine for simple use-cases, but sometimes you might want to reuse bits of code. This is where functions come into play:

```python
def print_something() -> None:
  print("Something!")
  >>> "Something!"

print_something()

def multiply(x: int, y: int) -> int:
  return x * y

result = multiply(5, 2)
print(result)
>>> 10
```

In the above code we defined two functions. One without any arguments called `print_something()` that does exactly what the name suggests when used. It prints "Something!" to the console.

`multiply()` is a bit more advanced as it utilizes return values as well as arguments. Within the brackets following the function name we can specify parameters and their type by using the format `<name>: <type>`. Those parameters can be used within the function by their name.

The `return` statement allows functions to return a result after they've been executed. This is useful when we don't want to perform a visible action, but instead return a new result based on the given arguments.

If a function has a return value, we can assign this return value or use it directly after calling it. Calling a function is synonymous to executing it, and is done in Python by writing `func_name()`.

#### Lambdas

Lambdas are a type of anonymous functions. Writing that extra line of code for the `multiply()` function above was a little unnecessary now that Python has lambdas. So it can be shortened to the following:

```python
multiply = lambda x, y: x * y

print(multiply(5, 2))
>>> 10
```

Lambdas automatically return the value they're assigned to, so the `return` keyword can be omitted.
