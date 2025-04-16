# HashingJobApp

# Description
If you want to hash with the best, beat this test!
Additional details will be available after launching your challenge instance.
# Solution
In this challenge there are some text examples that I have to parse using a hashing algorithm (md5)  so using the command echo and filtering with a pipe trough the ```md5sum``` command I get the needed input to accomplish the challenge and finally get the flag.

-  Game play
``` bash
Please md5 hash the text between quotes, excluding the quotes: 'hairballs'
Answer: 
360927e98748b8675251a4a68b637b4b
360927e98748b8675251a4a68b637b4b
Correct.
Please md5 hash the text between quotes, excluding the quotes: 'Babe Ruth'
Answer: 
3875acc0c1561d949c39685e96b9a4bb
3875acc0c1561d949c39685e96b9a4bb
Correct.
Please md5 hash the text between quotes, excluding the quotes: 'the sunrise'
Answer: 
3652f115c238da1f79187d39b64e3fa2
3652f115c238da1f79187d39b64e3fa2
Correct.
picoCTF{4ppl1c4710n_r3c31v3d_bf2ceb02}

```

- Commands used 
```bash
echo -n "hairballs"|md5sum
echo -n "Babe Ruth"|md5sum
echo -n "the sunrise"|md5sum
```

