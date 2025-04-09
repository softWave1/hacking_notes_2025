# shark on wire 2

# Description
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/b506393b6f9d53b94011df000c534759/capture.pcap). Recover the flag that was pilfered from the network.
# Solution
After downloading the file and exploring the packages using ```wireshark``` I found out that the packages that uses the ```udp``` protocol has some marks of start and end going even deeper in the content of this packages all has the same port destination once I filter the packages that has the port 22 as destination I saw that the one that has the information field up to 5000 after subtracting  5000 to this numbers I found out that they can be converted from ASCII code into letters and iterate over every packet until I get the flag so I made a python script to accomplish this task.
##### Python code

``` python 
from scapy.all import * 
 
packets = rdpcap('capture.pcap')
 
flag = ''
 
for p in packets:
    if UDP in p and p[UDP].dport == 22:
        if p[UDP].sport > 5000:
            flag += chr(p[UDP].sport - 5000)
 
 
print(flag)

# Output 
# picoCTF{p1LLf3r3d_data_v1a_st3g0}
```

# References
- [picoCTF 2019 writeup 23 - Forensic - shark on wire 2](https://www.youtube.com/watch?v=WcMl1SvQ6hI&list=PLDo9DMLZyP6kTZ8Td37-LdbAx4-yNfHBl)
