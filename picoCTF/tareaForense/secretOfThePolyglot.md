# Secret of the Polyglot

# Description
The Network Operations Center (NOC) of your local institution picked up a suspicious file, they're getting conflicting information on what type of file it is. They've brought you in as an external expert to examine the file. Can you extract all the information from this strange file?Download the suspicious file [here](https://artifacts.picoctf.net/c_titan/9/flag2of2-final.pdf).
# Solution
-  In this challenge the flag was spitted into 2 parts for the first one I only need to open the file directly in this case a pdf and then with the tool ```foremost``` I found another file inside the previous file that contained the last part of the flag.

``` bash
open flag2of2-final.pdf
foremost flag2of2-final.pdf 
Processing: flag2of2-final.pdf
|*|
ls
flag2of2-final.pdf  output
cd output/
ls
audit.txt  png
cd png/
open 00000000.png
# Flag 
picoCTF{f1u3n7_1n_pn9_&_pdf_7f9bccd1}
```
