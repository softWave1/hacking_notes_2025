# PW Crack 3

# Descripción 
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/18/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/18/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/18/level3.hash.bin) in the same directory too.There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.
# Solución 
## 1. Bash

``` bash
# Getting the needed files
wget https://artifacts.picoctf.net/c/18/level3.py https://artifacts.picoctf.net/c/18/level3.flag.txt.enc https://artifacts.picoctf.net/c/18/level3.hash.bin

# The password is visible in the code but there's 7 possible solutions 
# Adding a function for printing the right password 
```

``` python
def printPassword():
	for i in pos_pw_list:
		if (hash_pw(i) == correct_pw_hash):
			print(i)
```

``` bash 
# Running the code
python3 level3.py

# Code output: 
2295
Please enter correct password for flag:2295

# Input:2295 
# Output: Welcome back... your flag, user:
# picoCTF{m45h_fl1ng1ng_6f98a49f}

# Flag: picoCTF{m45h_fl1ng1ng_6f98a49f}
```
# Notas adicionales 

# Referencias 
