# money-ware

## Overview

**100 points**

Category: [General Skills](../)

Tags: `#cryptocurrency`

AUTHOR: JUNI19

DESCRIPTION
Flag format: `picoCTF{Malwarename}`
The first letter of the malware name should be capitalized and the rest lowercase.
Your friend just got hacked and has been asked to pay some bitcoins to `1Mz7153HMuxXTuR2R1t78mGSdzaAtNbBWX`. He doesn’t seem to understand what is going on and asks you for advice.
Can you identify what malware he’s being a victim of?

HINTS

- _Some crypto-currencies abuse databases exist; check them out!_
- _Maybe Google might help._

---

## Approach

Seems like it should be a challenge with some googling. After copy and pasting the bitcoin address `1Mz7153HMuxXTuR2R1t78mGSdzaAtNbBWX` into google, I clicked into an [article](https://www.cnbc.com/2017/06/28/ransomware-cyberattack-petya-bitcoin-payment.html) that discuss about the vulnerability called **Petya**, a type of ransomware.

## Solution

It is a straight forward challenge, hence

> picoCTF{Petya}
