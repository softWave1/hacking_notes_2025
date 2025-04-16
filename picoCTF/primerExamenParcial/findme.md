# findme

# Description
Help us test the form by submitting the username as test and password as test!
Additional details will be available after launching your challenge instance.
# Solution
After login in with the credentials given in the challenge in the browser bar the url change instantly but with any screen recorder I can record the exact time where the url is showed an take a screenshot of that later with an any ocr engine like ```tesseract``` I can catch the text of the image in this case there's an interesting code at the text because it's in ```base64``` after decoding it I realize that it's a part of the flag.
-  step one
``` bash
ls
imagen.png 
tesseract imagen.png salida
cat salida.txt 
© | GNotSecure  saturn.picoctf.net:50315/next-page/id=cGljbONURntwcm94aWVzX2Fs
echo "cGljbONURntwcm94aWVzX2Fs" | base64 -d
picl�TF{proxies_al
# The flag have some weird simbols but since I know the structure of the flag I can correct it by myself
picoCTF{proxies_al
```

- Analyzing the http request at the network page of the browser inspection tool I realize that in the header of one there's another id in the exact same coding than before so in the same way of the previous I just decode it and get the other part of the flag

```bash
GET /home HTTP/1.1
Host: saturn.picoctf.net:50315
User-Agent: Mozilla/5.0 (X11; Linux x86_64; rv:137.0) Gecko/20100101 Firefox/137.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: en-US,en;q=0.5
Accept-Encoding: gzip, deflate
DNT: 1
Sec-GPC: 1
Connection: keep-alive
Referer: http://saturn.picoctf.net:50315/next-page/id=bF90aGVfd2F5XzI1YmJhZTlhfQ==
Upgrade-Insecure-Requests: 1
If-None-Match: W/"7b1-0saSQV5P/nyzFi+aDsyr7qbJFk4"
Priority: u=0, i

echo "bF90aGVfd2F5XzI1YmJhZTlhfQ" | base64 -d
l_the_way_25bbae9a}

# Final flag
picoCTF{proxies_all_the_way_25bbae9a}
```

