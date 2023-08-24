---
title: Scripts in Python
layout: default
parent: Python Brief Intro
nav_order: 6
---
# Scripts in Python

When we use Python in "interactive mode" in the REPL, our code isn't saved after we exit Python. To save code so that we can use it repeatedly, we need to store it in a file. From the terminal, we can then run the code stored in that file with a simple shell command.

This section of our brief introduction to Python requires that you either have Python installed on your machine or that you read up on how to import `.py` files into Google Colab. The examples below assume that you have a local installation of Python.

## Create a script file

Like files containing HTML, CSS, Markdown, CSV, etc., Python files are written in [plain text]({{ site.url }}/mod-3/understanding-text). You can write and store them in any plain-text editor; if you've been using VS Code for this course, it's your best bet. In your terminal, navigate to your `~/critical-digital` folder (or wherever else you've been storing practice files for this course) and save a new file there with the name `hello.py`. If you're using VS Code, you can type

```zsh
code hello.py
```
Just be sure you're in your practice folder when you do this. And remember that you'll want to save the file before taking the next step.

Add the following text to your `hello.py` file:

```python
print("Hello world!")
```
Save the file again.

## Run your script

For the next step, to repeat, you need to be sure you're in the same folder in your terminal where the file lives. You can check by typing

```zsh
ls
```

You should see your `hello.py` file listed. If you don't, use `pwd` to figure out where you are in your file hierarchy, and have a look at the top of your VS Code file to check that the path showing there is the same as the one you're seeing in the terminal. Move the file if necessary, or navigate in the terminal to the folder where `hello.py` is actually living. Again, make sure you've saved the file.

Now you can type the following at the terminal prompt. (Yes, the terminal prompt, not the `>>>` Python prompt we used in the previous section. If you're at the `>>>` prompt, perhaps because you were so eager that you started up Python without looking ahead to the next instruction, exit Python with `exit()`.)

```zsh
python hello.py
```
When you follow the `python` command with the name of a file containing a valid Python script, the terminal won't launch Python and put you into the Python REPL. What will happen, instead, is that Python will read the contents of the file and execute the code it finds there. It will print the contents to your terminal screen:

```zsh
$ python hello.py
Hello world!
```

Congratulations&mdash;you've written and executed your first Python script. The process should have seemed at least a little familiar if you remembered the [shell script we wrote earlier for creating a daily journal file in Markdown]({{ site.url }}/mod-3/keep-a-daily-journal#automation-step-1-write-the-script). That script, too, lived in its own file, `journal.sh`. When you ran your journal shell script in the terminal, each command in the script was executed in the order it appeared in your file. Python scripts operate the same way.

## Vary your script with a variable

Now let's make a small change to `hello.py`, taking advantage of what you learned above about variables. Open the file and edit it to read as follows:

```zsh
greeting = "Hello world!"
print(greeting)
```

Run the script again. You can save yourself the trouble of re-typing `python hello.py` again by using a [trick covered earlier, in the command line module]({{ site.url }}/mod-2/creating-files-and-folders#time-saver-up-arrow): hitting the up arrow (&#x25b2;) will put your most recent command back at the prompt. (You can also *execute* the previous command directly by typing `!!` at the prompt.)

Notice that in the REPL, after we set the variable `greeting`, we can just type `greeting` and the REPL will return its value, `'Hello world!'`, but that our script must contain the command `print(greeting)` for `Hello world!` to appear in our terminal.