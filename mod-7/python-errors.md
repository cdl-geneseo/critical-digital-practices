---
title: Python Errors
layout: default
parent: Python Brief Intro
nav_order: 7
---
# Python Errors

It's common to get error messages when working in Python. These messages can be a little intimidating at first, but once you understand how they work, you'll find them very helpful.

Many of the errors you'll make in Python fall into two categories: **syntax errors** and **traceback errors**. 

## Syntax errors

When you ask Python to run a program or execute a line in the REPL, it will first check to see if the program is **valid** Python code&mdash;that is, if the code properly follows the grammar of Python, its **syntax**. If it doesn't, before the program even runs, you'll see a syntax error message printed out to the screen.

In the example below, the syntax error is a common one—mismatched single and double quotes, which is not allowed in Python. You can replicate the error for yourself by opening the REPL (type `python` in the command line) and entering the line after the `>>>` prompt.

```python
>>> print('This string has mismatched quotes. But Python will help us figure out this bug.")
  File "<stdin>", line 1
    print('This string has mismatched quotes. But Python will help us figure out this bug.")
                                                                                          ^
SyntaxError: EOL while scanning string literal
```

Note the caret (`^`) underneath the mismatched quote, helpfully pointing out where the error lies. If this error happened in the course of running a script, Python would tell us the filename and the number of the line where the error occurs.

## Traceback errors

Traceback errors occur during the execution of a Python program when the program finds itself in an untenable state and must stop. Traceback errors are often logical inconsistencies in a program that is syntactically valid Python code. A common traceback error is referring to a variable that hasn't been defined, as below.

```zsh
>>> print(not_yet_a_variable)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'not_yet_a_variable' is not defined
```
Traceback error messages try to tell you a bit about what happened in the program that caused the problem, including the category of error, such as `NameError` or `TypeError`.

## Debugging

Debugging is simply the (not always simple) process of fixing problems with a program. It takes patience. Here are some common strategies for debugging a program when first learning Python:

- If the error is a **syntax** error:
    - Look at where the caret is pointing.
    - Pay attention to syntax features such as quotes, parentheses, and indentation.
    - Consider reading the program, or the offending line, backward. It's surprising, but this often helps to detect the issue.
- If the error is a **traceback** error:
    - First, look at the line where the error occured, then consider the general category of error. What could have gone wrong?
    - If the error is a name error (NameError), check your spelling.
    - Try copying the last line of the error and pasting it into a search engine such as Google or Duck Duck Go. You'll often find a quick solution this way.
- If you changed the program and expect a different output, but are getting old output, you may not have saved the file. Go back and make sure the file has been correctly saved.