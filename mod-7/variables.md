---
title: Variables
layout: default
parent: Python Brief Intro
nav_order: 5
---
# Variables

A variable can be defined as **a symbol that refers to an object**, such as a string, integer, or list. 

Try the example commands, in the order shown below, at the Python prompt; you should get the same output shown below as well:

```zsh
>>> x = 5

>>> x
5

>>> x + 10
15

>>> y = "hello"

>>> y
'hello'

>>> y + " and goodbye"
'hello and goodbye'
```

As you can see from the examples above, the `=` sign lets you assign symbols like `x` and `y` to data. The variable stands to the left of the `=` sign. The data to the right of `=` is the **value** temporarily assigned to that variable. Just as it may be surprising to discover that the `1` on your keyboard can be used to represent either a numeric value or (when contained within quotation marks) a string, so it may seem unusual, especially for folks outside the STEM fields, to think of a word or other combination of letters as a "value." Python doesn't find either of these possibilities odd at all.

Note, however, that while you can use the `+` operator either to sum two numeric values or to join (aka **concatenate**) two strings, Python will not be happy if you try to use it to concatenate a numeric value *with* a string:

```zsh
>>> x = "The sum of 2 + 3 is"
>>> y = 5
>>> x + y

Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: can only concatenate str (not "int") to str
```
We'll have more to say about error messages like this in Python in a bit. It's easy to see, though, why Python would categorize this one as a `TypeError`; we're asking it to concatenate data of two different types, one of which is `str` and the other of which is `int`. 

Since we know that we can express a number in Python as a string value rather than a numeric one, the way to avoid this error should be clear:

```zsh
>>> x = "The sum of 2 + 3 is"
>>> y = " 5"
>>> x + y

'The sum of 2 + 3 is 5'
```

Notice that in our solution, the string that's being **stored** in the variable `y` begins with a space: 

```zsh
" 5"
```
In a string, space isn't the absence of a character; it's a character itself. Try the above solution in your own terminal, omitting the space (i.e., setting the value of `y` to `"5"`) and see what you get.

Variables can be set to data types other than `int` and `str`, including `list` and similar data types that group data elements together (aka **arrays**).

```zsh
>>> books = ['Gender Trouble', 'Cruising Utopia', 'Living a Feminist Life']

>>> books
['Gender Trouble', 'Cruising Utopia', 'Living a Feminist Life']

>>> type(books)
<class 'list'>
```
Variables can contain letters, numbers, and underscores, but not spaces. If you want to combine one or more words in a variable name, you can do so by using hyphens, underscores, or mixed case (e.g.,`my-books`, `my_books`, `myBooks`, but never `my books`). *A Python variable cannot begin with a number*. Try using `1Book` as a variable and Python will throw a `SyntaxError`.

The Python Foundation maintains a [style guide](https://peps.python.org/pep-0008/) that covers a wide range of best practices for writing Python code, including [naming conventions](https://www.python.org/dev/peps/pep-0008/#naming-conventions).
