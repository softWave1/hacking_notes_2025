# Sleuthkit Intro

# Description
Download the disk image and use `mmls` on it to find the size of the Linux partition. Connect to the remote checker service to check your answer and get the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.[Download disk image](https://artifacts.picoctf.net/c/164/disk.img.gz)

Additional details will be available after launching your challenge instance.
# Solution
-  Download the disk of the image
-  Unzip disk image with ```gzip``` 
-  Use ```mmls``` on the image 
- Once I know the partitions and its sizes I could connect with net cat and get the answer.
- Finally after answer the question I get the flag.
``` bash
wget https://artifacts.picoctf.net/c/164/disk.img.gz
gzip -d disk.img.gz
mmls disk.img 
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000204799   0000202752   Linux (0x83)

nc saturn.picoctf.net 58075
What is the size of the Linux partition in the given disk image?
Length in sectors: 0000202752
0000202752
Great work!
picoCTF{mm15_f7w!}

```