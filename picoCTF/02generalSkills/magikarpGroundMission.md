# Magikarp Ground Mission 

# Descripción 
Do you know how to move between directories and read files in the shell? Start the container, `ssh` to it, and then `ls` once connected to begin. Login via `ssh` as `ctf-player` with the password, `481e7b14`
# Solución 
## 1. Bash

``` bash
# Show files 
ls
1of3.flag.txt  instructions-to-2of3.txt
# Cat first part of the flag and instructions to the next one 
cat 1of3.flag.txt instructions-to-2of3.txt 
picoCTF{xxsh_
Next, go to the root of all things, more succinctly `/`
# Change to the root directory
cd /
# Show files 
ls
2of3.flag.txt  boot  etc   instructions-to-3of3.txt  lib64  mnt  proc  run   srv  tmp  var
bin	       dev   home  lib			     media  opt  root  sbin  sys  usr
# Cat second part of the flag and instructions to the last one
cat 2of3.flag.txt instructions-to-3of3.txt 
0ut_0f_\/\/4t3r_

# Change  to home directory
Lastly, ctf-player, go home... more succinctly `~`
cd ~
# Show files 
ls
3of3.flag.txt  drop-in
# Show last part of the flag
cat 3of3.flag.txt 
1118a9a4}

# Flag : picoCTF{xxsh_0ut_0f_\/\/4t3r_1118a9a4}
```

# Notas adicionales 

# Referencias 
