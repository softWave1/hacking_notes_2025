# c0rrupt

# Description
We found this [file](https://jupiter.challenges.picoctf.org/static/ab30fcb7d47364b4190a7d3d40edb551/mystery). Recover the flag.
# Solution
After downloading the file and using the ```file``` command I didn't get any information about the file but after using an hex editor I realized that It used to be a png file but it can't be oppened yet since it't corrupt so I'll made a set of changes into the file structure.

- First step change the header values to ``` 89 50 4E 47 0D 0A 1A 0A```.

-  Second step  changing the IHDR chunk into the right one from ``` 43 22 44 52```  to ``` 49 48 44 52``` that represent the letters I,H,D,R  in hexadecimal after checking out the file it can be opened yet.

- Third step  changing the  chunk pHYs  into the right one from ```AA```  to ```00``` but I can open it though. 

- Fourth step I change the IDAT from ```AB 44 45``` to ```49 44 41``` and from ``` AA AA ``` to ```00 00```  then after checking the integrity of the image with ```pngcheck``` It says that has no error so I can open it and get the flag written in the image.

```bash
# Flag : picoCTF{c0rrupt10n_1847995}
```

# References
- [picoCTF 2021 writeup 21 - Forensic - c0rrupt](https://www.youtube.com/watch?v=7zY4VkiWbBI&list=PLDo9DMLZyP6kTZ8Td37-LdbAx4-yNfHBl)
