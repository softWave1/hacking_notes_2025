# Plumbing

# Descripción 
Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag? Connect to jupiter.challenges.picoctf.org 4427.

# Solución 
## 1. Bash (netcat(nc))

``` bash
# Redirecting nc output to a text file 
nc jupiter.challenges.picoctf.org 4427 > output.txt

# Filtering flag from a text file
cat output.txt | grep pico

# output:picoCTF{digital_plumb3r_5ea1fbd7}
# Flag:picoCTF{digital_plumb3r_5ea1fbd7}

```
# Notas adicionales 

# Referencias 
