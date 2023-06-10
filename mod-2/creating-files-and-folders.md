---
title: Creating Files and Folders
layout: default
parent: The Command Line
nav_order: 7
---
# Creating Files and Folders

## Warm up

So far, we've only performed commands that give us information. Let's use a command that creates something on the computer.

First, make sure you're in your home directory:

```zsh
pwd
/Users/your-username # What you'll see on a Mac, where your-username is your actual username
/c/Users/your-username # What you'll see in Git Bash
/home/your-username # What you'll see in Ubuntu
```
On any of these operating systems, by the way, you can always verify the location of your home folder by typing

```zsh
echo $HOME
```
And wherever you are in your file system, you can always get *back* home by typing

```zsh
cd ~
```
The tilde (`~`) is shorthand for your home directory. In many (though not all) situations, using it will spare you the trouble of havng to type the full path to your home.

Let's move to the `Desktop` folder, or "change directory" with `cd`:

```zsh
cd Desktop
```
On Mac and in Windows, this will move you to your Desktop folder. In Ubuntu for Windows, a Desktop folder isn't automatically created. You can create one using the `mkdir` command. 

```zsh
mkdir Desktop # Only necessary for Ubuntu useres
```
Or you can simply create a new folder with any other name you like. The name should not contain spaces. After doing so, use `cd` to move into the new directory, as shown above for Mac and Windows.

Use `pwd` again to make sure you're in the `Desktop` folder (or other folder you've created).

```zsh
pwd
/Users/your-username/Desktop # Mac
/c/Users/schacht/Desktop # Git Bash
/home/your-username/Desktop # Ubuntu
```
Go back home.

```zsh
cd ~
```
Go back to your Desktop.

```zsh
cd ~/Desktop
```
You could have left out the `~/` in this last move because `Desktop` is immediately inside your home directory. But including it also works. So does the full path: `cd /Users/your-username/Desktop` on Mac, for example.

## Create a file

```zsh
touch foo.txt
```

The `touch` command is used to create a file without any content. This command can be used when you don’t have any data yet to store in it.

If the command succeeds, you won't see any output. Now move the terminal window and look at your "real" desktop, the graphical one. See any differences? If the command was successful and you were in the right place, you should see an empty text file called `foo.txt` on the desktop. Pretty cool, right?

## Handy Tip: Up Arrow

Let's say you liked that `foo.txt` file so much you'd like another! In the terminal window, press the <kbd>up arrow</kbd> on your keyboard. You'll notice this populates the line with the command that you just wrote. You can hit <kbd>enter</kbd> to create another `foo.txt,` (note - [`touch`](https://en.wikipedia.org/wiki/Touch_(Unix)) command will not overwrite your document nor will it add another document to the same directory, but it will update info about that file.) or you could use your left/right arrows to move the insert cursor around on the screen so you can, for instance, change the file name to `foot.txt` to create a different file.

As we start to write more complicated and longer commands in our terminal, the <kbd>up arrow</kbd> is a great shortcut so you don't have to spend lots of time typing.

## Creating Folders

OK, so we're going to be doing a lot of work during the Digital Humanities Research Institute. Let's create a `projects` folder on our desktop, where we can keep all our work in one place.

First, let's check to make sure we're still in the `Desktop` folder with `pwd`:

```zsh
pwd
/Users/your-username/Desktop
```

Once you've double-checked you're in `Desktop`, we'll use the `mkdir` or "make directory" command to make a folder called `projects`:

```zsh
mkdir projects
```

Now run `ls` to see if a projects folder has appeared. Once you confirm that the projects folder was created successfully, `cd` into it.

```zsh
cd projects
pwd
/Users/your-username/Desktop/projects
```

OK, now you've got a projects folder that you can use throughout the Institute. It should be visible on your graphical desktop, just like the `foo.txt` file we created earlier.

## Challenge

Try and create a sub-folder and file on your own!

## Solution

1. Type `pwd` to see where on your computer you are located. If you are not in the `projects` folder we just created, navigate to that folder using the commands you learned in the [lesson on navigation](https://curriculum.dhinstitutes.org/workshops/command-line/lessons/?page=6).
2. Type `mkdir name-of-your-subfolder` to create a subfolder.
3. Type `cd name-of-your-folder` to navigate to that folder.
4. Type `touch challenge.txt` to create a new text file.
5. Type `ls` to check whether you created the file correctly.

## Evaluation

What does the <kbd>up arrow</kbd> command do?
- It quits the Terminal/GitBash.
- It undoes my last command.
- It inserts my last command.*
- It shows me what folder I am working in.