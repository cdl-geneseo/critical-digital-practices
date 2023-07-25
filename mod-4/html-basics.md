---
title: HTML Basics
layout: default
parent: Internet and Web
nav_order: 5
---

# HTML Basics

## Create an HTML file

Open a terminal window and navigate to the [folder you created in the command line module]({{ site.url }}/mod-2/creating-files-and-folders).

```zsh
cd ~/critical-digital
```
If didn't create a folder with that name, or you've deleted it since completing the earlier module, create a new one.

```zsh
mkdir ~/critical-digital
```
The name of the folder isn't really important. If you prefer, you can give the folder a different name and swap that name in for `critical-digital` where necessary in the examples below. The location of the folder isn't really important, either. You could, for example, create your folder for this section inside `~/Documents`. The important thing is to take note of where your folder is so that you can navigate to it when you need to either from the command line or the GUI.

If you haven't already done so, navigate into the folder. Again, if the folder already exists, the command to do that is

```zsh
cd ~/critical-digital
```
Use `pwd` to make sure you're where you want to be. Ready? Now create and open a new file named `index.html` in your [text editor of choice]({{ site.url }}/mod-3/text-editors). If you're using [VS Code]({{ site.url }}/mod-3/text-editors#visual-studio-code), the command will be

```zsh
code index.html
```
Remember that the file will be lost until you save it at least once, so do that now with `cmd-S` (macOS) or `ctrl-S` (Windows).

Type or paste the following into your new file:

```html
<!DOCTYPE html>
<html>
    <head>
        <title>My Awesome Web Page</title>
    </head>
<body>
    <!-- This is a comment and won't be displayed. -->
    <p>This is an HTML document with one-sentence.</p>
</body>
</html>
```

Save the file.

## Open the file in a browser

Now let's see how your file looks in a browser. Navigate to the file in your GUI. If you're having difficulty locating it there, you can right-click on the file tab in VS Code and select "Reveal in Finder" (macOS) or "Reveal in File Explorer" (Windows).

![VS Code context menu showing Reveal in Finder selected](../assets/reveal-in-finder.png)  
*Right-click the file tab in VS Code to reveal the file's location in Finder or File Explorer*

You may be able to open the file in your system's default browser by simply double-clicking it. If that doesn't work&mdash;if the file opens in a text editor, for example&mdash;try right-clicking the file in your GUI and choosing "Open with" from the context menu that pops up. Then select the browser in which you'd like to open the file.

![File Explorer in Windows showing Open With in context menu](../assets/open-with-windows.png)

The result will look pretty bare bones: The sentence, "This is an HTML document with one-sentence" looking rather lonely in the upper left of your browser window, probably in the Times font, on a white background.

Notice that the address in your browser's location bar doesn't begin with `http://`  or or `https://` but with `file://`, and that the rest of the address is simply the path to the file on your machine. We saw the same thing before when ...

Notice that this bit of your file is nowhere to be seen:

```html
<!-- This is a comment and won't be displayed. -->
```
That's because your markup has identified this bit as a comment, so&hellip;it won't be displayed.

Notice also that the text you put in the `<title>` element shows up, not within your document, but in the browser tab or title bar. Your document's "title" isn't part of the document at all; it's information *about* your document, also known as **metadata**.



## Edit the document

It might be nice to put some kind of title or heading in the document itself. Let's do that.