# Wave a Flag
# Descripción 
Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/a14be2648c73e3cda5fc8490a2f476af/warm) has extraordinarily helpful information...
# Solución 
## 1. Bash

``` bash
# Getting the binary file
wget https://mercury.picoctf.net/static/a14be2648c73e3cda5fc8490a2f476af/warm

# Add permissions 
chmod +x warm

# Executing the file with the help flag
./warm -h

#Output: Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_755f3544}
#Flag: picoCTF{b1scu1ts_4nd_gr4vy_755f3544}
```
# Notas adicionales 

# Referencias 
