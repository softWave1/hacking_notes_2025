# First Find

# Descripción 
Unzip this archive and find the file named 'uber-secret.txt'
- [Download zip file](https://artifacts.picoctf.net/c/501/files.zip)

# Solución 
## 1. Bash

``` bash
# Find the file and print it 
find files/ -name uber-secret.txt -exec cat {} \;
# Flag: picoCTF{f1nd_15_f457_ab443fd1}
```

# Notas adicionales 

# Referencias 
