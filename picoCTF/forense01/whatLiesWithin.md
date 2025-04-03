# What Lies Within 

# Description
There's something in the [building](https://jupiter.challenges.picoctf.org/static/011955b303f293d60c8116e6a4c5c84f/buildings.png). Can you retrieve the flag?
# Solution
Using the tool ```Zsteg``` I could looked up for hidden information on image files and get the flag also I use grep for filtering the flag.

``` bash
zsteg -a buildings.png | grep pico

# Output
b1,rgb,lsb,xy       .. text: "picoCTF{h1d1ng_1n_th3_b1t5}"

# Flag
picoCTF{h1d1ng_1n_th3_b1t5}
```
