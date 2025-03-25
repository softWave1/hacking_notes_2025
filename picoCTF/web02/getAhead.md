# Get a head

# Description
#### Description

Find the flag being held on this server to get ahead of the competition [http://mercury.picoctf.net:28916/](http://mercury.picoctf.net:28916/)
# Solution

-  Use curl command to send an https request metod diferent to Get and post (HEAD) to the server

``` bash
curl -I http://mercury.picoctf.net:28916/index.php
HTTP/1.1 200 OK
flag: picoCTF{r3j3ct_th3_du4l1ty_70bc61c4}
Content-type: text/html; charset=UTF-8
```
