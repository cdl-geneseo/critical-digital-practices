---
title: Conditionals
layout: default
parent: Python Brief Intro
nav_order: 11
---
# Conditionals

Earlier, you learned that there's a [data type in Python called a **Boolean**]({{ site.url }}/mod-7/types.md).

Open a terminal window and start a Python session by typing `python` at the terminal prompt. Once in the Python REPL, type the following and hit `enter`:

```zsh
>>> sum = 5 + 2
```

At the next prompt type the following and hit `enter` again:

```zsh
>>> sum == 7
```
The **comparison operator** `==` tells Python to evaluate whether the value on left is identical to the value on the right. If it is, Boolean `True` is returned. If it isn't, `False` is returned.

Type the following and hit `return`. See what you get.

```zsh
>>> sum == 8
```

It's easy to confuse the comparison operator `==` with the **assignment operator** `=`, which is used, as we've had many occasions to see by now, to assign a value to a variable. 

Give the "greater than or equal to" and "less than or equal to" comparison operators a try. You should get results like the following:

```zsh
>>> sum == 8
False
>>> sum >= 5
True
>>> sum <= 9
True
>>> sum >= 8
False
>>> sum <= 6
False
>>> 
```

Comparison operators (which also include "not equal to" \[`!=`\], "greater than" \[`>`\], and "less than" \[`<`\]) make it possible for us to write **conditional statements** that control the **flow** of our program, causing the program to move forward in one way if a stated condition is true and another way if the stated condition is false.

## Flow control

Here's a simple example:

```zsh
>>> field = "Media Studies"

>>> if field == "Media Studies":
        print("Grammophone, Film, Typewriter")
```

As you can see from the example, the comparison operator `==` doesn't just compare numerical values. After we set the value of the variable `field` in the first line to the string `"Media Studies"`, we can write an `if` statement, followed by a colon (`:`), followed by an indented code block containing a function (`print()`) that will be called only **if** the condition in the `if` statement (`field == "Media Studies`) evaluates to `True`.

If we run this program, we won't see the word `True` appear anywhere. But if the conditional statement evaluates to `True`, we'll get output (the string that's the argument of `print()`). And if it evaluates to `False`, we'll get no ouput at all.

Test this for yourself by first running the program above in the REPL, then running it again, with a different value for the `field` variable. For example,

```zsh
>>> field = "Geology"
>>> if field == "Media Studies":
        print("Grammophone, Film, Typewriter")
```

Now let's give our program a path it can follow, other than simply returning no output, if the condition in the `if` statement is evaluated to `False`. The example below shows how our code will look in the REPL, including the ellipses (`...`) printed when we hit return. If you were writing this program in an external file, you wouldn't write the ellipses.

```zsh
>>> field = "Geology"
>>> if field == "Media Studies":
...     print("Grammophone, Film, Typewriter")
... else:
...     print("Wait - there are fields that aren't Media Studies? Who knew.")
```
This example, by the way, should clarify *why* the REPL prints those ellipses. The ellipses indicate that the REPL is waiting to see if we have anything more to add to our program. After a statement followed by a colon, the REPL is waiting for our indented code block. If the program ran as soon as we hit `enter` after that code block (the first `print()` function above), we wouldn't be able to include our `else` statement.

Notice that our `else` statement, like our `if` statement, must be followed by a colon, and that the code block beneath it must be indented.

## Elif

Pairing an `if` statement with an `else` statement allows our program to flow in two different directions, depending on the conditions we set. What if we want more options than two?

That's where the `elif` statement, short for "else if", comes in. We can set an unlimited number of alternative conditions following our initial `if` statement, each handling a different circumstance, before ending with a final `else` statement to handle any circumstance not handled by the other statements. Depending on the circumstance in each case, we can have our program do something different.

Play around with the following program, changing the value of `field`, to see the different types of output you'll get. Try setting the value of `major` in the second line to some of the different values in the `elif` statements, and also to a variety of majors not mentioned in the `elif` statements, like Psychology.

This exercise will be less tedious if, instead of writing the program in the REPL, you put it in an external file, say `orientation.py`, and run it from the terminal prompt (not the Python prompt) with

```zsh
python orientation.py
```
Remember to save `orientation.py` each time you change it, before re-running the program.

The program:

```python
leadIn = "Your post-graduation celebration will be in "
major = "English"

if major == "English":
    print(leadIn + "Welles Hall.")
elif major == "Biology":
    print(leadIn + "the Integrated Sciences Center.")
elif major == "Sociology":
    print(leadIn + "Bailey Hall.")
elif major == "Art History":
    print(leadIn + "Brodie Hall.")
elif major == "Education":
    print(leadIn + "South Hall Third Floor.")
elif major == "Business":
    print(leadIn + "South Hall Ground Floor.")
else:
    print(leadIn + "the College Union Ballroom.")
```