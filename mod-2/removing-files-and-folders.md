---
title: Removing Files and Folders
layout: default
parent: The Command Line
nav_order: 8
---
# Removing Files and Folders

You can remove files and folders (together with their folder contents) with the `rm` command.

{: .warning}
When you use `rm`, you delete files and folders ***permanently***. This is not the same as moving them to the Trash or Recycle Bin. Files removed with `rm` are ***gone***. Your can't get them back. Before using `rm`, it's crucial that you know where you are in your file system and will be truly removing what you want to remove. Check inside folders before removing them.

## Remove a file

To remove the file `foo.txt`, use `cd` to navigate to the directory where it lives, then execute

```zsh
rm foo.txt
```
You can add the `-i` option if you'd like to be asked one last time if you're certain.

```zsh
rm -i foo.txt
remove foo.txt?
```
Type "y" to proceed, "n" to change your mind.

You can use the `-i` option with folders, too, but you'll be prompted to approve the deletion of each file individually.

## Remove a folder (and its enclosed contents)

To remove a folder, use `cd` to navigate to the directory where the folder lives, then execute

```zsh
rm -r some-folder
```

The `-r` option is short for "recursive." The command will delete the folder and, to repeat, ***all its contents, including other folders inside it, folders inside them, and the files inside these folders.***
Use this command with extreme caution.