UDP PACKET GENERATOR 
------
UDP Packet Generator is an old file made a few years ago, to send packets to specific destinationIP addresse with random source addresses. 

Note : It only works on Unix based systems.  

Used against some cisco IP phones, it is able to perform a DOS attack. 


How to
-----

- Do not forget to change the IP address on line  28 and 31 : 

```
udp("xxx.xxx.xxx.xxx"); //replace with IP
```

-  To compile : 

```
$ gcc UDPacketGenerator.c -o udpPacketGenerator

```
- To run :

```
$ ./udpPacketGenerator

```



Sources 
------
The function ***in_chksum***  was taken from the papasmurf source code : http://packetstormsecurity.com/files/15266/papasmurf.c.html