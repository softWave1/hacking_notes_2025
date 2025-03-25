# Scavenger Hunt

# Description
There is some interesting information hidden around this site http://mercury.picoctf.net:27278/. Can you find it?
# Solution
We need to look up for the different parts of the flag in the website 

-  First place the source code 
``` bash
# URL
view-source:http://mercury.picoctf.net:27278/
# Flag 
picoCTF{t
```

- Second place the css file

```bash
# URL 
view-source:http://mercury.picoctf.net:27278/mycss.css
# Flag
h4ts_4_l0
```

-  Third place the robots.txt file

```bash
# URL
http://mercury.picoctf.net:27278/robots.txt
# Third flag
t_0f_pl4c
```

- Fourth place 
```bash
# URL
http://mercury.picoctf.net:27278/.htaccess
# Flag
3s_2_lO0k
```

-  Fifth place 
```bash
# URL
http://mercury.picoctf.net:27278/.DS_Store
# Flag 
_a69684fd}
```

- Final flag
```picoCTF{th4ts_4_l0t_0f_pl4c3s_2_lO0k_a69684fd}```

