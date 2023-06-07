---
title: Text Editors
layout: default
parent: What is Text?
nav_order: 3
---

# Text Editors

You've seen that you can create and edit plain text documents [right from the command line](/mod-2/editing-from-the-command-line). That's a handy skill to have, especially when you find yourself needing to edit a file on a remote server. But most of the time you'll want to do you plain text editing in a dedicated application that runs in your GUI. There are many such applications to choose from.

## Notepad and TextEdit

Notepad, mentioned in the previous section, is a plain text editor that comes bundled with the Windows operating system. Apple bundles its own text editor with macOS, called TextEdit. These applications provide minimal functionality for plain text editing, but it's good to know they're there and to understand a bit about how they work. By default your Mac will try to open files ending with the `.txt` extension in TextEdit. You'll want to change that behavior at some point, but until you do, you're certain to find yourself looking at the TextEdit interface.

You can launch Notepad by going to the Start menu and typing "Notepad" in the search box. You can launch TextEdit from your Applications folder or by holding down `command` while typing `Space` and typing "TextEdit" in the Spotlight search box.

By default, TextEdit will open in a "rich text" interface and want to save your files with the `.rtf` extension. RTF stands for "rich text format," a file format meant to be interoperable with Word and other word-processing applications. In RTF, you can format text just as you would in Word. You'll know you're looking at an RTF file in TextEdit if you see a formatting toolbar and ruler above your text.

![TextEdit file in rtf](../assets/textedit-rtf.png)

To make TextEdit useful for plain text editing, you'll want to change your settings to tell TextEdit to open new files as "Plain text."

![TextEdit settings](../assets/textedit-settings.png)

Your new TextEdit files should now look like this:

![TextEdit file in txt](../assets/textedit-txt.png)

One other thing to watch for with TextEdit. On newer Macs, by default your TextEdit files will be saved to your iCloud account. Be sure that when you save a TextEdit file, you instead choose a location on your computer itself, rather than iCloud.

## Visual Studio Code

For this course, it's recommended that you install Microsoft's Visual Studio Code and use it for your text editing tasks. VS Code is free to use and has a host of advanced features that will simplify your workflow and help you better understand the structure of your plain text documents. To install it, follow [these instructions if you're on a Mac](https://www.curriculum.dhinstitutes.org/installations/microsoft-visual-studio-code/macos/) or [these instructions if you're using Windows](https://www.curriculum.dhinstitutes.org/installations/microsoft-visual-studio-code/windows/).

Be sure to follow the instructions carefully! Be particularly careful to carry out Step 6 (Mac) or Step 7 (Windows) so that, once it's installed, you'll be able to invoke VS Code from the command line.