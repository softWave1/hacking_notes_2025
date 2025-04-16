# Bookmarklet

# Description
Why search for the flag when I can make a bookmarklet to print it for me?
Additional details will be available after launching your challenge instance.
# Solution
-  Analyzing the website it has some javascript code where  it prints the flag so I only ran the code in the browser console.

``` javascript
        javascript:(function() {
            var encryptedFlag = "àÒÆÞ¦È¬ëÙ£ÖÓÚåÛÑ¢ÕÓ¨ÍÕÄ¦í";
            var key = "picoctf";
            var decryptedFlag = "";
            for (var i = 0; i < encryptedFlag.length; i++) {
                decryptedFlag += String.fromCharCode((encryptedFlag.charCodeAt(i) - key.charCodeAt(i % key.length) + 256) % 256);
            }
            alert(decryptedFlag);
        })();
```

- The output of the code run.

```bash
# Flag 
picoCTF{p@g3_turn3r_18d2fa20}
```

