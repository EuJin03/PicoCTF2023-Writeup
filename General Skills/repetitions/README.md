# repetitions

## Overview

**100 points**

Category: [General Skills](../)

Tags: `#base64`

AUTHOR: THEONESTE BYAGUTANGAZA

DESCRIPTION
Can you make sense of this file?
Download the file [here](./enc_flag).

HINTS

- _Multiple decoding is always good._

---

## Solution

Seems like it is encoded using `base64` encoder. I attempted by throwing the entire string from the [file](./enc_flag) provided into [CyberChef](https://gchq.github.io/CyberChef/). However, it returns me some giberrish strings.
Uh oh, after reading the hint again, I dump the decoded string in the decoder and cycle it again until the output returns me a plaintext which is the answer

> picoCTF{...<redacted>...}
