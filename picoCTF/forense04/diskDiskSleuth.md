# Disk,Disk, Sleuth!

# Description
Use `srch_strings` from the sleuthkit and some terminal to find a flag in this disk image: dds1-alpine.flag.img.gz
# Solution

-  Unzip it using gzip and finally with ```srch_strings``` and a ```grep``` I got the flag.

``` bash
gzip -d dds1-alpine.flag.img.gz
srch_strings dds1-alpine.flag.img | grep pico
ffffffff81399ccf t pirq_pico_get
ffffffff81399cee t pirq_pico_set
ffffffff820adb46 t pico_router_probe
SAY picoCTF{f0r3ns1c4t0r_n30phyt3_267e38f6}
# Flag
picoCTF{f0r3ns1c4t0r_n30phyt3_267e38f6}
```

