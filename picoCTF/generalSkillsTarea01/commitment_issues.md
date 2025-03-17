# Commitment Issues

# Description
I accidentally wrote the flag down. Good thing I deleted it!You download the challenge files here:
- [challenge.zip](https://artifacts.picoctf.net/c_titan/75/challenge.zip)
# Solution

-  After unzip the file and see the git log I needed to got back to the previous commit where the flag was created and finally get the flag.

``` bash
git log

commit 3899edb7f3110d613c72ad40083fd8feeef703d0 (HEAD -> master)
Author: picoCTF <ops@picoctf.com>
Date:   Sat Mar 9 21:09:58 2024 +0000

    remove sensitive info

commit 6603cb4ff0c4ea293798c03a32e0d78d5ab12ca2
Author: picoCTF <ops@picoctf.com>
Date:   Sat Mar 9 21:09:58 2024 +0000

    create flag
    
git reset --hard HEAD~1
HEAD is now at 6603cb4 create flag

cat message.txt 
picoCTF{s@n1t1z3_9539be6b}

```
