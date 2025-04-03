# Shark on wire

# Description
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/483e50268fe7e015c49caf51a69063d0/capture.pcap). Recover the flag.
# Solution
Using the tool wireshark I looked up for the packages then I selected the UDP  and I clicked on "folow stream ' finally I switch over channels until y found the flag in channel number 6

``` bash
# open wireshark
wireshark capture.pcap

# flag 
picoCTF{StaT31355_636f6e6e}
```


