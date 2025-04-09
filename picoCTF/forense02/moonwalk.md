# m00nwalk

# Description

Decode this [message](https://jupiter.challenges.picoctf.org/static/d6fcea5e3c6433680ea4f914e24fab61/message.wav) from the moon.
# Solution

Using the tool ```qsstv``` that can be installed with ```apt get install qsstv``` I code decode the audio file , first off once the tool is installed I open it using the command  ```qsstv```  then I clicked up on the receive button that is located on the left upper corner , then I played the file and finally I get an image were the flag was written is important to select the right mode in order to get the flag in this case the mode was scottie 1 this was part of the hints on the challenge page.

![image ]( picoCTF/assets/image1.png "Image after the transmission")

``` bash
qsstv
paplay -d virtual-cable message.wav
# Flag:
picoCTF{beep_boop_im_in_space}
```
# References
- [Dvd848/CTFs m00nwalk ](https://github.com/Dvd848/CTFs/blob/master/2019_picoCTF/m00nwalk.md)
