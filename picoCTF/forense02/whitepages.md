# WhitePages

# Description
I stopped using YellowPages and moved onto WhitePages... but [the page they gave me](https://jupiter.challenges.picoctf.org/static/74274b96fe966126a1953c80762af80d/whitepages.txt) is all blank!
# Solution
After downloading the file and try to open it with an ordinary text editor I face that it looks completely blank but using the ```file``` command I get more information about this text file , after that using the ```xxd``` command I figured it out that it uses two type of spaces the standard space and the Unicode using a python program that replaces this two types of spaces by its binary representation the output reveals the flag.
#### Python program

``` python
from pwn import *

with open("whitepages.txt", "rb") as bin_file:
    data = bytearray(bin_file.read()) 
    data = data.replace(b'\xe2\x80\x83', b'0')
    data = data.replace(b'\x20', b'1')
    data = data.decode("ascii")
    print unbits(data)


# Flag 
#picoCTF{not_all_spaces_are_created_equal_c54f27cd05c2189f8147cc6f5deb2e56}
```

# References
- [picoCTF 2019 writeup 20 - Forensic - WhitePages](https://www.youtube.com/watch?v=427HDV7tzow&list=PLDo9DMLZyP6kTZ8Td37-LdbAx4-yNfHBl)
