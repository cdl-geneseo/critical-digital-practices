---
title: Input
layout: default
parent: Python Brief Intro
nav_order: 12
---
# Input

It would be nice if we could write a program like `commencement.py`, in the previous section, and let the value of `major` be set, not by us, but by someone wondering where to go for their post-commencement celebration.

And in fact we can do just that.

Open a terminal window and start up a Python session by typing `python` at the terminal prompt. At the Python prompt, type the following, followed by `enter`:

```zsh
>>> greeting = input()
```
The REPL waits for you to supply some input. Type a greeting, like `Hey there!`, followed by `enter` again. You'll be returned to the Python prompt. Kind of seems like nothing happened, doesn't it? But something did happen. The `input()` function in Python takes user input and, in this case, sets the value of the variable `greeting` to that input.

At the waiting Python prompt, type `greeting`, then `enter`. Your whole session should look something like this.

```zsh
>>> greeting = input()
Hey there!
>>> greeting
'Hey there!'
```

Now let's put what we've learned to use in `commencement.py`. Be sure that, in the terminal, you're inside `~/critical-digital` (or wherever `commencement.py` is living in your file hierarchy).

Open `commencement.py` in VS Code or your preferred text editor, and change the top of the file so it looks like this:

```python
print("Let me help you figure out where to go for your post-commencement celebration. What's your major?")
major = input()
leadIn = "Your post-commencement celebration will be in "
```

Leave everything else the same. Save the file.

Confirm for yourself that, in the terminal, you're in the directory that contains `commencement.py`. At the terminal (not the Python) prompt, type the following, followed by `enter`

```zsh
python commencement.py
```

Your output should look like this:

```
python commencement.py
Let me help you figure out where to go for your post-commencement celebration. What's your major?

```
Type a major, followed by `enter`, and see what you get. It might be something like this:

```
python commencement.py
Let me help you figure out where to go for your post-commencement celebration. What's your major?
Biology
Your post-commencement celebration will be in the Integrated Sciences Center.
```

Do this a few times. (Remember: No need to keep typing `python commencement.py`. You can use the up arrow instead.) Put a different major in each time.

By now it may have occurred to you that some students using the interactive program we've built could end up in the wrong place for their post-commencement celebration. See what happens if you answer `Engl` or `business` when prompted for input.

Our program isn't a very good one for steering students to the right post-commencement celebration venue. ☹️ 

There are ways to improve it, but we won't go into them here.

Still, it's not a bad example for demonstrating how we can let the flow of a program be determined, in part, by external input.