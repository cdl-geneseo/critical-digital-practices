---
title: More About Functions
layout: default
parent: Python Brief Intro
nav_order: 8
---
# More About Functions

Broadly, we can define a Python **function** as *a block of reusable code that performs a specific task*. Python functions are an essential tool for saving time, preventing errors, and keeping your code concise and readable.

Often, a function takes an **input**, transforms it in some way, and returns an **output**. Let's consider a couple of analogies:

- The [penny press](https://en.wikipedia.org/wiki/Elongated_coin) is a tourist attraction that accepts a penny (the input), flattens and embosses the penny (the transformation), and spits out an elongated coin with a new design, perhaps an image of the Statue of Liberty (the output). 
- In algebra, the function `f(x) = x + 1` means that given an input `x`, the function will return `x + 1`. For example, if we substitute `2` for `x`, our function will read `f(2) = 2 + 1`, or `f(2) = 3`. In this case, our input is `2`, the transformation is to add `1`, and the output is `3`. 

Python functions work in much the same way.

## Write a function

Create a new plain-text file inside `~/critical-digital` (or wherever you're storing your practice files for this course). Before you go any further, save it as `myfunctions.py`.

Now let's write a Python function that prints the output from our alegebraic equation `f(x) = x + 1` above:

```python
def add_one(x):
    print(x + 1)
```

Let's break down this little block of code. Functions begin with the Python **keyword** `def`. (Keywords are "reserved" in Python for certain specific purposes and aren't available to be used as variable names, function names, or identifiers of other kind).

We follow `def` with our chosen function name. The [naming conventions](https://www.python.org/dev/peps/pep-0008/#function-and-variable-names) for functions resemble those for variables: try to make them descriptive and simple; use hyphens, underscore, and mixed case to combine words; don't put spaces in them. Since our function will "add 1" to the integer we feed it as input, `add_one` is a reasonable name. The parentheses following `add_one` are kind of like the coin receptacle of the penny press. We want our function to accept one coin at a time (some functions can accept multiple inputs), and to alter our analogy a bit, we want it to accept more than just pennies: nickels, dimes, quarters, non-U.S. coins of all denominations&mdash;as long as they're coins. We need a placeholder for the input that will be fed to the function; we'll just name that placeholder `x`. This placeholder is what's known, in Python, as a **parameter**.

We end the first line with a colon (`:`), then indent the next line by one or more spaces (four is common). This next line describes what the function will "do." In our case, we want the function to `print` the result of adding `1` to our input, `x`. We're asking our function to do only one task. In reality, functions typically consist of a list of tasks that will be executed in sequence.

Omitting the colon and forgetting to indent are two common errors when you first start to write functions. Python will complain with `SyntaxError` if you do the first and `IndentationError` if you do the second.

After adding the function to `myfunctions.py`, save the file.

To **call** our function from the terminal, we'll need to **pass** an actual value to it. After all, it needs to know what `x` is before it can add `1` to `x`. Another way to say this is that when the function is called, the parameter `x` must be replaced by an **argument**, the actual input that we want the function to operate on. To recall our modified penny press analogy, the argument is the actual coin placed in the receptacle.

## Import the function

Let's now use our function in the REPL. To do that, first make sure that, in the terminal, you're in the same directory as `myfunctions.py`. Navigate there and use `ls` to be sure you can see `myfunctions.py` in the file list.

At the Python prompt, we begin by making our new function available for use in the current session. We do that by **importing** the function from the file that's storing it.

```zsh
>>> from myfunctions import add_one
```
Notice that we refer to `myfunctions` here without using the file extension `.py`

We can now start feeding arguments to the function as we would feed coins to the penny press:

```zsh
>>> add_one(4)
5
>>> add_one(12)
13
>>> 
```

## Write a second function

Despite the algebraic-sounding name, functions aren't just for mathematical operations. And they don't have to include any specific parameters. But they still need to include those placeholder parentheses, whether they're being defined or called.

Return to `myfunctions.py` and add another function below `add_one` (leaving an empty line between them), so that your whole `myfunctions.py` file looks like this:

```python
def add_one(x):
    print(x + 1)

def greet():
    print("Hello! How are you today?")
```

Save the file. 

Return to your terminal, and at the Python prompt type

```zsh
>>> from myfunctions import greet
>>> greet()
```
Did your terminal print the greeting you specified in your function definition? If not, debug and try again.

## Write a third function

Our last function will combine what we've learned about parameters with what we've learned about concatenation using `+`. While we can't concatenate integers and strings using `+`, we *can* concatenate strings and *variables that store strings*. 

Our `greet()` function is pretty generic. How about we fix that so that we can pass the function a new first name as a value each time we call it?

Return to your `myfunctions.py` file and add a new function, `greet_name()`:

```python
 def greet_name(x):
    print("Hello, " + x + "! How are you today?")
```
Save the file.

In the terminal, at the Python prompt, call your function, passing any name you like as argument to the function.

```zsh
>>> from myfunctions import greet_name
>>> greet_name("Jess")
```
*Notice that we need to put our argument in quotation marks*. Otherwise, Python will think that `Jess` in this case is a variable, and it will complain that the variable hasn't been defined.

Pass a few different names as argument to the function. By now you should be getting a sense of how functions can help you automate things you want to do in Python.