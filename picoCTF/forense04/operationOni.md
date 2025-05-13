# Operation Oni

# Description
Download this disk image, find the key and log into the remote machine.
Note: if you are using the webshell, download and extract the disk image into /tmp not your home directory.
Additional details will be available after launching your challenge instance.
# Solution
 - Download and unzip image file
 - Explore root files and then .ssh directory
 - Copy the keyfile into another file
 - Give the needed permissions using ```chmod``` 
 - Connect through ssh  
``` bash
wget https://artifacts.picoctf.net/c/70/disk.img.gz 
gunzip disk.img.gz
mmls disk.img 
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000206847   0000204800   Linux (0x83)
003:  000:001   0000206848   0000471039   0000264192   Linux (0x83)
fls disk.img -o 206848 470  
r/r 2344:	.ash_history
d/d 3916:	.ssh
icat disk.img -o 206848  2345 > keyfil
chmod 600 keyfile 
ssh -i keyfile -p 53728 ctf-player@saturn.picoctf.net
The authenticity of host '[saturn.picoctf.net]:53728 ([13.59.203.175]:53728)' can't be established.
ED25519 key fingerprint is SHA256:XBSvB1lk28EctsAVdKJtsl0A7C5bonqPrvHCYH8aEy4.
This host key is known by the following other names/addresses:
    ~/.ssh/known_hosts:37: [hashed name]
    ~/.ssh/known_hosts:38: [hashed name]
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[saturn.picoctf.net]:53728' (ED25519) to the list of known hosts.
Welcome to Ubuntu 20.04.5 LTS (GNU/Linux 6.5.0-1023-aws x86_64)

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

ctf-player@challenge:~$ ls
flag.txt
ctf-player@challenge:~$ cat flag.txt 
picoCTF{k3y_5l3u7h_b5066e83}

```