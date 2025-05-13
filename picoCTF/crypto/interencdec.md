# interencdec 

# Description
Can you get the real meaning from this file.Download the file [here](https://artifacts.picoctf.net/c_titan/109/enc_flag).
# Solution


-  Using ```base64``` twice 
- Decode using Cesar code 

``` bash
cat enc_flag | base64 -d
b'd3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrX20wMjEyNzU4fQ=='
echo "d3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrX20wMjEyNzU4fQ==" | base64 -d
wpjvJAM{jhlzhy_k3jy9wa3k_m0212758}
# Tool 
https://www.dcode.fr/caesar-cipher
# Input 
wpjvJAM{jhlzhy_k3jy9wa3k_m0212758}
# Ouput
picoCTF{caesar_d3cr9pt3d_f0212758}
```
