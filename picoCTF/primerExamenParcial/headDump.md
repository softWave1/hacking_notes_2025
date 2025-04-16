# head-dump 
# Description
Welcome to the challenge! In this challenge, you will explore a web application and find an endpoint that exposes a file containing a hidden flag.The application is a simple blog website where you can read articles about various topics, including an article about API Documentation. Your goal is to explore the application and find the endpoint that generates files holding the server’s memory, where a secret flag is hidden.

Additional details will be available after launching your challenge instance.
# Solution

-  Exploring the website there's an interesting section where it's the api documentation in the list of endpoints there's this url ```/heapdump``` that leads to a .json file where there's information about the memory of the application after downloading the file and filter its content with the ```grep``` I get the flag.

``` bash
wget http://verbal-sleep.picoctf.net:55344/heapdump
# The file downloaded name could change

cat heapdump-1744748730800.heapsnapshot | grep picoCTF{
picoCTF{Pat!3nt_15_Th3_K3y_439bb394}
```
