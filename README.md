# EJPT-Guide

# Host Discovery / Enumeration
#### Let's find out what we are working with.  We are completely blind.
![image](https://user-images.githubusercontent.com/80599694/147906631-44437a80-1098-4275-bc2f-22b8827da8bb.png)

### Ping Sweep, who can we find on the network?

#### fping:
````bash
fping -a -g {IP RANGE} 2>/dev/null
````
#### fping example:
````bash
fping -a -g 10.10.10.0/8 2>/dev/null
`````
#### Nmap Ping Sweep:
````bash
 nmap -sn 10.10.10.0/8 | grep -oP '(?<=Nmap scan report for )[^ ]*'
````
