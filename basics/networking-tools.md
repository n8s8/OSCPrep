# Essential/basic networking tools

## ping
Used to test whether a connection to a remote resource is possible.
Ping works using the ICMP protocol, which works on the Network layer of the OSI Model and Internet layer of the TCP/IP model. 

Basic syntax:
> `ping <target>`

Example:

![ping](pictures/ping-eg.png "ping google.com")

Ping returned the IP address for the Google server that it connected to, rather than the requested URL. 

Ping Manual (on Linux):
> `man ping`
