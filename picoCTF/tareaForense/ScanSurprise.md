# Scan Surprise

# Description
I've gotten bored of handing out flags as text. Wouldn't it be cool if they were an image instead?
You can download the challenge files here:
- [challenge.zip](https://artifacts.picoctf.net/c_atlas/3/challenge.zip)
# Solution
-  Download file
- Unzip file
- Inside the path home/ctf-player/drop-in/ there's an image file that contains a qr code so I  use the command ```zbarimg``` but it could be scanned it manually with any phone.

``` bash
unzip challenge.zip
tree home/
home/
└── ctf-player
    └── drop-in
        └── flag.png
cd home/ctf-player/drop-in
zbarimg flag.png 
QR-Code:picoCTF{p33k_@_b00_a81f0a35}
scanned 1 barcode symbols from 1 images in 0 seconds
```

