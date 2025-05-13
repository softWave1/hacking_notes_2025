# hideme

# Description
Every file gets a flag.The SOC analyst saw one image been sent back and forth between two people. They decided to investigate and found out that there was more than what meets the eye [here](https://artifacts.picoctf.net/c/256/flag.png).
# Solution


-  This image have some images inside I only explore the directories and open the image until I get the flag in the next section there's some of the commands I used:

``` bash
 foremost flag.png 
Processing: flag.png
|foundat=secret/UT	
foundat=secret/flag.pngUT	
*|
cd output/
ls
audit.txt  png  zip
cd zip/
ls
00000077.zip
unzip 00000077.zip 
Archive:  00000077.zip
	creating: secret/
	inflating: secret/flag.png 
cd secret/
ls
flag.png
open flag.png 
# Flag
picoCTF{Hiddinng_An_imag3_within_@n_ima9e_85e04ab8}
```
