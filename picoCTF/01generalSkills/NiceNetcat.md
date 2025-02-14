# Nice netcat...

# Descripción 

There is a nice program that you can talk to by using this command in a shell: `$ nc mercury.picoctf.net 22342`, but it doesn't speak English...
# Solución 

## 1. Python

```bash
# Previous fase to get more details about the flag
nc mercury.picoctf.net 22342 > encryptedFlag.txt
cat output.txt
```

``` python
with open('encryptedFlag.txt', 'r') as file:
    lines = file.readlines()

lines = [line.strip() for line in lines]

myFlag = ""

for l in lines:
    tempChar = chr(int(l))
    myFlag+=tempChar

print(myFlag)

#Output: picoCTF{g00d_k1tty!_n1c3_k1tty!_5fb5e51d}
#Flag: picoCTF{g00d_k1tty!_n1c3_k1tty!_5fb5e51d}
```


# Notas adicionales 

# Referencias 

