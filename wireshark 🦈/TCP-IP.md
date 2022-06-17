The **TCP/IP**model comprises four layers, as shown in the following diagram. Each layer has a specific purpose to fulfill and utilizes a set of protocols to facilitate communications. Every protocol in every layer has a specific purpose:![[Pasted image 20220527173333.png]]

The first layer is the **Application Layer**, which directly interacts with users and subsequent layers and protocols; it is primarily concerned with the representation of the data in a understandable format to the user. The application layer also keeps track of user sessions, monitoring who is connected; it uses a set of protocols that helps to interface with users and other layers in the TCP/IP model. Some popular protocols in the Application Layer are as follows:
- Hypertext Transfer Protocol (HTTP)
-  File Transfer Protocol (FTP)
-  Simple Network Management Protocol (SNMP)
-  Simple Mail Transfer Protocol (SMTP)
- DNS

The second layer is the **Transport Layer** .The purpose of this layer is to create sockets (a combination of the port and IP address) in order to let two endpoints communicate. Sockets facilitate the creation of multiple distinct connections between two or more devices (more than one tab can be opened in Chrome).
The transport layer also serves as a backbone for the communication. The two most critical protocols that work in this layer are the #TCP and #UDP:
- The #TCP is a connection-oriented protocol, also called a reliable protocol. Firstly, a dedicated communication channel is established between the endpoints, which is then followed by data transmission. Equally partitioned chunks are transmitted from the source, and the receiving end sends an acknowledgement for every packet received. The side that is sending the data resends the packet if an acknowledgement is not received within a stated time frame. 
- The #UDP is a connectionless protocol and is often called an unreliable communication form. In the UDP, no dedicated channel is established, which also makes it a simpler and faster way of communication. There are also no acknowledgement packets sent by the endpoints. For example, if you are playing an online game, the loss of a few packets over the communication channel is not going to hamper your gaming experience because the number of packets coming through is huge, and a few missing packets will not make much difference to the overall quality of the network stream.

The third layer is the **Internet Layer**, which is primarily concerned with routing and movement of data between networks. The primary protocol that works in this layer is the #IP (Internet Protocol). The IP provides the network packets with the routing capability that they need in order to reach their destination. Other protocols included in this layer are the #ICMP and #IGMP.

The fourth and final layer is the **Link Layer** (often called the network interface layer). It interfaces with the physical network hardware. There are no protocols specified in this layer by the TCP/IP; however, several protocols are implemented, such as the Address Resolution Protocol ( #ARP) and the Point to Point Protocol( #PPP). This layer is concerned with how information travels inside the communication channel (wired or wireless). The link layer is responsible for establishing and terminating the connection, as well as converting the signals from analog to digital and vice versa. Devices such as bridges and switches operate in this layer.

The following diagram depicts the process of encapsulation:
![[Pasted image 20220527175224.png]]
