
### Definitions:
[[#Subnet Mask]] - used to identify a network
[[#Prefix Length]] - a less cumbersome method used to identify a subnet mask address
[[#Broadcast Address]] - this is when one host is sending packets to every other IP addresses
### In-Session Notes: 

#### SOFTWARE TO BE USED THROUGHOUT THE COURSE
##### Wireshark
**FORENOTE:** This was based on the lab from last week but we did not have enough time in the lab room to go over it. *Unfortunately,* I was located in the side of the room but the prof did record it.

- This program automatically organises packets into colours based on present filters
	- THESE COLOURS CAN BE CHANGED
- By clicking into the row, the bottom left "terminal" gives information such as the MAC address, protocol type etc
	- it can also split the MAC address' into the source and the destination
- You can filter out the packets by filtering
	- for example, if you wanted the DNS packets then you would just type DNS in the filter search bar located just above the window showing all of the packets
	- *to close the filter* - press the **cross/x** on the right of the filter search bar
- *You **CAN** filter by time and date also*
- A three way handshake (TCP) is:
	- sending system sends a sync request (SYN)
	- receiving system receives this
	- receiving system sends a sync request + acknowledge signal (ACK + SYN)
	- sending system sends an acknowledge signal (ACK)
##### Cisco Packet Tracer 
**FORENOTE:** This was based on the lab from last week but we did not have enough time in the lab room to go over it. *Unfortunately,* I was located in the side of the room but the prof did record it.
#### Slide Notes - IPv5 Addressing and Subnetting
- An IPv4 address is a 32-bit hierarchical address that is made up a network portion and a host portion
	- THIS IS NO LONGER VIABLE FOR MODERN SYSTEMS
		(below is a diagram representation of this)
		![[Pasted image 20250123195259.png]]
##### Subnet Mask
- This mask is compared to the IPv4 address bit for bit, *from left for right*
- The actual process used to identify the network and host portions is called "**ANDing**"
	(below is the IP address annotated to highlight this)
	![[Pasted image 20250123195600.png]]

##### Prefix Length
- The prefix length is the number of bits set to 1 in the subnet mask
- It is written in the slash notation
	- counting the number of bits in the subnet mask and prepend it with a slash
	![[Pasted image 20250123195805.png]]

##### Broadcast Address
![[Pasted image 20250123200407.png]]

##### Routing to the internet
- NAT (Network Address Translation) translates private IPv4 addresses to public addresses
	- this is usually enabled on the edge router connecting to the internet
- It translates the private *INTERNAL* addresses into public addresses 

##### Types of IPv4 Addresses
###### Link-Local Addresses
- This is when the device can self assign addresses
- Usually used by the Windows DHCP clients to self-configure when no DHCP servers are available
- ***SHOULD*** only be used for temporary connections
###### Legacy Classful Addressing
- *THIS HAS BEEN ABOLISHED SINCED THE **1990'S***
	![[Pasted image 20250123201556.png]]
	