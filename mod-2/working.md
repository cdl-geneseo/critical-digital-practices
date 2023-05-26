---
title: Working at the Command Line
layout: default
parent: Module 2
nav_order: 3
---

## Command structure

Now that you\'ve gotten used to seeing the terminal and understand a little bit more about how it works, let\'s learn a little more about how commands are structured.

<figure>
<img src="$IMS-CC-FILEBASE$/Uploaded%20Media/Screen%20Shot%202021-09-29%20at%2010.38.45%20AM.png" style="display: block; margin-left: auto; margin-right: auto;" data-api-endpoint="https://canvas.geneseo.edu/api/v1/courses/20408/files/1841203" data-api-returntype="File" width="556" height="174" alt="Screenshot displaying annotated command in the MacOS terminal showing &quot;command,&quot; &quot;option,&quot; &quot;argument,&quot; and &quot;cursor&quot; from left to right." />
<figcaption>Command structure of the command line. (Remember, your prompt may look different!)</figcaption>
</figure>

As shown in the screenshot above, the first part of the command structure is the actual **command**, or, what you actually are trying to do. The command in this example is `rm` which stands for \"remove\" and is used to delete files/folders on your machine. Following this part of the structure would be where you could claim an **option**, or, parameters you can set for your command to follow. In this case, the `-f` option means you\'d like the `rm` command to work without prompting for confirmation. Next, comes the command line **argument**, which is the file, folder, or program that you\'d like to influence.

### Preliminary tips

1.  Go **slow** at first, you\'ll be less likely to make a mistake. Navigating the command structure can be tricky, especially at the beginning.
2.  Check your **spelling**; if you misspell something, your code won\'t work, and there\'s no spell checker.
3.  The command line is **case-sensitive**. A lowercase letter versus an uppercase letter will mean something different, and that matters. Spacing also matters, as a \"whitespace\" is considered a distinct character.
4.  **Type**, don\'t copy/paste. While it may be tempting, and is certainly something you can do when trying to go fast, copy/pasting isn\'t going to help you understand what you\'re instructing your computer to do.

## Getting started: know thyself

You may also see your username to the left of the command prompt `%`. Let\'s try our first command. Type the following and press `enter` on your keyboard:

`% whoami`

The `whoami` command should print out your username. Congrats, you\'ve executed your first command! This is a basic pattern of use in the command line: type a command, press `enter` on your keyboard, and receive output.

## Orienting Yourself in the Command Line: Folders

OK, we\'re going to try another command. But first, let\'s make sure we understand some things about how your computer\'s filesystem works.

Your computer\'s files are organized in what\'s known as a hierarchical filesystem. That means there\'s a top level or `root` folder on your system. That folder has other folders in it, and those folders have folders in them, and so on. You can draw these relationships in a tree:

![Screenshot of the directory structure in the GUI.]($IMS-CC-FILEBASE$/Uploaded%20Media/hierarchical-filesystem-example.png){style="display: block; margin-left: auto; margin-right: auto;" width="796" height="278" api-endpoint="https://canvas.geneseo.edu/api/v1/courses/20408/files/1841661" api-returntype="File"}

The `root` or highest-level folder on macOS is just called `/`. We won\'t need to go in there, though, since that\'s mostly just files for the operating system. On Windows, the root directory is usually called `C:`. 

Note that we are using the word \"directory\" interchangeably with \"folder\"---they both refer to the same thing.

OK, let\'s try a command that tells us where we are in the filesystem:

`% pwd`

You should get output like `/Users/your-username`. That means you\'re in the `your-username` directory in the `Users` folder inside the `/` or root directory. This directory is often called the \"home\" directory.

On Windows, your output would instead be `C:/Users/your-username`. The folder you\'re in is called the working directory, and `pwd` stands for \"print working directory.\" \"Print\" as a word can be somewhat misleading. The command `pwd` won\'t actually print anything except on your screen. This command is easier to grasp when we interpret \"print\" as \"display.\"

Now we know \"where\" we are. But what if we want to know what files and folders are in the `your-username` directory, a.k.a. the working directory? Try entering:

`% ls`

You should see a number of folders, probably including `Documents`, `Desktop`, and so on. You may also see some files. These are the contents of the current working directory. `ls` will \"list\" the contents of the directory you are in.

Wonder what\'s in the `Desktop` folder? Let\'s try navigating to it with the following command:

`% cd Desktop`

The `cd` command lets us \"change directory.\" (Make sure the \"D\" in \"Desktop\" is capitalized.) If the command was successful, you won\'t see any output. This is normal---often, the command line will succeed silently.

So how do we know it worked? That\'s right, let\'s use our `pwd` command again. We should get:

`% pwd`\
`/Users/your-username/Desktop`

Now try `ls` again to see what\'s on your desktop. These three commands---`pwd`, `ls`, and `cd`---are the most commonly used in the terminal. Between them, you can orient yourself and move around.

## Challenge

Take a minute to navigate through our computer\'s file system using the command line. Use the three commands you\'ve just learned---`pwd`, `ls` and `cd`---eight (8) times each. Go poking around your `Photos` folder, or see what\'s so special about that root `/` directory. When you\'re done, come back to your \"home\" folder with

`% cd ~`

(That\'s a tilde `~`, on the top left of your keyboard.) One more command you might find useful is `cd ..` which will move you one directory up in the filesystem. That\'s a `cd` with two periods after it:

`% cd ..`

### Compare with the GUI

It\'s important to note that this is the same old information you can get by pointing and clicking displayed to you in a different way.

Go ahead and use pointing and clicking to navigate to your working directory---you can get there a few ways, but try starting from \"My Computer\" and clicking down from there. You\'ll notice that the folder names should match the ones that the command line spits out for you, since it\'s the same information! We\'re just using a different mode of navigation around your computer to see it.

### Solution

1.  Type `pwd` to see where on your computer you are located.
2.  Type `cd name-of-your-folder` to enter a subfolder.
3.  Type `ls` to see the content of that folder.
4.  Type `cd ..` to leave that folder.
5.  Type `pwd` to make sure you are back to the folder where you wish to be.
6.  Type `cd ~` to go back to your home folder.
7.  Type `pwd` to make sure you are in the folder where you wish to be.
8.  Type `cd /` to go back to your root folder.
9.  Type `ls` to see the content of folder you are currently in.
10. Type `pwd` to make sure you are in the folder where you wish to be.
11. Type `cd name-of-your-folder` to enter a subfolder.

## Evaluation

What command do you run if you are trying to identify where in the filesystem you are currently located/working?

`% ls`

`% pwd*`

`% cd`

`% whoami`

When and why would you want to use the command line as opposed to your operating system\'s GUI?

### Keywords

Do you remember the glossary terms from this section?

-   Filesystem
-   GUI
-   Root

------------------------------------------------------------------------

~Based\ on\ a\ work\ at <https://github.com/DHRI-Curriculum>.\ When\ sharing\ this\ material\ or\ derivative\ works,\ preserve\ this\ paragraph,\ changing\ only\ the\ title\ of\ the\ derivative\ work,\ or\ provide\ comparable\ attribution.~
