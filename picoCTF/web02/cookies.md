# Cookies

# Description
Who doesn't love cookies? Try to figure out the best one. [http://mercury.picoctf.net:21485/](http://mercury.picoctf.net:21485/)
# Solution

-  We iterate over a loop sending cookies until we found the flag 
``` bash
for i in {1..30}; do curl -s  http://mercury.picoctf.net:21485/check -H "Cookie: name=$i" | grep pico; done;

# Flag
picoCTF{3v3ry1_l0v3s_c00k135_94190c8a}
```

