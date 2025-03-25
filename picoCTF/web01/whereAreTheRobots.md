# where are the robots

# Description
Can you find the robots? `https://jupiter.challenges.picoctf.org/problem/36474/` ([link](https://jupiter.challenges.picoctf.org/problem/36474/)) or http://jupiter.challenges.picoctf.org:36474
# Solution

-  Try to access to the robots.txt file 

``` bash
# Go the robots.txt file
http://jupiter.challenges.picoctf.org:36474/robots.txt
# output
User-agent: *
Disallow: /477ce.html
```

- The output doesn't have the flag but it has a path after going that path the flag is reveled

```bash
# Path
http://jupiter.challenges.picoctf.org:36474/477ce.html

# output
picoCTF{ca1cu1at1ng_Mach1n3s_477ce}
```
