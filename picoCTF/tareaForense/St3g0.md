# St3g0

# Description
Download this image and find the flag.
- [Download image](https://artifacts.picoctf.net/c/217/pico.flag.png)
# Solution

-  Use ```zteg``` into the image file.

``` bash
zsteg -a pico.flag.png 
b1,r,lsb,xy         .. text: "~__B>VG?G@"
b1,rgb,lsb,xy       .. text: "picoCTF{7h3r3_15_n0_5p00n_a9a181eb}$t3g0"

```

