# useless

## Overview

**100 points**

Category: [General Skills](../)

Tags: `#man`

AUTHOR: LOIC SHEMA

DESCRIPTION
There's an interesting script in the user's home directory The work computer is running SSH. We've been given a script which performs some basic calculations, explore the script and find a flag. Hostname: saturn.picoctf.net Port: 60547 Username: picoplayer Password: password

---

## Approach

After ssh into the instance, we can see a file called `useless` in the default directory. I ran the command `file useless` to see what type of file it was. It returns me `useless: Bourne-Again shell script, ASCII text executable`. I attempted to run the script and it says `Read the code first`. Hence, i `cat` the file and see the following code:

```bash
#!/bin/bash
# Basic mathematical operations via command-line arguments

if [ $# != 3 ]
then
  echo "Read the code first"
else
        if [[ "$1" == "add" ]]
        then
          sum=$(( $2 + $3 ))
          echo "The Sum is: $sum"

        elif [[ "$1" == "sub" ]]
        then
          sub=$(( $2 - $3 ))
          echo "The Substract is: $sub"

        elif [[ "$1" == "div" ]]
        then
          div=$(( $2 / $3 ))
          echo "The quotient is: $div"

        elif [[ "$1" == "mul" ]]
        then
          mul=$(( $2 * $3 ))
          echo "The product is: $mul"

        else
          echo "Read the manual"

        fi
fi
```

Seems like the bash script needs to append some arguments to perform some basic arithmatic from cli. However, there is an else statement that pique my interest:

```bash
else
	echo "Read the manual"
fi
```

## Solution

It reminds me of the command `man` that will prompt me bunch instructions and manual regarding a file. Hence, i ran the command `man useless` and voila! i got the flag. _Hope the author does not implies that man are useless :D_

> picoCTF{us3l3ss_ch4ll3ng3_3xpl0it3d_6173}
