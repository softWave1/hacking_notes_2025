# information

# Description
Files can always be changed in a secret way. Can you find the flag? [cat.jpg](https://mercury.picoctf.net/static/c28a959c5605d5f67480d5dd3a77f302/cat.jpg)
# Solution
-  Download the file
- Check metadata using ```exiftool``` 
- Copy the license field string because looks like a base64 string
- Get the flag with ```base64``` command
``` bash
wget https://mercury.picoctf.net/static/c28a959c5605d5f67480d5dd3a77f302/cat.jpg
exiftool cat.jpg 
ExifTool Version Number         : 12.40
File Name                       : cat.jpg
Directory                       : .
File Size                       : 858 KiB
File Modification Date/Time     : 2021:03:15 12:24:46-06:00
File Access Date/Time           : 2025:05:12 21:00:38-06:00
File Inode Change Date/Time     : 2025:05:12 21:09:04-06:00
File Permissions                : -rwxrwxrwx
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.02
Resolution Unit                 : None
X Resolution                    : 1
Y Resolution                    : 1
Current IPTC Digest             : 7a78f3d9cfb1ce42ab5a3aa30573d617
Copyright Notice                : PicoCTF
Application Record Version      : 4
XMP Toolkit                     : Image::ExifTool 10.80
License                         : cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9
Rights                          : PicoCTF
Image Width                     : 2560
Image Height                    : 1598
Encoding Process                : Baseline DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Image Size                      : 2560x1598
Megapixels                      : 4.1

echo "cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9" | base64 -d
picoCTF{the_m3tadata_1s_modified}

```

# References
- [Information medium by nicola.moro2312](https://medium.com/@nicola.moro2312/picoctf-information-b50b7db01eaf)
