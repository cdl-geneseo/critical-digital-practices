---
title: Interacting with Python
layout: default
parent: Python Brief Intro
nav_order: 3
---
# Interacting with Python

Let's begin by starting an "interactive session" session with Python. This means we'll be using Python in the terminal, where we can run little bits of code, experimenting and exploring what it can do, without having to save it. Think of this interactive space as a playground. Later on, we'll be working with Python in a more robust way, saving and executing Python scripts.

For now, though, let's start an interactive session with Python, which is accessed through the terminal.

Open your terminal, and at the prompt type:

```zsh
python
```

You should see something like this:

```zsh
Python 3.9.17 (main, Jul  5 2023, 16:05:27) 
[Clang 14.0.6 ] :: Anaconda, Inc. on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>> 
```
As you can see, Python has its own prompt, distinct from your terminal's default prompt. It looks like this:

```zsh
>>>
```

When you see the Python prompt, you know that you've entered an interactive session with Python, where you'll enter commands specific to Python rather than the shell commands you learned earlier in the [command line module]({{ site.url }}/mod-2/getting-started). When you first use Python in the terminal, it's easy to get confused about which kinds of command to enter. Keeping an eye on the prompt will help you remember whether to use shell commands or Python commands.  


## A little math

Let's try a little math at the Python prompt. In the example below, type the text that appears after the Python prompt (the `>>>`). This is your Python **input**. The line below is the **output** that is returned. This will be a standard convention when giving examples using the Python prompt.

```python
>>> 2 + 3
5

>>> 14 - 10
4

>>> 10 * 10
100

>>> 6 / 3
2

>>> 21 % 4
1

>>> 2 ** 8
256
```

The first four operations above are addition, subtraction, multiplication, and division, respectively. The next is modulo, or mod, which returns the remainder after division. The last command treats `8` as the exponent of `2`, raising 2 to the power of 8.

The spaces on either side of the operator symbols are optional but standard in writing Python. Python programmers prize the readability of their code, and including these spaces generally makes code more readable.

Note the way you interact with Python at the prompt. After entering an expression such as `2 + 3`, Python "evaluates" it to a simpler form, `5`, and then prints the answer to your screen. This process is known as **Read Eval Print Loop, or REPL**. Python **reads** your command, **evaluates** (or "runs") the command, **prints** the result, and lands you back at the prompt, completing a **loop**. The sequence of events when you issue shell commands in the terminal is also a REPL.

When using Python, the REPL is useful for quick tests and, later, can be used for exploring and debugging your programs interactively. Among other things, it's a great alternative to running a dedicated calculator program if you have to do a little bit of quick math and already have a terminal window open.

## Practice

Practice moving in and out of Python's interactive mode (aka the REPL). You can get out of Python by hitting `control` + `d` (or `control` + `z` or `control` + `z` + `enter` if you're on a computer running Windows) or by typing `exit()`. You can get back in the REPL by typing `python` at your ordinary terminal prompt. Remember that you're in the REPL when you see `>>>`, and you're in your shell when you see terminal's default prompt.

Notice those parentheses in the `exit()` command, by the way. You can exit a shell session in the terminal with just `exit`, but in Python you need to include those parentheses. The reason will become clear later on.