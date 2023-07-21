---
title: Getting Started
layout: default
parent: The Command Line
nav_order: 4
---
# Getting Started

As we saw previously, macOS comes with a terminal application you can use to start a shell session and begin working at the command line. If you're a Windows user, you should have installed Git Bash or Ubuntu, as described in [Types of Commands]({{ site.url }}/mod-2/types-of-commands).

You can launch Terminal.app in macOS by finding it in Applications > Utilities > Terminal.app or by doing a Spotlight search for the application. Once you've installed Git Bash or Ubuntu, you can launch either by searching for it in the Start menu.

## The command prompt

No matter what OS you're on or what your terminal application looks like, it will present you with a cursor to the right of a command **prompt**. The cursor may be a vertical line, underscore, or rectangular block, and it may or may not be blinking. The prompt may appear as a $, %, &#x2192; or other symbol. To the left of the prompt, you may see `your-username@your-computer-name:` (where `your-username` is your actual username and `your-computer-name` is the name of your own computer). On a Mac, you may see information about transitioning from Bash to Zsh. You can safely ignore that message for now and continue with Bash. You can play at your leisure with the settings of your terminal application to change the cursor style, background color, font style, font size, and more. In Terminal.app, the default font size is pretty small. That's one setting you may want to consider changing.

For the most part, when example commands are displayed in this course, the prompt symbol has been omitted. In other words, you'll see this:
```zsh
pwd
```
rather than this:
```zsh
$ pwd
```
## Typing commands

The command line is fussy about things like spelling and case. It doesn't do autocorrect, and if you accidentally type `mwfile.txt` it won't ask, helpfully, "Did you mean myfile.txt"? Instead it will just shrug and return, "No such file or directory."

You'll want to type slowly at the command line, and if you don't get the result you're looking for, the first thing you'll want to do is check whether you spelled things correctly.

## Moving your cursor

Since the command line pre-dates the GUI by many years, it also pre-dates the mouse. There are ways to use your mouse or trackpad at the command line, but we'll look past those for now. You'll want to develop the skill of moving around in and deleting text with your keyboard alone. Here are some useful keyboard commands to know for text navigation:

- Right-arrow (&#x25b6;): Move right one character
- Left-arrow (&#x25c0;): Move left one character
- `ctrl`-a: Go to the beginning of the line
- `ctrl`-e: Go to the end of the line
- `ctrl`-u: Delete from the cursor position to the start of the line
- `ctrl`-k: Delete from the cursor position to the end of the line
- `option`-f (Mac): Move forward a word at a time (Other keyboards use `alt`-f)
- `option`-b (Mac): Move backward a word at a time (Other keyboards use `alt`-b)

One thing you can definitely do with your mouse or trackpad, though, is select, copy, and paste text. This behavior is available by default in Terminal.app on Mac. You have to enable it in Git Bash and WSL, as described in [Types of Commands]({{ site.url }}/mod-2/types-of-commands).


## Your friend: tab completion

You do have one stay against the pulling of hair and gnashing of teeth that typos and misspelled words are bound to create at the command line: tab completion.

Let's say you want to tell your shell to do something with a file named `supercalifragilisticexpialidocious.txt`. If you just type a few letters, say `super`, and hit the `tab` key, your shell should auto-complete the file name. If there's another file in the same directory named `superwoman.txt`, your shell will show you both filenames, and typing either `c` or `w` and hitting `tab` again will enable you to select the one you want. If you type `super`, hit `tab`, and get *no* result, your shell is silently informing you that at your current location in your file system, there is, in fact, *no file or directory* that begins with the string `super`. Maybe the file you're looking for actually has a different name, or maybe you're not at the location in your file system where the file lives. Soon, you'll learn how to see just where you are and get to where you want to be.