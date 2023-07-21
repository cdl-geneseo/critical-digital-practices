---
title: What is the Command Line?
layout: default
parent: The Command Line
nav_order: 2
---
# What is the Command Line? 

The command line is an interface for communicating with your computer's operating system. You'll sometimes see it referred to with the abbreviation "CLI" for "Command Line Interface."

You typically access the command line through a program called a "shell." Common shell programs for Unix-related operating systems (including macOS and Linux) are Bash (an acronym for Bourne Again SHell) and Zsh (Z shell). On a Windows computer, there's PowerShell.

You can use the command line to navigate, access information about, and manipulate your [file system]({{ site.url }}/mod-1/file-system#know-thy-file-system) (folders and files), access and manipulate peripherals (such as an external drive), and run programs. Before the widespread adoption of the [graphical user interface (GUI)](https://arstechnica.com/features/2005/05/gui/), the command line provided the principal means of interacting with a "personal" or "desktop" computer. Before the advent of the personal computer, a computer operator might use the command line on a device called a "console" or "terminal" to connect and interact with a computer located somewhere other than the operator's desktop. This "mainframe" computer might take up an entire room. One way to think about the command line on your desktop computer is as a kind of terminal emulator, recreating, on a single machine, that pre-graphical, text-based relationship between user and computer. This is why the program you use on a Mac to launch and work inside a shell is called Terminal.app. You can find Terminal.app by navigating to Applications > Utilities in your file system and looking for it by name, or by searching for it using [Spotlight](https://support.apple.com/guide/mac-help/search-with-spotlight-mchlp1008/mac).

## Some things you can do at the command line

- Easily automate tasks such as creating, copying, and converting files.
- Execute a variety of useful commands built into the shell software (aka [builtins](https://www.computerhope.com/jargon/b/builtin.htm)).
- Run a great many other productivity-enhancing programs and [packages](https://www.computerhope.com/jargon/p/package.htm) freely shared by developers and available through sources such as [Homebrew](https://brew.sh/) and [APT](https://www.computerhope.com/jargon/a/apt.htm) .
- Connect to and interact with a remote server, such as the server that hosts a website you own. 

## The bigger picture

Familiarizing yourself with the command line not only gives you the ability to accomplish certain computing tasks more easily. It also changes your relationship to your computer in a crucial way, making the operation of your computer a bit less mysterious and thereby giving you a bit more power and autonomy in how you use it&mdash;as well as in your ability to control how it uses you.

If you're thoroughly comfortable with your computer's GUI, this may seem like an odd claim. It's the command line that's likely to strike you as mysterious, requiring you to learn a new vocabulary and set of routines, and giving you scant assistance when your interactions with it don't go as planned. The brilliance of the modern GUI lies precisely in its ability to reduce the friction between your intentions and its actions. Every refinement to the GUI increases the illusion of direct manipulation: point, click, drag 'n drop, or&mdash;on mobile devices and interactive screens&mdash;*literally* carry out actions with your hands (the root meaning of the word "manipulate"). Devices that respond to voice commands increase still further the illusion of control: your spoken wish is the machine's command, which is to say that you're the one *in* command.

But who's really in command when, to borrow a phrase from the science fiction writer Arthur C. Clarke, as far as you're concerned your computer's responses to your commands are ["indistinguishable from magic"](https://en.wikipedia.org/wiki/Clarke%27s_three_laws)? 

The truth is that even as modern computer interfaces put increasing power at our fingertips, they also increase the power of those who design them, in part by burnishing their own self-image as magicians, but also by enabling them to define the horizon of possibility we see in our own devices. It's perhaps no accident that these interfaces increasingly seem to hide, by default, controls and settings that were once readily visible, even as the hardware that runs those intefaces is increasingly difficult for users to access, modify, or [repair](https://www.ifixit.com/Right-to-Repair) for themselves.

Even when working at the command line, you're interacting with your computer in a way that's *mediated* by layers of software that others have written and that thereby shape your experience, which means that layers of mystery still separate you from the 0's and 1's that are the only real language computers understand. In very different ways, Neal Stephenson's essay "In the Beginning Was the Command Line" (1999) and Wendy Chun's ["On Software, or the Persistence of Visual Knowledge"](https://direct.mit.edu/grey/article/doi/10.1162/1526381043320741/10837/On-Software-or-the-Persistence-of-Visual-Knowledge) (2004) explore the history through which these layers came to be, and what that history means not just for our experience as computer users but for the ongoing relationship between digital technology and other aspects of society.

Learning to use the command line won't set you free, but it will certainly make you less readily subject to the manipulation and control of others.