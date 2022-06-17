![[Pasted image 20220601212910.png]]
Due to relatively few restrictions present in switch-based infrastructures, packet analysis becomes quite challenging. Like hubs, switches do not broadcast the packets to every network port except the port the packet is received from. They learn the physical addresses of devices through the ARP (address resolution protocol) and populate a list of port numbers with corresponding MAC addresses. Even so, through some hardware or configurational changes it is possible to capture packets from other ports. The two most popular techniques are hubbing out and port mirroring.
Let’s make it simpler for you with a logical illustration. For instance, let’s assume that we have a 24—port switch and eight PCs, which are connected to different switch ports. We can place our sniffer (Wireshark PC) in any of the free switch ports and then configure port mirroring, which will copy all the traffic from the desired device we want to sniff to the port of our choice.

The following diagram depicts a simple demonstration of port mirroring:
![[Pasted image 20220601213225.png]]

Hubbing out is feasible when your switch doesn’t support port mirroring. To use the technique, you must actually unplug the target PC from the switched network, then plug your hub to the switch, and then connect your analyzer and target device to the hub so the target device becomes part of the same network.
Now the protocol analyzer and the target machine are part of the same broadcast domain. The following diagram will make it easier for us to understand the process precisely and in a simpler way:
![[Pasted image 20220601213348.png]]