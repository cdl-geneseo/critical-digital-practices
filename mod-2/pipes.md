---
title: Pipes
layout: default
parent: The Command Line
nav_order: 10
---
# Pipes

At the command line, the pipe character (`|`) lets you take the output of one command and use it as the input for another.

Let's consider how we might pipe the output of the `echo` command to another command, `wc`. The `echo` command does pretty much what its name says: it "echoes" the content contained in the argument to the command.

```zsh
echo "The quick brown fox jumps over the lazy dog"
The quick brown fox jumps over the lazy dog
```
In this case, `echo` simply prints the argument we've given it&mdash;the text string "The quick brown fox jumps over the lazy dog"&mdash;to `stdout`.

With the pipe, we can make this string the argument to another command. For example,

```zsh
echo "The quick brown fox jumps over the lazy dog" | wc -w
9
```
What happened? Rather than being printed to `stdout`, the output of `echo` was piped to the `wc` command with the `-w` option. The `wc` command counts things&mdash;words if we pass `-w` to it, lines if we pass `-l` to it, characters (or bytes) if we pass `-c` to it. What we get at `stdout` is only the output of the second command. Our text string, says `wc`, contains 9 words.

Try this for yourself, using either the same string as in the example or a different one, first printing the string to `stdout`, then piping it to `wc` with your preferred option.

Remember that you don't have to type your string twice! After executing `echo` with your string as argument the first time, simply type &#x25b2; to bring the command up a second time. Your cursor will be waiting for you at the end of the line, where you can add the pipe symbol and your second command before hitting `enter` again.