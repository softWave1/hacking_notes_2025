# Glory of the Garden

# Description

This [garden](https://jupiter.challenges.picoctf.org/static/43c4743b3946f427e883f6b286f47467/garden.jpg) contains more than it seems.
# Solution
-   After getting the file I use the command ```strings``` and i filter it with a grep . 
``` bash
# Getting the file 
wget https://jupiter.challenges.picoctf.org/static/43c4743b3946f427e883f6b286f47467/garden.jpg

# Printing the printable characters 
strings -n 20 garden.jpg | grep pico

#output 
strings -n 20 garden.jpg | grep pico
```