# macroHardWeakEdge

# Description
I've hidden a flag in this file. Can you find it? [Forensics is fun.pptm](https://mercury.picoctf.net/static/3944a59474f9f676942282c50b9c3675/Forensics%20is%20fun.pptm)
# Solution
-  First off I need to unzip the file once its unziped I can see that there some files and folders and there's a folder called  ```hidden``` that's quite suspicious  after seeing the contents of the folder there's a text file with some text in base64 so using the command base64 but the output is not a flag but after using the command tr -d to delete the spaces I was able to get the flag.

``` bash
unzip unzip Forensics\ is\ fun.pptm
tree 
.
├── [Content_Types].xml
├── docProps
│   ├── app.xml
│   ├── core.xml
│   └── thumbnail.jpeg
├── Forensics is fun.pptm
├── ppt
│   ├── presentation.xml
│   ├── presProps.xml
│   ├── _rels
│   │   └── presentation.xml.rels
│   ├── slideLayouts
│   │   ├── _rels
│   │   │   ├── slideLayout10.xml.rels
│   │   │   ├── slideLayout11.xml.rels
│   │   │   ├── slideLayout1.xml.rels
│   │   │   ├── slideLayout2.xml.rels
│   │   │   ├── slideLayout3.xml.rels
│   │   │   ├── slideLayout4.xml.rels
│   │   │   ├── slideLayout5.xml.rels
│   │   │   ├── slideLayout6.xml.rels
│   │   │   ├── slideLayout7.xml.rels
│   │   │   ├── slideLayout8.xml.rels
│   │   │   └── slideLayout9.xml.rels
│   │   ├── slideLayout10.xml
│   │   ├── slideLayout11.xml
│   │   ├── slideLayout1.xml
│   │   ├── slideLayout2.xml
│   │   ├── slideLayout3.xml
│   │   ├── slideLayout4.xml
│   │   ├── slideLayout5.xml
│   │   ├── slideLayout6.xml
│   │   ├── slideLayout7.xml
│   │   ├── slideLayout8.xml
│   │   └── slideLayout9.xml
│   ├── slideMasters
│   │   ├── hidden
│   │   ├── _rels
│   │   │   └── slideMaster1.xml.rels
│   │   └── slideMaster1.xml
│   ├── slides
│   │   ├── _rels
│   │   │   ├── slide10.xml.rels
│   │   │   ├── slide11.xml.rels
│   │   │   ├── slide12.xml.rels
│   │   │   ├── slide13.xml.rels
│   │   │   ├── slide14.xml.rels
│   │   │   ├── slide15.xml.rels
│   │   │   ├── slide16.xml.rels
│   │   │   ├── slide17.xml.rels
│   │   │   ├── slide18.xml.rels
│   │   │   ├── slide19.xml.rels
│   │   │   ├── slide1.xml.rels
│   │   │   ├── slide20.xml.rels
│   │   │   ├── slide21.xml.rels
│   │   │   ├── slide22.xml.rels
│   │   │   ├── slide23.xml.rels
│   │   │   ├── slide24.xml.rels
│   │   │   ├── slide25.xml.rels
│   │   │   ├── slide26.xml.rels
│   │   │   ├── slide27.xml.rels
│   │   │   ├── slide28.xml.rels
│   │   │   ├── slide29.xml.rels
│   │   │   ├── slide2.xml.rels
│   │   │   ├── slide30.xml.rels
│   │   │   ├── slide31.xml.rels
│   │   │   ├── slide32.xml.rels
│   │   │   ├── slide33.xml.rels
│   │   │   ├── slide34.xml.rels
│   │   │   ├── slide35.xml.rels
│   │   │   ├── slide36.xml.rels
│   │   │   ├── slide37.xml.rels
│   │   │   ├── slide38.xml.rels
│   │   │   ├── slide39.xml.rels
│   │   │   ├── slide3.xml.rels
│   │   │   ├── slide40.xml.rels
│   │   │   ├── slide41.xml.rels
│   │   │   ├── slide42.xml.rels
│   │   │   ├── slide43.xml.rels
│   │   │   ├── slide44.xml.rels
│   │   │   ├── slide45.xml.rels
│   │   │   ├── slide46.xml.rels
│   │   │   ├── slide47.xml.rels
│   │   │   ├── slide48.xml.rels
│   │   │   ├── slide49.xml.rels
│   │   │   ├── slide4.xml.rels
│   │   │   ├── slide50.xml.rels
│   │   │   ├── slide51.xml.rels
│   │   │   ├── slide52.xml.rels
│   │   │   ├── slide53.xml.rels
│   │   │   ├── slide54.xml.rels
│   │   │   ├── slide55.xml.rels
│   │   │   ├── slide56.xml.rels
│   │   │   ├── slide57.xml.rels
│   │   │   ├── slide58.xml.rels
│   │   │   ├── slide5.xml.rels
│   │   │   ├── slide6.xml.rels
│   │   │   ├── slide7.xml.rels
│   │   │   ├── slide8.xml.rels
│   │   │   └── slide9.xml.rels
│   │   ├── slide10.xml
│   │   ├── slide11.xml
│   │   ├── slide12.xml
│   │   ├── slide13.xml
│   │   ├── slide14.xml
│   │   ├── slide15.xml
│   │   ├── slide16.xml
│   │   ├── slide17.xml
│   │   ├── slide18.xml
│   │   ├── slide19.xml
│   │   ├── slide1.xml
│   │   ├── slide20.xml
│   │   ├── slide21.xml
│   │   ├── slide22.xml
│   │   ├── slide23.xml
│   │   ├── slide24.xml
│   │   ├── slide25.xml
│   │   ├── slide26.xml
│   │   ├── slide27.xml
│   │   ├── slide28.xml
│   │   ├── slide29.xml
│   │   ├── slide2.xml
│   │   ├── slide30.xml
│   │   ├── slide31.xml
│   │   ├── slide32.xml
│   │   ├── slide33.xml
│   │   ├── slide34.xml
│   │   ├── slide35.xml
│   │   ├── slide36.xml
│   │   ├── slide37.xml
│   │   ├── slide38.xml
│   │   ├── slide39.xml
│   │   ├── slide3.xml
│   │   ├── slide40.xml
│   │   ├── slide41.xml
│   │   ├── slide42.xml
│   │   ├── slide43.xml
│   │   ├── slide44.xml
│   │   ├── slide45.xml
│   │   ├── slide46.xml
│   │   ├── slide47.xml
│   │   ├── slide48.xml
│   │   ├── slide49.xml
│   │   ├── slide4.xml
│   │   ├── slide50.xml
│   │   ├── slide51.xml
│   │   ├── slide52.xml
│   │   ├── slide53.xml
│   │   ├── slide54.xml
│   │   ├── slide55.xml
│   │   ├── slide56.xml
│   │   ├── slide57.xml
│   │   ├── slide58.xml
│   │   ├── slide5.xml
│   │   ├── slide6.xml
│   │   ├── slide7.xml
│   │   ├── slide8.xml
│   │   └── slide9.xml
│   ├── tableStyles.xml
│   ├── theme
│   │   └── theme1.xml
│   ├── vbaProject.bin
│   └── viewProps.xml
└── _rels
# First try
echo "$(cat hidden)"|base64
WiBtIHggaCBaIHogbyBnIGMgRyBsIGogYiAwIE4gVSBSIG4gdCBFIE0gVyBSIGYgZCBWIDkgciBi
IGogQiAzIFggMyBCIHcgZCBIIE4gZiBjIGwgOSA2IE0gWCBBIDEgZiBRCg==
# Second try
echo "$(cat hidden)" | tr -d " " | base64 -d
flag: picoCTF{D1d_u_kn0w_ppts_r_z1p5}
```
# References
- [picoCTF 2021 writeup 28 - Forensic - MacroHard WeakEdge](https://www.youtube.com/watch?v=CsCeOp9PFGs&list=PLDo9DMLZyP6kTZ8Td37-LdbAx4-yNfHBl&index=28)
