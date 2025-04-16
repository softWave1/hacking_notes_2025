# Python Wrangling

# Description
Python scripts are invoked kind of like programs in the Terminal... Can you run [this Python script](https://mercury.picoctf.net/static/0bf545252b5120845e3b568b9ad0277e/ende.py) using [this password](https://mercury.picoctf.net/static/0bf545252b5120845e3b568b9ad0277e/pw.txt) to get [the flag](https://mercury.picoctf.net/static/0bf545252b5120845e3b568b9ad0277e/flag.txt.en)?
# Solution
-  After downloading the files I only run the python script using the -d flag into the flag.txt.en file and paste the password to get the flag.

``` bash
cat pw.txt 
6008014f6008014f6008014f6008014f
python3 ende.py
Usage: ende.py (-e/-d) [file]

# The right way
python3 ende.py -d flag.txt.en 
Please enter the password:6008014f6008014f6008014f6008014f
picoCTF{4p0110_1n_7h3_h0us3_6008014f}
```
