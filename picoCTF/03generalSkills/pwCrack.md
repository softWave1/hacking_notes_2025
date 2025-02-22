# PW Crack 1

# Descripción 
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/12/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/12/level1.flag.txt.enc) in the same directory too.
# Solución 
## 1. Bash

``` bash
# Getting the needed files

wget https://artifacts.picoctf.net/c/12/level1.py https://artifacts.picoctf.net/c/12/level1.flag.txt.enc

# The password is visible in the code 

# Getting the password 
cat level1.py | grep "user_pw =="
# if( user_pw == "8713"):

# Running the code
python3 level1.py

# Input: 8713
# Output: Welcome back... your flag, user:
# picoCTF{545h_r1ng1ng_1b2fd683}

# Flag: picoCTF{545h_r1ng1ng_1b2fd683}

```

# Notas adicionales 

# Referencias 
