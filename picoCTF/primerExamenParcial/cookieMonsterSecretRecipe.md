# Cookie Monster Secret Recipe

# Description
Cookie Monster has hidden his top-secret cookie recipe somewhere on his website. As an aspiring cookie detective, your mission is to uncover this delectable secret. Can you outsmart Cookie Monster and find the hidden recipe?You can access the Cookie Monster [here](http://verbal-sleep.picoctf.net:54630/) and good luck
# Solution
- After trying to log in with any credentials like ```admin``` ```admin```  the website ask me to check my cookies and after doing this with  the add-on cookie editor the cookie is text in base 64 so I only need to copy the cookie content and after that using the ```base64``` command to get the flag.

``` bash
# Cookie content
# Name : secret_recipe
# Value : cGljb0NURntjMDBrMWVfbTBuc3Rlcl9sMHZlc19jMDBraWVzX0U2MzRERkJCfQ%3D%3D

echo "cGljb0NURntjMDBrMWVfbTBuc3Rlcl9sMHZlc19jMDBraWVzX0U2MzRERkJCfQ%3D%3D" | base64 -d
picoCTF{c00k1e_m0nster_l0ves_c00kies_E634DFBB}
```
