# Permissions

## Overview

**100 points**

Category: [General Skills](../)

Tags: `#vim`

AUTHOR: GEOFFREY NJOGU

DESCRIPTION
Can you read files in the root file?
The system admin has provisioned an account for you on the main server
Can you login and read the root file?

HINTS

- _What permissions do you have?_

---

## Solution

Boring challenge, ssh into the shell and navigate into the root directory, saw a directory named `challenge`. It contains a file that bear a flag, hence it can be solved by simply `cat {filename}`

> picoCTF{<redacted>}
