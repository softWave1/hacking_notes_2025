# Operation Orchid

# Description
Download this disk image and find the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download compressed disk image](https://artifacts.picoctf.net/c/212/disk.flag.img.gz)
# Solution

-  Download file
-  Unzip it using ```gunzip```
-  List partitions 
- Explore the partition using ```fls``` and using ```grep``` I filter the search looking for a flag file.
- Once I found the flag file I can show its contents using ```icat``` this time there's was not any readable output with the command and because of the name of the file I could bet its encrypted
- Since the flag is encrypted I copy the flag file into a directory for later manipulation.
- Once I copy the flag file once again using ```icat``` and redirection I could see the command history and discover the algorithm used for the flag.
- Once I know the encryption algorithm I use the command ``` openssl``` for see the flag file contents.

``` bash
wget https://artifacts.picoctf.net/c/212/disk.flag.img.gz
gunzip disk.flag.img.gz
mmls disk.flag.img 
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000206847   0000204800   Linux (0x83)
003:  000:001   0000206848   0000411647   0000204800   Linux Swap / Solaris x86 (0x82)
004:  000:002   0000411648   0000819199   0000407552   Linux (0x83)
fls disk.flag.img -o 411648 -r | grep flag
r/r * 1876(realloc):	flag.txt
r/r 1782:	flag.txt.enc
icat disk.flag.img -o 411648 2371
icat disk.flag.img -o 411648 2371 > flag.txt
fls disk.flag.img -o 411648 -r | grep history
r/r 1875:	.ash_history
Salted__0��!�-6V����0�U��l��&�:�pj_1�0�|�h
                                          �Ȥ7� ���؎$�
icat disk.flag.img -o 411648 1875
touch flag.txt
nano flag.txt 
apk get nano
apk --help
apk add nano
nano flag.txt 
openssl
openssl aes256 -salt -in flag.txt -out flag.txt.enc -k unbreakablepassword1234567
shred -u flag.txt
ls -al
halt
openssl aes256 -salt -d -in flag.txt.enc -out flag1.txt -k unbreakablepassword1234567
openssl aes256 -salt -d -in flag.txt -out flag1.txt -k unbreakablepassword1234567
*** WARNING : deprecated key derivation used.
Using -iter or -pbkdf2 would be better.
bad decrypt
40D781E1F8770000:error:1C800064:Provider routines:ossl_cipher_unpadblock:bad decrypt:../providers/implementations/ciphers/ciphercommon_block.c:124:
cat flag1.txt 
picoCTF{h4un71ng_p457_0a710765}
```