# Time Machine

# Description
What was I last working on? I remember writing a note to help me remember...You can download the challenge files here:
- [challenge.zip](https://artifacts.picoctf.net/c_titan/66/challenge.zip)
# Solution

-  After downloading and unzip the zip file i found out that the flag is embedded in the git log 

``` bash
git log
commit 3339c144a0c78dc2fbd3403d2fb37d3830be5d94 (HEAD -> master)
Author: picoCTF <ops@picoctf.com>
Date:   Sat Mar 9 21:10:22 2024 +0000

    picoCTF{t1m3m@ch1n3_d3161c0f}

```

