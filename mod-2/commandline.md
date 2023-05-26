---
title: What is the Command Line?
layout: default
parent: Module 2
nav_order: 2
---

## The Command Line

The command line is the most direct way by which you can communicate with your computer. A strictly hierarchical, linear mode of access, your command line can take some time to adjust to, especially if the directory structure is already an unfamiliar concept to you. That being said, once you get the hang of it, working out the command line is an informed and powerful way to access and get things done on your computer. You can use the command line to easily navigate to all areas of your computer, not having to rely on what\'s available via the GUI (Graphical User Interface), to manipulate files and folders, to run and automate scripts, and more.

The screenshot above shows my terminal window. Now, yours isn\'t going to look like this; mine is customized to fit my ✨aesthetic✨\... but it won\'t be too different. Yours will look especially different if you\'re operating on a Windows machine. This difference is due to the difference between command line instances known as \"shells\". For a long time, the Windows Command Line shell that was built-in was the Command Prompt, or, CMD. In 2016, PowerShell came onto the scene as an open source, cross-platform shell for the Windows command line and is widely understood as a game-changer. 

Since Dr. Schacht and I are Mac users, we have little to no experience with or knowledge of PowerShell commands, only UNIX-based commands. So, to make it easy for us all to work together, we\'ve asked you all to download and install a program called [Git Bash](https://gitforwindows.org/){.inline_disabled target="_blank" rel="noopener"}, which will allow you to interact with a UNIX-familiar command line instance. \"Bash\" (Bourne Again Shell) is the command line shell most typically associated with Linux and MacOS.

## What does all that text even *mean*?

Let\'s take a closer look at my terminal window in the screenshot below and see if we can make some more sense of what we\'re being shown. 

At the very top of the terminal window, in the grey bar, you\'ll see that the letters \"zsh\" follow my username, aschmidt. These letters stand for \"z shell\", which is the (latest) MacOS command line shell. Like PowerShell for Windows, zsh is somewhat new, and comes with a lot more features than the old bash shell. We may explore some of these features later in the semester depending on interest and usefulness.

The first line you see in the main screen of the terminal window is an introductory line that notes the last time you were recorded as having logged onto terminal. According to this screenshot, the last time I logged onto terminal was Tuesday, September 28th at 10:13am.

The second line is where the action is. When you see a line that begins with this series of information, you\'ll know that you can start typing!

Starting at the very left, you\'ll see the **username** and, sometimes, the computer name included with it. My username is aschmidt, and my computer name immediately follows that username. This is necessary on my machine, because it\'s owned by the school, and is configured to include a unique computer ID that can be traced back to me.

The next piece of the line is where you\'ll look to determine your **current directory**, that is, where you physically are in your computer\'s directory structure. The \"\~\" shown in the screenshot means that we are in my \"home\" directory. If I were to move to my desktop, that \"\~\" would be replaced with \"Desktop\". It can be easy to lose track of where you are in the terminal, so one of the ways you can keep your wits about you is to check this part of the statement.

Finally, the \"%\" following the current directory section is what is considered the **prompt**. When you see this symbol appear, that means the terminal is ready for you to type a new command. In the old bash shell, this symbol was a \"\$\".

![Screenshot highlighting where to find the username, current directory, prompt, and shell symbols within the terminal on a Mac.](https://canvas.geneseo.edu/courses/20408/files/1839044/preview){style="display: block; margin-left: auto; margin-right: auto;" width="670" height="465" api-endpoint="https://canvas.geneseo.edu/api/v1/courses/20408/files/1839044" api-returntype="File"}

### Open your own terminal window! {#open-your-own-terminal-window style="max-width: 900px; margin: auto;"}

Now it\'s time to pull up your own window and see what it looks like on *your* machine!

**Mac users:** Bring up the search bar by typing \"⌘ + space bar\" then start to type in \"terminal.\" Select \"terminal\" from the search results.

**Windows users:** In your search bar (either in directly in your dock or within the \"Start\" button) start typing \"Git Bash\" and select the application from the results.

Try to identify everything we covered on this page in your own terminal window.
:::
