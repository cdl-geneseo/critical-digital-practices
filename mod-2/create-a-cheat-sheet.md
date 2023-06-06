---
title: Create a Cheat Sheet
layout: default
parent: The Command Line
nav_order: 8
---
# Create a Cheat Sheet

Let's create a text file that we can use as a cheat sheet. You can use it to keep track of all the awesome commands you're learning.

## Echo

Instead of creating an empty file like we did with `touch`, let's try creating a file with some text in it. But first, let's learn a new command: `echo`.

```zsh
$ echo "Hello from the command line"
Hello from the command line
```

## Redirect (`>`)

By default, the echo command just prints out the text we give it. Let's use it to create a file with some text in it:

```zsh
$ echo "This is my cheat sheet" > cheat-sheet.txt
```

Now let's check the contents of the directory:

```zsh
$ pwd
/Users/your-username/projects
$ ls
cheat-sheet.txt
```

OK, so the file has been created. But what was the `>` in the command we used? On the command line, a `>` is known as a "redirect." It takes the output of a command and puts it in a file. Be careful, since it's possible to overwrite files with the `>` command.

If you want to add text to a file but _not_ overwrite it, you can use the `>>` command, known as the redirect and append command, instead. If there's already a file with text in it, this command can add text to the file _without_ destroying and recreating it.

## Cat

Let's check if there's any text in `cheat-sheet.txt`.

```zsh
$ cat cheat-sheet.txt
This is my cheat sheet
```

As you can see, the `cat` command prints the contents of a file to the screen. `cat` stands for "concatenate," because it can link strings of characters or files together from end to end.

## A Note on File Naming

Your cheat sheet is titled `cheat-sheet.txt` instead of `cheat sheet.txt` for a reason. Can you guess why?

Try to make a file titled `cheat sheet.txt` and observe what happens.

Now imagine you're attempting to open a very important data file using the command line that is titled `cheat sheet.txt`

For your digital best practices, we recommend making sure that file names contain no spaces—you can use creative capitalization, dashes, or underscores instead. Just keep in mind that the macOS and Unix file systems are usually pre-configured as cAsE-pReSeRvInG, which means that capitalization matters when you type commands to navigate between or do things to directories and files. You may also want to avoid using periods in your file names, as they sometimes can prompt you to confuse them with system files or file extensions (e.g., the full name of a PDF file is usually `file.pdf`).

## Using a Text Editor

The challenge for this section will be using a text editor, specifically Visual Studio Code ([install guide here](https://github.com/DHRI-Curriculum/install/blob/v2.0/guides/visual-studio-code.md)), to add some of the commands that we've learned to the newly created cheat sheet. Text editors are programs that allow you to edit plain text files, such as `.txt`, `.py` (Python scripts), and `.csv` (comma-separated values, also known as spreadsheet files). Remember not to use programs such as Microsoft Word to edit text files, since they add invisible characters that can cause problems.

## Challenge

You _could_ use the GUI to open your Visual Studio Code text editor—from your programs menu, via Finder or Applications or Launchpad in macOS, or via the Windows button in Windows—and then click `File` and then `Open` from the drop-down menu and navigate to your Desktop folder and click to open the `cheat-sheet.txt` file.

_Or_, you can open that specific `cheat-sheet.txt` file in the Visual Studio Code text editor directly from the command line! Let's try that by using the `code` command followed by the name of your file in the command line. (Remember, the command `code` prompts your computer to open Visual Code.)

Once you've got your cheat sheet open in the Visual Studio Code text editor, type to add the commands we've learned so far to the file. Include descriptions about what each command does. Remember, this cheat sheet is for you. Write descriptions that make sense to you or take notes about questions.

Save the file.

Once you're done, check the contents of the file on the command line with the `cat` command followed by the name of your file.

## Solution

- Step 1

```zsh
$ code cheat-sheet.txt
```
- Step 2

```
$ cat cheat-sheet.txt
My Institute Cheat Sheet

ls
lists files and folders in a directory

cd ~
change directory to home folder
```

## Evaluation

What does effect does the following command produce?

```zsh
$ echo "Hello! My Name is Mark!" > introduction.txt
```
- It adds the line "Hello! My Name is Mark!" to the existing content of the `introduction.txt` file.
- It checks whether the content of the `introduction.txt` file contains the line "Hello! My Name is Mark!"
- It replaces the content of the `introduction.txt` file with the line "Hello! My Name is Mark!"*
- None of the above.