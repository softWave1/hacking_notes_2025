# Big Zip

# Descripción 
Unzip this archive and find the flag.
- [Download zip file](https://artifacts.picoctf.net/c/504/big-zip-files.zip)

# Solución 
## 1. Bash

``` bash
# Getting the zip file 
wget https://artifacts.picoctf.net/c/504/big-zip-files.zip
# Unzip this archive 
unzip big-zip-files.zip

# Find the flag using grep 
grep -R pico big-zip-files

# Output: big-zip-files/folder_pmbymkjcya/folder_cawigcwvgv/folder_ltdayfmktr/folder_fnpfclfyee/whzxrpivpqld.txt:information on the record will last a billion years. Genes and brains and books encode picoCTF{gr3p_15_m4g1c_ef8790dc}

# Flag : picoCTF{gr3p_15_m4g1c_ef8790dc}
```

# Notas adicionales 

# Referencias 
