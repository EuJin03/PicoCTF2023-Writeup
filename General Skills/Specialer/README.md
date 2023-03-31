# Specialer

## Overview

**400 points**

Category: [General Skills](../)

Tags: `#bash` `#ssh`

AUTHOR: LT 'SYREAL' JONES

DESCRIPTION
Reception of Special has been cool to say the least. That's why we made an exclusive version of Special, called Secure Comprehensive Interface for Affecting Linux Empirically Rad, or just 'Specialer'. With Specialer, we really tried to remove the distractions from using a shell. Yes, we took out spell checker because of everybody's complaining. But we think you will be excited about our new, reduced feature set for keeping you focused on what needs it the most. Please start an instance to test your very own copy of Specialer.
Start your instance to see connection details.
ssh -p 58983 ctf-player@saturn.picoctf.net
The password is 8a707622

HINT

1. _What programs do you have access to?_

---

## Approach

Thanks god, this challenge requires less head scratching compared to (Special)[../Special]. Somehow, I am not able to use commands such as `ls, cat, file and so on...`

However, I could still use `cd` and `echo`. I could read the directory I am located by using `echo *` and navigate using `cd`.

```
Specialer$ echo *
abra/ 	ala/ 		sim/
```

I am allowed to navigate into these directory and read the files by

```
Specialer$ cd ala
Specialer$ echo *
kazam.txt 	mode.txt
```

However, when I tried to read the files with `cat, head, tail, less and so on`, it returns me `-bash: {cmd}: command not found`. Looks like i need to find another way to read the files. After some googling, I found out that I could utilize bash scripts to read files such as `printf "%s" "$( <{filename})"`.

```
Specialer$ printf "%s" "$( <kazam.txt)"
return 0 picoCTF{y0u_d0n7_4ppr3c1473_wh47_w3r3_d01ng_h3r3_49193632}
```

## Solution

The commands that has been used to solve this question:

```
Specialer$ cd ala
Specialer$ printf "%s" "$( <kazam.txt)"
return 0 picoCTF{y0u_d0n7_4ppr3c1473_wh47_w3r3_d01ng_h3r3_49193632}
```
