# flags are stepic 

# Description
A group of underground hackers might be using this legit site to communicate. Use your forensic techniques to uncover their message

Additional details will be available after launching your challenge instance.
# Solution
-  Look out for the country that doesn't exist
-  The line containing the country that doesn't exist  it's an image that could be downloaded using ```wget``` 
- Using ```stepic``` I get the flag
 
``` bash
# Suspicious line
{ name: "Upanzi, Republic The",img: "flags/upz.png", style:"width: 120px!important; height: 90px!important;" },
wget http://standard-pizzas.picoctf.net:49873/flags/upz.png
stepic -i upz.png -d
picoCTF{fl4g_h45_fl4g4a37da4c}
```
