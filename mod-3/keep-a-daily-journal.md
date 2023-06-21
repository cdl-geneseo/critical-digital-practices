---
title: Keep a Daily Journal in Markdown
layout: default
parent: What is Text?
nav_order: 6
---

# Keep a Daily Journal in Markdown

Let's put together what you've learned so far about the command line and Markdown to set up a workflow for keeping a daily Markdown journal.

## Why do this?

Besides giving you an opportunity to use your new skills at the command line and take advantage of Markdown's simplicity, flexibility, and interoperability, creating this workflow and keeping the journal will give you a way to document your learning in this course&mdash;and beyond.

## Step 1: Write a shell script to create a new daily file

A **shell script** is a series of shell commands stored in a file that will run in succession when you execute it.

We're going to write a very short script to create a daily journal document. You only have to write this script once; after that, you just execute the script with a simple terminal command&mdash;or from your GUI&mdash;whenever you're ready to do some journaling. Every time you run the script, you'll create a fresh plain-text document with the current date (yyyy-mm-dd) and time (hh-mm) right in the file name, and the Markdown extension (`.md`) at the file name's end. 

Over time, you may want to write other scripts, so let's begin by creating a folder to hold these. Open a terminal window and use `pwd` to make sure you're in your home folder. If you're not, go there with

```zsh
cd ~
```
Next, create a folder for your scripts. You can call it anything you want. Maybe `scripts` is a good name?

```zsh
mkdir scripts
```
Descend into your new `scripts` folder.

```zsh
cd scripts
```
To create your file, you have a few options. One option is to use `touch`:

```zsh
touch journal.sh
```
However, if you followed the instructions carefully for [installing VS Code](/critical-digital-practices/mod-3/text-editors#visual-studio-code), you should be able to create the file and open it in VS Code with a single command:

```zsh
code journal.sh
```
Remember that if you create and open the file using `code`, the file will have only a temporary existence until you save it. If you close the VS Code tab for the file without saving, you'll lose the file contents, and you won't find the file in your file system.

If you're not able to use the `code` command, you can either revisit the instructions to get VS Code's command-line tools in your PATH, or you can go to your GUI, right-click on the file name, and tell the Finder or File Explorer to open the file in VS Code.

Other options, of course, include opening the file in any other plain-text editor and opening it in your terminal using, say, Vim or Nano.

Here's what you should put in the file:

```zsh
#!/bin/bash

# A script to create and open a daily
# journal file.

# create path to new file and store it in a variable
filename=$HOME/journal/journal_$( date '+%Y-%m-%d_%H-%M' ).md

# add title line to top of file
echo "JOURNAL FOR $( date '+%Y-%m-%d' )" >> $filename

# open file in VS Code
code $filename
```
Save the file. 

Before going on to the next step, let's take a moment to review what's in the file you created. We'll go through it line-by-line.

### She-bang

```zsh
#!/bin/bash
```
The first line combines an exclamation point and a pound sign to form what's known as a [shebang](https://www.computerhope.com/jargon/s/shebang.htm). It's followed by the path to your Bash installation. This first line tells your operating system where to find the program that will execute your script.

### Comments

```zsh
# A script to create and open a daily
# journal file.
```
The next two lines, each beginning with `#`, are comments. Comments are ignored when the script is processed; their purpose is to remind you, or someone reading your script, what the script as a whole and various executable lines within it are designed to do. You can remove or edit these comments as you see fit. Just keep in mind that every new line of commentary requires a new `#` at the beginning. VS Code's syntax highlighting is your friend here, helping you to clearly distinguish comments from code in your file.

### Variable = file path
```zsh
# create path to new file and store it in a variable
filename=$HOME/journal/journal_$( date '+%Y-%m-%d_%H-%M' ).md
```

The first line of executable code in the file creates a **variable** named `filename`, setting the variable equal to the **value** of the path where you want your script to create a new file. We create variables by making up names for them. When we want to make use of the variable's value, we put a `$` directly in front of the name. `HOME` is a variable that's typically already set in your operating system; its value is the path to your home folder. If you wanted to, you could swap out this variable for the actual path to your home folder: For example, `/Users/c/your-username` in Git Bash.

{: .tip}
Need a refresher on home folder paths in Mac/Git Bash/Ubuntu? Look back at [A Sense of Where You Are](/critical-digital-practices/mod-2/where-you-are).

The last part of the path will create a file name that begins with `journal_`, is followed by the current date and time (pulled from your system's clock) and ends with the `.md` file extension.

### Add a title line

```zsh
# add title line to top of file
echo "JOURNAL FOR $( date '+%Y-%m-%d' )" >> $filename
```

The next line of code creates a title line for your file by echoing some words and the date (no hours and minutes this time) and writing them to the file. Earlier, we used a single right-angle bracket (`>`) as a "redirect" to write contents to a new file. The double right-angle brackets in our script (`>>`) **append** content to an existing file. Instead of writing out the whole path to that existing file again, we reference it using the variable we created earlier.

Don't want a title line in your file? You can comment out this command or simply remove it from your script. 

### Open the file in VS Code to start journaling

```zsh
# open file in VS Code
code $filename
```
The final line of code opens the file in VS Code, where it's ready and waiting for you to start journaling. If you don't yet have VS Code's command line tools installed, you should comment this line out until you do. Just add a `#` to the beginning of the line. To open the file without using the `code` command, just go to it in your GUI. You may have to right-click on it and tell it to open in VS Code rather than TextEdit or Notepad.

## Step 2: Make your script executable, then run it

We saw in [Some Plain-Text File Formats](/critical-digital-practices/mod-3/kinds-of-text) that files ending in `.sh` are **excecutable** plain-text files. You can read and edit them like other plain-text files, but you can also ask your computer to **run** the code that's inside them. How?

In [Getting More Information About Files and Folders](/critical-digital-practices/mod-2/getting-more-information), we saw that a "long" display of a folder's contents will show us the permissions associated with each file in the folder. The `r` in these permissions stands for **read**, the `w` for **write**, and the `x` for **execute**. In order to run, an executable file must contain valid executable code and also have that `x` in its permissions.

To make your `journal.sh` file executable in macOS or Ubuntu for Windows, make sure you're in your `~/scripts` folder and type the following:

```zsh
chmod u+x journal.sh
```
The `chmod` command will add an `x` to your permissions as user. You can verify this by typing

```zsh
ls -l journal.sh
```
The first three letters in the permissions column should be `rwx`, indicating that you can execute the code in the file.

Things are a little different in Git Bash, where you can't actually change file permissions using `chmod`. However, that first line in your script&mdash;the one with the she-bang&mdash;should have made the file executable already. Again, you can verify with `ls -l`.

Whether in macOS, Ubuntu, or Git Bash, you can run the code in your executable file by navigating to `~/scripts` using `cd` and typing the following

```zsh
./journal.sh
```
After a few seconds, your new journal file should open in VS Code and be ready for you to start journaling. To repeat, if you don't have VS Code's command line tools installed, you can just navigate to the new file  (it will be waiting for you in your `~/journal` folder)  and open it from there.

## Step 3: Journal away in Markdown

