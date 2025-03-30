# JaWTScratchpad

# Description
Check the admin scratchpad! `https://jupiter.challenges.picoctf.org/problem/58210/` or http://jupiter.challenges.picoctf.org:58210
# Solution

-  The website use JWT for admin authentication first off using cookie editor  I try to log in using any username and copy the jwt cookie and we save it to text file. 
``` bash
echo eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyIjoiSnVhbiJ9.DlLO_Ef3lVdAkZ1uFzyeabScd3-0bduv1hDNvdnDsTs > hash.txt
```

- Using the tool [John the ripper](https://github.com/openwall/john)  I use the word list rockyou.txt to get the password for the signature.

```bash
# Unzip zip file with the wordlist
sudo gzip -d /usr/share/wordlists/rockyou.txt.gz

# Trying to get the password
john hash.txt -w:/usr/share/wordlists/rockyou.txt 

#output 
ilovepico

#Flag 
picoCTF{jawt_was_just_what_you_thought_44c752f5}
```

-  Once I get the password for the signature I can paste it on the verify signature field , get the encoded text and paste in the cookie editor jwt field and get the flag.

# Additional notes
The jwt is not encrypted so it could be dangerous using it for sensitive data.
# References
- [Reference links](youtube.com)
