# SansAlpha

# Description
The Multiverse is within your grasp! Unfortunately, the server that contains the secrets of the multiverse is in a universe where keyboards only have numbers and (most) symbols.
Additional details will be available after launching your challenge instance.

# Solution

-  After log in into the server trough ssh and trying some commands I get to know that I can use any common command at least it the common way

``` bash
❯ ssh -p 52097 ctf-player@mimas.picoctf.net
The authenticity of host '[mimas.picoctf.net]:52097 ([52.15.88.75]:52097)' can't be established.
ED25519 key fingerprint is SHA256:n/hDgUtuTTF85Id7k2fxmHvb6rrLrACHNM6xLZ46AqQ.
This host key is known by the following other names/addresses:
    ~/.ssh/known_hosts:26: [hashed name]
    ~/.ssh/known_hosts:28: [hashed name]
    ~/.ssh/known_hosts:29: [hashed name]
    ~/.ssh/known_hosts:30: [hashed name]
    ~/.ssh/known_hosts:31: [hashed name]
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[mimas.picoctf.net]:52097' (ED25519) to the list of known hosts.
ctf-player@mimas.picoctf.net's password: 
Welcome to Ubuntu 20.04.3 LTS (GNU/Linux 6.5.0-1016-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

SansAlpha$ ls
SansAlpha: Unknown character detected
SansAlpha$ cat
SansAlpha: Unknown character detected
SansAlpha$  

```

- Checking the server looks like the arithmetic , symbols  and the *wildcards* still working after trying some I get to know that there a directory where is the flag but I can show its contents. 

```bash
SansAlpha$ */*
bash: blargh/flag.txt: Permission denied

SansAlpha$ $((1+2))
bash: 3: command not found

SansAlpha$  
```

-  Since when a wildcard matches one single executable binary it will be interpreted as a command using this to my advantage I can build a wildcard that matches the ```base64``` command to later parse it into text and get the flag

```bash
SansAlpha$ /*/???[!_]64 */????.*
cmV0dXJuIDAgcGljb0NURns3aDE1X211MTcxdjNyNTNfMTVfbTRkbjM1NV84YjNkODNhZH0=
echo "cmV0dXJuIDAgcGljb0NURns3aDE1X211MTcxdjNyNTNfMTVfbTRkbjM1NV84YjNkODNhZH0=" | base64 -d
return 0 picoCTF{7h15_mu171v3r53_15_m4dn355_8b3d83ad}
```
# Additional notes

Even if it's rare use wildcards in this particular way it's a good practice using an ```echo``` before any wildcard where We are not so sure about the files that could be compromised. 
# References
- [PicoCTF SansAlpha Writeup](https://lavafroth.is-a.dev/post/picoctf-sansalpha-writeup/)
