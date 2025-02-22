# Serpentine

# Descripción 
Find the flag in the Python script [Download Python script](https://artifacts.picoctf.net/c/35/serpentine.py)
# Solución 
## 1. Bash

``` bash
# Getting the python code
wget https://artifacts.picoctf.net/c/35/serpentine.py

# When running the code the function for printing the flag is missplaced
# we need to change just a line
```

``` python
# Before fix: print('\nOops! I must have misplaced the print_flag function! Check my source code!\n\n')

# After fix: print_flag()

# Flag: picoCTF{7h3_r04d_l355_7r4v3l3d_ae0b80bd}
```
# Notas adicionales 

# Referencias 
