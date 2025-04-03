# Extensions

# Description
This is a really weird text file [TXT](https://jupiter.challenges.picoctf.org/static/e7e5d188621ee705ceeb0452525412ef/flag.txt)? Can you find the flag?
# Solution
First off after using the command file I get to know that is a png file so I change the file extension to png and then I use the tool [Tesseract](https://github.com/tesseract-ocr/tesseract?tab=readme-ov-file#about) for extracting the flag easier and don't need to write it down manually.
-  step one
``` bash
# know file type
file flag.txt
# output 
flag.txt: PNG image data, 1697 x 608, 8-bit/color RGB, non-interlaced

# Change file extension
mv flag.txt flag.png

# extract the text in the image and show it 
tesseract flag.png output; cat output.txt

# output 
Tesseract Open Source OCR Engine v4.1.1 with Leptonica
picoCTF{now_you_know_about_extensions}
```
