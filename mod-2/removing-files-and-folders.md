---
title: Removing Files and Folders
layout: default
parent: The Command Line
nav_order: 11
---
# Removing Files and Folders

Create a new folder, or go to the folder you used previously.

```zsh
$ cd path/to/folder
```
or

```zsh
$ cd Desktop
```
or other desired location, such as `Documents`. After creating the folder, descend into it with `cd`.

```zsh
$ mkdir workshop
$ cd workshop
```
(Note that `workshop` is an example name. Name your folder whatever you like!)

Create a folder within the folder.

```zsh
$ mkdir my-new-folder
```
Again, use any name you like for your folder, but remember, no spaces in the name!

Descend into the folder.

```zsh
$ cd my-new-folder
```
Create a new file inside your new folder.

```zsh
$ touch my-awesome-file.txt
```
Open the file in VS Code.

```zsh
$ code my-awesome-file.txt
```
If the `code` command doesn't open your text file in Visual Studio Code, either you haven't yet installed Visual Studio Code or you neglected to follow Step 5 in the <a href="https://github.com/DHRI-Curriculum/install/blob/v2.0/guides/visual-studio-code.md" target="_blank">installation instructions</a>.

No worries. If do you have VS Code installed, fire it up and open your file with File > Open. If you don't, locate the file in the GUI and double-click to open it. It should open in your operating system's default plain text editor, such as TextEdit (Mac) or Notepad (Windows).

Make a mental note to get yourself properly set up in VS Code at a later date. 

Add some content to the file. Type anything you like. Maybe "Hello, World!" Save the file.

Switch back to your terminal and look inside the file.

```zsh
$ cat my-awesome-file.txt
```
Let's remove (delete) the file.

```zsh
$ rm my-awesome-file.txt
```
**Important**: The `rm` command deletes files and folders from your computer *permanently*. It doesn't move them to a "Trash" or "Recycle" folder. Once you remove files or folders this way, you can't get them back. 

If you still have the file open in VS Code, you'll see "(deleted)" next to the file name. Notice that your file content is still there. This does, in fact, give you a way to recover the file content, using `File > Save` or `File > Save As`. Technically, you're not getting your original file back but creating a new file with the content that's still displayed in your VS Code window. 

If you don't want that file content any more, click the "x" next to the file name, and the content will be permanently deleted. Note that if you hadn't had the file open in VS Code, you wouldn't have had this option. There would have been no going back after issuing `rm` at the command line.

Let's create a new file.

```zsh
$ touch my-terrific-file.txt
```
Once again, open the file in VS Code or another application to add content.

```zsh
$ code my-terrific-file.txt
```
(Pro tip: You could have actually skipped the `touch` step above; simply typing `code filename.txt` at the command line will create a file *and* open it in VS Code. But we've walked you through both steps to help you remember the `touch` command. Also, fair warning: A file created with `code` doesn't actually exist in your filesystem *until* you save it.) 

Type something in the file and save it.

Look inside the file from the command line.

```zsh
$ cat my-terrific-file.txt
```
Not seeing the content you added? Double-check that you *saved* the content, then try again.

Ascend out of `my-new-folder` (or whatever you called the folder you're working in). We're going to remove `my-new-folder`. We can't do that from inside the folder; that's why we have to move up a level.

```zsh
$ cd .. 
```

Be sure to include those two dots in your command, or you'll likely find yourself back in your home directory (`~`). Did that happen to you? Type `cd -` and your shell should return you to your previous location. 

Let's remove the folder. First, though, let's be extra careful and make sure that we know what we'll be removing. Remember that if you remove a folder with lots of files in it, you won't have a way to get them back. It's always a good idea to take one last look inside a folder before removing it.

```zsh
$ ls my-new-folder
```
Your terminal will list the contents of the folder. If what it lists isn't what you expected, double-check where you are in your file hierarchy. (Remember that `pwd` is helpful for this.) Your location should be something like `/Users/your-user-name/Desktop/workshop`, and if you simply type `ls`, you should see `my-new-folder` listed. 

In the right place? Time to remove the folder. In your GUI, when you delete a folder, its contents are deleted, too. At the command line, the process works a little differently. If you type

```zsh
$ rm my-new-folder
```
you'll get an error message that will look something like this:

```zsh
rm: vim-test: is a directory
```
This is a pretty helpful safeguard. Imagine if you thought you were removing a single, unneeded file, only to find that you'd permanently deleted a directory holding hundreds of valuable files!

To remove a directory (aka a "folder") from the command line, you have to add the `-r` flag to your command. The `-r` stands for "recursive." When you tell your shell to remove a directory, you're actually telling it to loop through the list of files in the directory and remove each one individually. This is true even if the list is a list of only one.

Once the files have been removed (remember: *permanently!*), the empty directory  is removed as well.

Got it? Here we go.

```zsh
$ rm -r my-new-folder
```

If you now type `ls` at the prompt, you should no longer see `my-new-folder` listed inside `workshop`.