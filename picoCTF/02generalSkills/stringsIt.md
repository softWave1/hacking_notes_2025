# Strings it

# Descripción 

Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/94d00153b0057d37da225ee79a846c62/strings) without running it?
# Solución 
## 1. Bash (strings)

``` bash

# Getting the text file 
wget https://jupiter.challenges.picoctf.org/static/94d00153b0057d37da225ee79a846c62/strings

# Filtering the printable characters 
strings strings | grep pico

# Output : picoCTF{5tRIng5_1T_d66c7bb7}
# Flag: picoCTF{5tRIng5_1T_d66c7bb7}
```
# Notas adicionales 

# Referencias 
