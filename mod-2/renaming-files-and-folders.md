---
title: Renaming Files and Folders
layout: default
parent: The Command Line
nav_order: 7
---
# Renaming Files and Folders

You can rename files and folders from the command line using the command `mv`. The command is short for "move," which might seem like an odd name for a command whose effect is to change names. But the fact is, when you rename a file or folder, you're in effect creating a new path. You're moving the file or folder's current location to a new one.

A common analogy for a file path, in fact, is a postal address. Just as a postal address begins with an individual person's name and continues outward to reference more encompassing domains, so a path on your computer begins with the most encompassing domain and narrows down to an individual folder or file.

```zsh
Alex Smith # individual person
3492 Oak Lane # street address
Anytown, NY # locality and state
USA # country
```
```zsh
/Users/username/folder-inside/folder-inside-that/folder-inside-that-one/file.xt
# / = most encompassing
# Users = one of several folders at this level
# username = one of several possible users
# folder-inside/folder-inside-that/folder-inside-that-one/ = drilling down several levels
# file.txt = individual file
```
This analogy helps explain why it's common to talk about a file as "living" at a particular spot on your computer. Every path is a unique address. To change a name is to tell your computer that what was once at one address is now to be found at new one. "We've moved!"

We can use complete file paths when executing the `mv` command, but as with many other operations, we can omit more-encompassing parts of a path when operating within a specific directory.

So let's say you start off at the folder we created earlier. Get there from anywhere with the following:

```zsh
cd ~/critical-digital
```
Inside `critical-digital` we earlier created the file `foo.txt`. Use `ls` to verify that it's there. If it isn't, created it using `touch`.

To rename `foo.txt` to `bar.txt` we would do the following:

```zsh
mv foo.txt bar.txt
```
Try this, followed by `ls` to verify that the change took effect. If you had any contents in `foo.txt`, they would not be altered by the move. You didn't change what's inside the file, only where the file lives. That is, you renamed it.

You can do the same with folders. Using `mv` to rename the folder won't affect the folder contents (except to give the contents, too, a new address&mdash;differing only at the point in the address where the folder name was changed).

Earlier, you created `my awesome file.txt` inside `some other folder`. Maybe you want to rename that folder.

```zsh
cd "~/critical-digital/some folder"
mv "some other folder" better-folder
```
If you do this and peek into `better-folder` with `ls`, you'll see that `my awesome file.txt` is still living inside.

## Moving things with mv

You can use `mv` to move files and folders in the more familiar sense of relocating them to other folders. For example, you can use it move `my awesome file.txt"` out of `better-folder` and into `critical-digital`, two levels above. For this example, we'll use full paths:

```zsh
mv ~/critical-digital/some\ folder/better-folder/my\ awesome\ file.txt ~/critical-digital/my\ awesome\ file.txt
```
If we then `cd` to `critical-digital`, we can use `ls` to confirm the move.

{: .warning}

The `mv` command is a powerful one. You can pretty much re-locate anything anywhere if you do it right. But doing it wrong can lead to heartache. Practice using it and get confident with it before using it with important files and folders. Consider backing up important files and folders in the GUI before you try anything fancy with them from the command line.