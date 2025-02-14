# GlitchCat

# Descripción 

Our flag printing service has started glitching!
Additional details will be available after launching your challenge instance.

# Solución 
## 1. Python

```bash
# Previous fase to get more details about the flag
nc saturn.picoctf.net 53725 > output.txt
cat output.txt
# output:'picoCTF{gl17ch_m3_n07_' + chr(0x62) + chr(0x64) + chr(0x61) + chr(0x36) + chr(0x38) + chr(0x66) + chr(0x37) + chr(0x35) + '}'
```

``` python

print('picoCTF{gl17ch_m3_n07_' + chr(0x62) + chr(0x64) + chr(0x61) + chr(0x36) + chr(0x38) + chr(0x66) + chr(0x37) + chr(0x35) + '}')


# output: picoCTF{gl17ch_m3_n07_bda68f75}
#Flag: picoCTF{gl17ch_m3_n07_bda68f75}

```
# Notas adicionales 

# Referencias 
