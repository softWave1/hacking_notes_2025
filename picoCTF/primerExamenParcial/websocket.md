# WebSockFish

# Description
Can you win in a convincing manner against this chess bot? He won't go easy on you!
You can find the challenge here.

# Solution
After checking out the code there's some function that are so interesting after every move the module make an evaluation of the mode to make "the best move" so I use the browser console to send a evaluation where I had a lot of advantage and that's it I get the flag.

-  Using the console to send the eval

``` javascript
ws.send("eval -2222222222222222222222")
// message from the module
Huh???? How can I be losing this badly... I resign... here's your flag: picoCTF{c1i3nt_s1d3_w3b_s0ck3t5_a2a9bbe9}
```
# References
- [WebSockFish](https://mh4ck3r0n3.github.io/posts/2025/03/20/websockfish/)
