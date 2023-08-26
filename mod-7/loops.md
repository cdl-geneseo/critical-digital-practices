---
title: Loops
layout: default
parent: Python Brief Intro
nav_order: 10
---
# Loops

In Python, a **loop** is a block of code that enables us to carry out a task or process repeatedly.

A **for loop** iterates over a series of items and performs the same action on each item in turn.

A **while loop** repeats a task or process until a specified condition has been met.

In both cases, once the loop has completed (because the action has been taken on each relevant item or the specified condition has been met), the program exits the loop and moves on to the next line of code. If the loop has been improperly written, and the program can't exit it to move on, the program becomes stuck in an **infinite loop**. 

In this section, we'll focus on the Python for loop.

## Write a for loop

Open a terminal window and start a Python session by typing `python` at the terminal prompt.

At the python prompt, let's once again create the list we worked with in the last section:

```zsh
>>> toRead = ['Walden', 'Broad Band', 'The Information', 'Surveillance Capitalism', 'Stamped from the Beginning']
```

Type the list as it appears above or copy-paste it; just be sure not to copy-paste the prompt itself.

Hitting `enter` should return you to the prompt:


```zsh
>>> toRead = ['Walden', 'Broad Band', 'The Information', 'Surveillance Capitalism', 'Stamped from the Beginning']
>>>
```

At the waiting prompt, type:

```zsh
for title in toRead:
    print("Remember to read " + title)
```

Hit `enter` *twice*. The first time you hit it, the REPL will simply return three dots. Your for loop won't run until you hit `enter` that second time. Altogether, your session should look like this:

```zsh
>>> toRead = ['Walden', 'Broad Band', 'The Information', 'Surveillance Capitalism', 'Stamped from the Beginning']
>>> for title in toRead:
...     print("Remember to read " + title)
... 
Remember to read Walden
Remember to read Broad Band
Remember to read The Information
Remember to read Surveillance Capitalism
Remember to read Stamped from the Beginning
>>> 
```
What did our for loop do? It iterated over the list of titles, prepending the string "Remember to read " to each item in the list.

Before we go further, let's look at the structure of our for loop. In the abstract, it's

```zsh
for <variable name> in <list name>:
    <do something>
```

Notice the similarity of structure to the way we used the keyword `def` in the last section. We have a statement followed by a colon, and underneath it some indented code. If either the colon or the indentation is missing, we'll get an error.

At this point, you may be asking yourself, "Why `title`? Is that a special Python word for referencing titles of books and other things? Not at all. It's just a word we selected to name a variable that can store the value of each item in the list in turn. Instead of `title`, we could have used `book`, `name`, `whatsit`, `thingy`, `item`, or `x`&mdash;to name just a few possibilities.

`title` is a good choice because it's meaningful and therefore helps our code make more sense to ourselves and others. It isn't necessarily better than `book` or `name`, but it's clearly more descriptive than `whatsit`, `thingy`, `item`, or `x`. A variable name is said to be "semantic" when it corresponds in a meaningful way to what it represents.

But wait, you may be thinking. We used `title` as a variable without first defining it. We didn't have to write a line that begins `title = `, followed by the value of title. Why didn't Python complain that the variable `title` hadn't been defined?

The answer is that this is how for loops work. When we follow the for loop syntax above, the variable is defined on the fly. It's understood to apply iteratively to the items in our list.

## Write another for loop

At the Python prompt, type:

```zsh
>>> for letter in "hello":
        print(letter)
```
Hit `enter` twice. The result should look like this:

```zsh
>>> for letter in "hello":
...     print(letter)
... 
h
e
l
l
o
>>>
```
Interesting! `"hello"` is not a list; it's a string. Yet we can iterate over the characters in a string, just as we can iterate over the elements in a list.

If you're suspecting this means that strings, like lists, are indexed, you're right! The fact that strings are indexed means that we can access characters in a string by their index (don't forget that space is a character, too), and that we can slice on a string. For example:

```zsh
>>> greeting = "Hello, there!"
>>> greeting[0]
'H'
>>> greeting[-1]
'!'
>>> 
```

With this knowledge, let's write one last for loop. If you haven't ended your Python session since creating the variable `toRead` above, it should still be stored. Test by typing it at the Python prompt and hitting `enter`:

```zsh
>>> toRead
```

If your list of titles isn't returned, define the variable again, or copy-paste the variable definition from above.

Now let's create our for loop:

```zsh
>>> for title in toRead:
        print(title[0])
```
What do you think this for loop will do? Let's try it. Hit `enter` twice. The result should be this:

```zsh
>>> for title in toRead:
...     print(title[0])
... 
W
B
T
S
S
>>> 
```
Our output is the first letter of each title.

## List comprehension

A handy variant of the loop syntax we've been using so far is called **list comprehension**. It's more compact and doesn't require code indentation. That doesn't make it better. The best syntax in any given situation will depend on what you're trying to accomplish. But it's worth a mention here.

Instead of 

```zsh
>>> for title in toRead:
...     print(title[0])
```
using list comprehension, we would write:

```zsh
>>> [title[0] for title in toRead]
```

Give it a try. Here's the result you should get:

```zsh
>>> [title[0] for title in toRead]
['W', 'B', 'T', 'S', 'S']
```
As you can see, we put our list comprehension code within list brackets `[]`. The REPL prints the output in the form of a list as well.