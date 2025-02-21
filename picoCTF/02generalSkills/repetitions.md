# Repetition

# Descripción 
Can you make sense of this file?
Download the file [here](https://artifacts.picoctf.net/c/474/enc_flag).
# Solución 
## 1. Bash

``` bash
cat enc_flag | base64 -d| base64 -d | base64 -d | base64 -d| base64 -d| base64 -d

# Flag: picoCTF{base64_n3st3d_dic0d!n8_d0wnl04d3d_3f81f7be}
```

# Notas adicionales 

# Referencias 
