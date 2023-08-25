---
title: Lists
layout: default
parent: Python Brief Intro
nav_order: 9
---
# Lists

You learned earlier that in addition to data types like `int` and `str`, Python has a number of data types that represent collections of things. One of the data types we looked at in this category is `list`.

We can have a list of integers. It might look like

```python
numbers = [2, 4, 8, 16]
```

We can just as easily have a list of strings. It might look like

```python
toRead = ['Walden', 'Broad Band', 'The Information', 'Surveillance Capitalism', 'Stamped from the Beginning'] 
```

Notice that the commas separating the list items must fall *outside* the quotation marks. The quotation marks, by the way, can be single or double; however, for any given list item, as we've already seen, the quotation marks must match. Entering `"Walden'` as a list item will result in an error when we go to do anything with our list. By now, you may have surmised correctly that if a list item contains an apostrophe, you'll want either to use double quotation marks to surround the item itself or escape the apostrophe:

```python
toRead = ["Thoreau's World and Ours", 'America\'s War']
```
To avoid confusing yourself, you'll probably do best to adopt a consistent solution for handling quotation marks within list items&mdash;at least within a given project&mdash;rather than mixing solutions as above.

## Print a list

Navigate in your terminal to `~/critical-digital` or wherever you're storing your practice files for this course and create a new file there, `loop.py`. Copy and paste the code below into the file.

```python
toRead = ['Walden', 'Broad Band', 'The Information', 'Surveillance Capitalism', 'Stamped from the Beginning']

print(toRead)
```

Save the file.

After confirming that you're in the same directory, in your terminal, as the file `loop.py`, type `python loop.py` at the *terminal* prompt (don't start a Python session). You should see the list printed to your terminal.

Now go back into the file and comment out the second line. Putting a hashtag (`#`) at the beginning of a line of Python code will cause the line to be treated as a comment rather than as code.

```python
toRead = ['Walden', 'Broad Band', 'The Information', 'Surveillance Capitalism', 'Stamped from the Beginning']

# print(toRead)
```

Add four new lines directly below the one you've commented out:

```python
toRead = ['Walden', 'Broad Band', 'The Information', 'Surveillance Capitalism', 'Stamped from the Beginning']

# print(toRead)

# The len() function will return the number of elements in our list
list_length = len(toRead) 

# Print the value of variable list_length, which we set to store the value of len(toRead)
print(list_length) 
```

Save the file.

Two of our four new lines use `#` not to "comment out" code but to provide genuine commentary on our code. As with HTML and CSS, adding comments like this to your code&mdash;especially as your code grows more complex&mdash;will help you remember what different chunks of your code are intended to accomplish, and will prove invaluable to others with whom you choose to share that code later on.

If you didn't really pay attention to the comments you pasted into `loop.py` just now, go back and read them carefully. Ask yourself what output you're likely to get when you run this new bit of code.

Ready? Let's do it. At the terminal prompt, type

```zsh
python loop.py
```
Here's what the result should look like:

```zsh
python loop.py
5
```
`5` is the value `list_length`, the variable we set to store the value of `len(toRead)`. Our list contains 5 elements.

## Using the list index

Python lists are **ordered**. They're also **indexed**, making it possible for us to access that order.

```zsh
>>> toRead = ['Walden', 'Broad Band', 'The Information', 'Surveillance Capitalism', 'Stamped from the Beginning']
>>> toRead[0]
'Walden'
>>> toRead[1]
'Broad Band'
```
We use square brackets to access a list item by its index, as in the example above. Notice that the *first* item's index is `[0]` and the *second* item's index is `[1]`. Until you get used to it, the fact that counting in Python begins at zero can be a little confusing.

We can access the last item in the list with index `[-1]`, the second-to-last with index `[-2]`, and so on.

```zsh
>>> toRead = ['Walden', 'Broad Band', 'The Information', 'Surveillance Capitalism', 'Stamped from the Beginning']
>>> toRead[-1]
'Stamped from the Beginning'
>>> toRead[-2]
'Surveillance Capitalism'
>>> toRead[-5]
'Walden'
```
## Slicing

We can access a portion of a list by **slicing**. 

```zsh
>>> toRead = ['Walden', 'Broad Band', 'The Information', 'Surveillance Capitalism', 'Stamped from the Beginning']
>>> toRead[0:2]
['Walden', 'Broad Band']
```

In the example above, `toRead[0:2]` returns a list containing the first and second items in our original list. Like indexing, the way Python represents a slice takes a little getting used to. The slice begins with the first-referenced item and ends with the item *before* the last-referenced item. Slicing on `[0:2]` returns list items `[0]` and `[1]` only. It does not return item `[2]`.

If we want to access the part of the list from the second item to the last, we can do so with 

```python
toRead[2:5]
```
But we can also do so more economically with

```python
toRead[2:]
```

Correspondingly, we can access all items up until the fourth with 

```python
toRead[:4]
```
This will return the items indexed `[0]`, `[1]`, `[2]`, and `[3]`.

Play around with slicing at the Python prompt until you get the hang of it. Slicing may not seem to do that much for you when you're dealing with a short list like the one in our example, but it doesn't take too much imagination to see how useful it can be in manipulating much longer lists.