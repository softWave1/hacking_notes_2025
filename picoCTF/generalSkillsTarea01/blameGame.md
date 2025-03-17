# Blame Game

# Description
Someone's commits seems to be preventing the program from working. Who is it?You can download the challenge files here:
- [challenge.zip](https://artifacts.picoctf.net/c_titan/158/challenge.zip)
# Solution
- So similar to the previous challenge where the flag was embedded in the git log is sort of the same but this time I needed to inspect the changes made on certain file

``` bash
 git log --follow -p message.py
commit 8c83358c32daee3f8b597d2b853c1d1966b23f0a
Author: picoCTF{@sk_th3_1nt3rn_2c6bf174} <ops@picoctf.com>
Date:   Tue Mar 12 00:07:11 2024 +0000

    optimize file size of prod code

diff --git a/message.py b/message.py
index 7df869a..326544a 100644
--- a/message.py
+++ b/message.py
@@ -1 +1 @@
-print("Hello, World!")
+print("Hello, World!"

```

