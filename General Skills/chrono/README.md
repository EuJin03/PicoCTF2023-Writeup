# chrono

## Overview

**100 points**

Category: [General Skills](../)

Tags: `#linux`

AUTHOR: MUBARAK MIKAIL

Description
How to automate tasks to run at intervals on linux servers?
Additional details will be available after launching your challenge instance.

_Note:_ This challenge launches an instance on demand.

---

## Approach

The description of the challenge mentioned about `cron` jobs.

`Cron` is a time-based job scheduler in Unix-like operating systems, including Linux. It allows users to automate the execution of commands or scripts at specified intervals.

After I launch into the instance and ssh into the shell using the credentials provided. I `cd` into the root directory and search for the `cron` file.

## Solution

After few attempts, I have located `/etc/crontab` and using the `cat` command, it prompts me the flag.

> picoCTF{Sch3DUL7NG_T45K3_L1NUX_0bb95b71}
