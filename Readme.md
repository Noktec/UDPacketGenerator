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

This line defines the number of packets send
``` 
 #define N_LOOP 10
```
Change 10 by 1000 if you need to send a 1000 packets


Errors 
------

If you face the following error: 
```
DPacketGenerator.c:48:2: warning: this decimal constant is unsigned only in ISO C90 [enabled by default]
  unsigned long ip_src = hasard(4294967295/2,4294967295);
```
Simply replace line 53 with this one :
```
unsigned long ip_src = hasard(4294967295LL/2,4294967295LL);
```



Sources 
------
The function ***in_chksum***  was taken from the papasmurf source code : http://packetstormsecurity.com/files/15266/papasmurf.c.html



---


Copyright (C) 2013 Noktec

This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with this program. If not, see http://www.gnu.org/licenses/.
