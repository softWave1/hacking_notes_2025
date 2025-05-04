# MatryoshkaDoll

# Description
Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one? Image: [this](https://mercury.picoctf.net/static/2978e1270538613cd8181c7b0dabe9bd/dolls.jpg)
# Solution
After checking the image using ```binwalk``` I found out that there's another zip file inside the image so I extracted using ```binwalk``` once I uncompressed the zip file inside it has another image with the exact same structure so I repeated this method until I reach the last image and the flag.

``` bash
binwalk -e dolls.jpg 
cd _dolls.jpg.extracted
binwalk -e 2_c.jpg
cd _2_c.jpg.extracted
binwalk 3_c.jpg 3_c.jpg
binwalk -e 3_c.jpg
cd _3_c.jpg.extracted
binwalk -e 4_c.jpg 
cd _4_c.jpg.extracted/
cat flag.txt
picoCTF{4cf7ac000c3fb0fa96fb92722ffb2a32} 
```
# References
- [picoCTF 2021 writeup 26 - Forensic - Matryoshka doll](https://www.youtube.com/watch?v=NkbtA7x5aVI&list=PLDo9DMLZyP6kTZ8Td37-LdbAx4-yNfHBl&index=26)
