# Tab, Tab, Attack

# Descripción 
Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames: [Addadshashanammu.zip](https://mercury.picoctf.net/static/3afd18a65e42b80526aa87f9766c588b/Addadshashanammu.zip)
# Solución 
## 1. Bash

``` bash
# Getting the zip file
wget https://mercury.picoctf.net/static/3afd18a65e42b80526aa87f9766c588b/Addadshashanammu.zip

# Unzip the zip file
unzip Addadshashanammu.zip

# Filtering the printable characters 
string fang-of-haynekhtnamet | grep pico

# Output: *ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_d32e018c}
# Flag : picoCTF{l3v3l_up!_t4k3_4_r35t!_d32e018c}
```

# Notas adicionales 
En este reto se utilliza demaciado la tecla "tab" para poder llegar hasta el final de los directorios descomprimidos.
# Referencias 
