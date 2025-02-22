#  PW Crack 2

# Descripción 
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/15/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/15/level2.flag.txt.enc) in the same directory too
# Solución 
## 1. Bash

``` bash
# Getting the needed files

wget https://artifacts.picoctf.net/c/15/level2.py https://artifacts.picoctf.net/c/15/level2.flag.txt.enc

# The password is visible in the code 

# Getting the password 
cat level1.py | grep "user_pw =="
# if( user_pw == chr(0x33) + chr(0x39) + chr(0x63) + chr(0x65)

# This time the password need to be decoded 
# Using python 
# print(chr(0x33) + chr(0x39) + chr(0x63) + chr(0x65))
# password : 39ce



# Running the code
python3 level2.py

# Input: 39ce
# Output: Welcome back... your flag, user:
# picoCTF{tr45h_51ng1ng_502ec42e}


# Flag: picoCTF{tr45h_51ng1ng_502ec42e}

```

# Notas adicionales 

# Referencias 
