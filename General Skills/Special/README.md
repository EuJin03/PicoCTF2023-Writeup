# Special

## Overview

**300 points**

Category: [General Skills](../)

Tags: `#bash` `#ssh`

AUTHOR: LT 'SYREAL' JONES

DESCRIPTION
Don't power users get tired of making spelling mistakes in the shell? Not anymore! Enter Special, the Spell Checked Interface for Affecting Linux. Now, every word is properly spelled and capitalized... automatically and behind-the-scenes! Be the first to test Special in beta, and feel free to tell us all about how Special streamlines every development process that you face.
When your co-workers see your amazing shell interface, just tell them:
That's Special (TM)
Start your instance to see connection details.
ssh -p 64886 ctf-player@saturn.picoctf.net
The password is fd7746b4

HINT

1. _Experiment with different shell syntax_

---

## Approach

This challenge is a bit tricky for me. Things has started to elevated and get nerdy hard. It took me hours to experiment with different bash shell syntax. From all commonly used bash commands such as `ls`, `echo`, `pwd`, `whoami` and so on to bash variables, command substitution to nested bash commands. It autocorrects words and capitalize it on every single commands.

After some trial and error with different symbols, I found out that `(pwd)` is able to return me `/home/ctf-player`. It could be the clue to solve this challenge. However, other useful commands such as `cat` and `ls` does not work unfortunately. When i tried some random commands, sometimes it prompts me a clue which is `Why go back to old shell?`.

After some googling, I stumbled upon a [website](https://0xffsec.com/handbook/shells/restricted-shells/#reconnaissance) that explains about _Escaping from Restricted Shell_. On the _Reconnaissance_ section, it explains that we can use `env` command to check the environment variables. And most _IMPORTANTLY_, i could escape from the restricted shell by using `$0` command.

By entering `Special$ ($0)` into the command line, the shell has been escaped and it is no longer the GODDAMN Special Shell.

## Solution

The commands that I used to retrieve the flag:

```
Special$ ($0)
$ echo */*
/blargh/flag.txt
$ cat ./blargh/flag.txt
picoCTF{5p311ch3ck_15_7h3_w0r57_f578af59}
```
