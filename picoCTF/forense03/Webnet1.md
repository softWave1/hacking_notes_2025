# Webnet1

# Description
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key). Recover the flag.
# Solution
At first I try to use the same method that I use in the [last challenge](webNet0) but after uploading the key I just found a fake flag , going deeper into the packages I found out that there was an image in the packet 43 after downloading and using ```strings``` to print the printable characters I found the flag.

``` bash
strings vulture.jpg | grep pico
picoCTF{honey.roasted.peanuts}
```
# References
- [picoCTF 2019 writeup 25 - Forensic - WebNet1](https://www.youtube.com/watch?v=Ym3i79nEHjw&list=PLDo9DMLZyP6kTZ8Td37-LdbAx4-yNfHBl&index=25)
