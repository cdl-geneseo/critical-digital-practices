---
title: Before You Start
layout: default
nav_order: 1
---

# Before You Start

One of the best ways to learn how a thing works is to play around with it. But it can be scary to play around with a piece of equipment that might have cost you or your family $1000 or more. As you start to play around with your computer, it's natural to worry that you might break something.

Rest assured that nothing you do in this course should put your computer's hardware at risk. You should be fine on the hardware side of things as long as you don't, say, drop your computer, or spill coffee on your keyboard, or close your screen on a pen.

But the software side is another matter. Here, yes, playing around could break something. The good news, though, is that virtually anything that might break on the software side can be easily fixed. The even better news is that figuring out how to fix something you broke is absolutely one of the best ways to learn.

We're talking about low-stakes breakage here anyway, such as accidentally deleting files, messing up a website you've built, or mangling a program you've written. If you follow a few precautions, then nothing you do in this course should break anything fundamental to your computer's normal functioning, and, again, anything that breaks should be easy to fix. But that's an important *if*. Let's go over some of these precautions.

## Back up your stuff

When playing around with your computer, the best insurance against grief and misery is to be able to put things back the way they were. If you already back up your most important files to a cloud service, that's a good start, but if you don't also back up to physical media such as an external drive or USB stick, you should seriously consider doing so. Set up automatic backups to your attached storage or establish a daily manual backup routine.

## Be careful what you touch

{: .alt-warning}
As you begin poking around in your computer's [file system]({{ site.url }}/mod-1/file-system), whether through your computer's graphical user interface (GUI) or from the [command line]({{ site.url }}/mod-2/what-is-the-command-line), you'll come across files and folders that you've likely never noticed before. These may be "hidden" files or folders (whose filenames begin with a `.`) or folders with names like `opt`, `bin`, and `usr`. You shouldn't be afraid of these files and folders. Banishing fear is one objective of this course! But banishing fear shouldn't be confused with throwing caution to the winds. ***You should treat these files and folders with respect and handle them with care&mdash;and <u>only</u> if you're absolutely sure you know what you're doing.*** 

## Search, but verify

The web is a rich information resource when you're trying to do something new on your computer (or trying to fix something you broke). But the quality of information you'll find there is far from uniform. If you turn to Google for answers (or to a more privacy-oriented search engine such as [DuckDuckGo](https://duckduckgo.com)), you'll want to follow a few basic rules.

- Be skeptical of sites that turn up in your search results whose URL is more or less identical to the thing you're trying to figure out how to do: e.g., `launchmyterminal.com`
- When looking at suggestions on community-driven sites like [Stack Overflow](https://stackoverflow.com/), [Stack Exchange](https://stackexchange.com/), and [Super User](https://superuser.com/), pay attention to how other users have voted on suggested answers to questions. Don't just pick the first suggestion you see.
- No matter where you find advice, see if you can find an answer to the same question elsewhere for confirmation that the advice is reasonable.

## sudo or sudon't?

{: .alt-warning}
Exercise special care when following advice that involves using `sudo` at the beginning of a terminal command. The term "sudo" is short for "super user do." When executing a command as a super user, you're taking an action that requires administrative privileges on your computer, and you'll be asked to enter your login password. You needn't be afraid to use `sudo`&mdash;a given command may simply require this level of privileges if you want to carry it out&mdash;but that may be because the command would affect some aspect of your computer's core functionality. Before using `sudo`, be certain that it's needed for what you want to accomplish, and be absolutely certain that you can trust the source of your advice.

## Ready to play? 

Okay then, [let's begin]({{ site.url }}/mod-1/overview).