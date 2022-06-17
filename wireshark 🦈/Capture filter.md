The building blocks of a capture filter are the protocol, direction, and type. For example,**tcp dst port 22** captures only TCP packets with a destination port of 22. The possible types are:
- host
-  port
-  net
-  portrange

Direction can be set using src or dst. As you suspect, *src is for capturing from a specified source address,* while *dst can specify the destination address*.

can be used: **src or dst and src and dst.**

The following are the most commonly used BPF protocols: 
- ether (filtering Ethernet protocols) 
- tcp (filtering TCP traffic)
-  ip (filtering IP traffic)
-  ip6 (filtering IPv6 traffic) 
- arp (filtering ARP traffic)

In addition to the standard components, there is a set of primitives that do not fit in one of the categories:
- gateway (matches if a packet used the specified host as gateway)
-  broadcast (for broadcast, not unicast, traffic) 
- less (less than, followed by a length) 
- greater (greater than, followed by a length)

Capture filter expressions can be strung together using logical operators. Again, with both the English and the logical notation: 
- and (&&) 
- or (||) 
- not (!)


[[examples]]
![[Pasted image 20220601221833.png]]

