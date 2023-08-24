---
title: Types and Functions
layout: default
parent: Python Brief Intro
nav_order: 4
---
# Types and Functions

## Types

Computer programs like Python sort data into a variety of **types**. Types recognized by Python include **integer** (int), **float** (float), **string** (str), **Boolean** (bool), and **list** (list)

Enter the following commands at the Python prompt as you see them below. When you do, you should also Python evaluate the commands and return the results that you see below inside the pointy brackets (`<>`).

```zsh
>>> type(1)
<class 'int'>

>>> type(1.0)
<class 'float'>

>>> type("Hello there!")
<class 'str'>

>>> type(True)
<class 'bool'>

>>> type([1, 2, 3])
<class 'list'>
```

**Integers** (like `1` above) are whole numbers.

**Floats** (like `1.0` above) are numbers with decimals. Python treats them a bit differently from integers.

**Strings** (like `"Hello there!"` above) are arbitrary sets of characters, such as letters and numbers. You can think of them as a way to store text.

**Booleans**: (like `True` above) is a fancy term for values representing "true" and "false," or "truthiness" and "falsiness." In Python, Boolean values are always capitalized: `True` and `False`.

**Lists**: (like `[1, 2, 3]` above) are ordered collections of values. You can put any of the other types in a list. For example, `["hello", "goodbye", "see ya later"]` is also a valid list.

For now, don't worry about remembering the names for these types. They'll become familiar as you begin to work with them.

One thing to keep in mind, though, is that, in commands like those above, the fact that you type a *number* on your keyboard doesn't mean that the data type that number represents is an integer or float. For example, consider the following two commands and the output Python prints to the screen when it evaluates them:

```zsh
>>> type(1)
<class 'int'>

>>> type("1")
<class 'str'>
```
In some situations, you may want Python to understand a number you strike on your keyboard as a numerical value, such as an integer, but in other situations&mdash;for example, when entering a zip code as part of a postal address&mdash;you may want Python to understand it as a string. Surrounding text and number values with quotation marks tells Python to treat them as strings.

## Functions

`type()` is a Python function. We'll have more to say about functions down the road, but for now, here are a few ways to think about functions in Python:

1. A way of doing something in Python.
2. A way of saving some code for reuse.
3. A way of taking an input, transforming that input, and returning an output. The input goes in the parentheses `()`.

The third way in this list is a good description of what you did above using the `type()` function. With each command, you **passed** a different value to the function by putting the value inside the parentheses. The function operated on that value and provided you with ouput.

When you use functions in Python, you always include the parentheses, even if there is no value to be passed inside them. This is why you exit Python in the terminal with `exit()`, which is a Python function.