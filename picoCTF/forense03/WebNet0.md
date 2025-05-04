# WebNet0 

# Description
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key). Recover the flag.
# Solution
-  After downloading the given files and checking out for the packages using ```wireshark``` I can see nothing related to the flag in the program due one of the hints challenges said something about TLS protocol and the challenge provide me a key I just upload the key into the program and its done I can see the contents of the packages finally using the search bar and flitering with the keyword *pico*  I found the flag.

``` bash
# Pico-Flag: picoCTF{nongshim.shrimp.crackers}
```


# References
- [picoCTF 2019 writeup 25 - Forensic - WebNet0](https://www.youtube.com/watch?v=9uflLPoETOc&list=PLDo9DMLZyP6kTZ8Td37-LdbAx4-yNfHBl&index=25)
