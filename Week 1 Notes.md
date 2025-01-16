
### Definitions:
- [[#Host Roles ]] - a network where each computer is *easily* defined as either a client or host
- [[#Peer-to-Peer ]] - a network where each computer is ***both*** the host and client
- [[#End Devices]] - where a message is sent from or received
- [[#Intermediary Network Devices]] - a device that is used to connect two (or more) end devices together
- MAC (media access control) address - a unique identifier *every* device has to help identify it on a LAN. It is *usually* made up of a series of 12-character hexadecimal number 
- [[#Network diagrams]] - these are diagrams to help represent how a network is connected and any other devices that are implemented (*CAN BE CALLED [[#Topology Diagrams]]*)
- [[#LAN]] - stands for local area network
- [[#WAN]] - stands for wide area network
- MAN - stands for metropolitan area network
- PAN - stands for personal area network
- [[#Intranets]] - a collection of LAN's connected by WAN's but administrated by one company/person
- [[#Scalability]] - to be able to expand quickly without diminishing service
- [[#Network Protocol Requirements]] - an agreement within a network in regards to certain requirements (such as encoding etc)
- Traffic Class - a number that represents the prioritisation of data (i.e. video or email)
- Payload Length - a number that represents how long the message is
- Hop Limit - ensures that this message does not flow through the network endlessly (ensures that the packet gets discarded eventually)
- Collisions - when more than one device sends a message causing both messages to become corrupt
- [[#Reference Models]] - models that are used as visual aids to help explain how networks may work
### Pre-Session Notes

#### Networking Today
- Communication has increased in the list of priorities we have for ourselves
- In modern networks, you have multiple roles to help the "web" become somewhat easy to circumnavigate

##### **Host Roles:**
- *every* computer is called a host or "end device"
- *servers are computers* that provide information to end devices
- you can have different types of servers:
	- web - servers run "web server software" whilst the end devices solely use browsers to help navigate the web servers
	- email - servers run "email server software" whilst clients use software to access emails
	- file - servers store these corporate and personal files whilst the end devices tend to only access them (remotely)
- **clients** are computers that send requests to retrieve information from the servers

##### **Peer-to-Peer:**
- it is actually possible for every computer on the network to be ***both*** the client and the host but there are some limitations
- its recommended to be reserved for *very* small networks
- below is a table representing the advantages and disadvantages to using this type of network

| ==Advantages==                                                  | ==Disadvantages==             |
| --------------------------------------------------------------- | ----------------------------- |
| Easy to set up                                                  | No centralized administration |
| Less complex                                                    | Not as secure                 |
| Lower cost                                                      | Not scalable                  |
| Used for simple tasks: transferring files, sharing printers etc | Slower performance            |

##### End Devices
- These are devices in the network where the message originates from (the sender) or where the message ends up being recieved at with no other pathway
	![[Pasted image 20250116160025.png]]

##### Intermediary Network Devices
- This is a device that connects two (or more) end devices together
- Examples of this include:
	- switches - devices that connect multiple devices within a network and use the relevant MAC addresses to forward data to the intended end device
		- LAN switch - 
		- multilayer switch - *"smarter"* than a standard switch as it acts as both a router and a  switch, in essence it has more usability
	- wireless access points (WAPs) - devices that act as the bridge for wireless devices to connect to the network 
	- routers - devices that connect local networks to a larger network (e.g. household network to the internet), it uses the IP addresses to forward data packets to the correct locations 
		- depending on the firmware, it may come with a firewall built-in/support (IT CANNOT BE ADDED RETROACTIVELY)
		- using the firmware, we can do something called [access control lists](https://learn.microsoft.com/en-us/windows/win32/secauthz/access-control-lists) to help *emulate* a firewall whilst maintaining the same router
	- firewalls - devices that monitor and control network traffic based on certain rules and regulations (that can be set), can be software-based, hardware-based or a combination of both
- These devices can:
	- regenerate and retransmit data signals
	- maintain information about what pathways exist in the network
	- notify other devices of errors and communication failures

##### Network Media

| ==Media Types==                                           | ==Description==                                                  |
| --------------------------------------------------------- | ---------------------------------------------------------------- |
| Metal wires within cables                                 | Uses electrical impulses                                         |
| Glass or plastic fibers within cables (fiber-optic cable) | Uses pulses of light                                             |
| Wireless transmission                                     | Uses modulation of specific frequencies of electromagnetic waves |

##### Network diagrams
- *Port and interface* can be used interchangeably 
- Network interface card (NIC) - a hardware component that allows a device to connect to a network, it can be built in or added but it **must have** the MAC address
- Physical Port - a physical place where you can plug in a wire to connect external peripherals to the network
- Interface - usually refers to the point of interaction between a device and the network (e.g. ethernet port)
![[Pasted image 20250116163905.png]]

##### Topology Diagrams
- There are two *main* types of topology diagrams:
	- **physical topology diagrams** - illustrate the physical location of intermediary devices and cable installation (see below)
		- *note:* there is room and location numbers for each of the devices (where applicable)
	![[Pasted image 20250116164545.png]]
	- **logical topology diagrams** - illustrate the devices, ports/interfaces and the addressing scheme of the network (see below)
	![[Pasted image 20250116164641.png]]

##### Types Of Networks
- The scalability of networks can very greatly depending on the user's need and the amount of devices connected to it
- Because of this *vary*, there are two main different types of networks that can be implemented depending on what the user's requirements are (*they can be used in tandem*)

###### LAN
- These networks tend to connect devices in a limited area
- There are usually administered by one person/organisation
- Can provide high-speed bandwidth to all devices connected
- LAN's are connected to each other via WAN's

###### WAN
- These are networks that link other LAN's together (over a wide geographical area)
	- by definition, it is greater than 1KM
- Typically administered by one or more organisations
- Provide slower speeds between the LAN's
- Typically use copper wires, fiber optic and/or wireless communications 
	- it depends on factors such as the environment, expected data transmission and cost


### In-Session Notes
#### Software and External Links
- He mentioned something called [packet tracer](https://www.netacad.com/cisco-packet-tracer)
- It ties in with the [cisco qualifications](https://www.cisco.com/site/us/en/learn/training-certifications/certifications/index.html)
- You can use [wireshark](https://www.wireshark.org/) to analyse packets

#### Common Types of networks
##### The Internet
- In essence, its a collection of multiple LAN's connected via multiple WAN's
- Because of the scope of the internet, it is administered by a multitude of companies
	- [IETF](https://www.ietf.org/) (Internet Engineering Task Force)
	- [ICANN](https://www.icann.org/) (Internet Corporation for Assigned Names and Numbers)
##### Intranets 
- This tends to be a *private* collection of LAN's (meaning invite-only)
- An organisation may use an extranet to provide secure access to their network for individuals who work for a different organisation
	![[Pasted image 20250116184448.png]]

#### Internet Connections
##### Internet Access Technologies
- There are a multitude of ways to connect to the internet such as:
	- broadband cable
	- broadband digital subscriber line (DSL)
		- this uses [existing phone lines](https://www.cisco.com/c/en_uk/solutions/routing-switching/dsl.html#:~:text=DSL%20(Digital%20Subscriber%20Line)%20is,and%20video%2C%20to%20service%20subscribers.) to connect you to the internet
	- wireless WAN's
	- mobile services

##### Home and Small Office Internet Connections

| ==Connection==    | ==Description==                                                                   |
| ----------------- | --------------------------------------------------------------------------------- |
| Cable             | high bandwidth, always on, internet offered by cable television service providers |
| DSL               | high bandwidth, always on, internet connection that runs over a telephone line    |
| Cellular          | uses a cell phone network to connect to the internet                              |
| Satellite         | major benefit to rural areas without Internet Service Providers                   |
| Dial-up telephone | an inexpensive, low bandwidth option using a modem                                |

##### Business Internet Connections
- Businesses tend to need a higher bandwidth with managed and *dedicated* connections (see [Vorboss](https://vorboss.com/))

| ==Type of Connection== | ==Description==                                                                                                                          |
| ---------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| Dedicated Leased Line  | These are reserved circuits within the service provider’s network that connect distant offices with private voice and/or data networking |
| Ethernet (WAN)         | This extends LAN access technology into the WAN                                                                                          |
| DSL                    | Business DSL is available in various formats including Symmetric Digital Subscriber Lines (SDSL)                                         |
| Satellite              | This can provide a connection when a wired solution is not available                                                                     |

##### The Converging Network
- Before, there would have been *separate lines* for telephone, video and data
	- each of these would have a different set of rules and standards
- Now, data networks carry them all

#### Reliable Network
##### Fault Tolerance
- Its something that can be used to describe a network that is **designed** in a way to ensure that not all devices will go down when there is a fault
	- **this means you need to provide alternate pathways** (think of parallel circuits)
	- you can add redundant (extra) devices that are in the network that click in when there is a fault 
	- you can do this by ensuring packet switching
		- packets of data takes different routes to the same destination
##### Scalability
- It means that it can expand *quick and easily* without impacting the performance of existing services
- You can achieve this by following the *accepted* standards and protocols
##### Quality of Service (QoS)
- This is the prioritisation of data traffic to ensure a smooth experience for all
- Most things can be staggered (which means that they are "*low priority*")
- Voice, video and audio **cannot** be staggered (which means that they are "*high priority*")

#### Network Trends
##### Cloud Computing
- This allows us to store/backup data on servers over the internet
- You *can* access applications virtually (through the server)
- It is made possible by utilising [data centres](https://cloud.google.com/)

##### Technology Trends In The Home
- Smart home technology is a growing trend
	- it allows everyday appliances to be interconnected with *"smart"* devices
	- it is done by sending and accessing data through the cloud
- **Security is not a forethought**

##### Powerline Networking
- This is a method of "boosting" signal range by utilising the powerline
	- [TP link has some good ones](https://www.tp-link.com/uk/home-networking/powerline/)
- More useful when WAP's cannot reach a location
- Tends to use a lot of power (inefficient)

#### Network Security
##### Security Threats
- Threats are *everywhere* regardless of the size of the network
- Network security ***must*** be implemented for all networks to ensure the security of data 
	- it should take into account the environment (home or office)
	- it should take into account the balance between data transmission and security
- Securing a network involves many protocols, technologies, devices, tools and techniques
- Threat vectors *may be* internal or external:
	- External:
		- viruses, worms, and Trojan horses  
		- spyware and adware  
		- zero-day attacks  
		- threat Actor attacks  
		- denial of service attacks  
		- data interception and theft  
		- identity theft
	- Internal:
		- lost or stolen devices  
		- accidental misuse by employees  
		- malicious employees
##### Security Solutions
- Security *should* be implemented in multiple layers using more than one solution
- Larger networks have additional requirements:
	- dedicated firewall systems
	- access control lists (ACL)
	- intrusion prevention systems (IPS)
	- virtual private networks (VPN)
- You can't really think about network security without understanding the underlying switching and routing infrastructure

#### Network Rules
##### Communications Fundamentals
- Due to the vary in size and complexity in networks, they must agree on *how* to communicate
- They must agree that
	- there will be a source (sender)
	- there will be a destination (receiver)
	- there will be a channel that provides the path for the communication to occur (media)
##### Communications Protocols
- ***ALL*** communications are governed by protocols
	- protocols are rules the communications will follow
##### Rule Establishment
- Individuals (or companies) must use the established rules to govern the conversation
- Example of comms without rule establishment:
![[Pasted image 20250116195523.png]]
- Example of comms with rule establishment:
![[Pasted image 20250116195547.png]]
- Protocols should account for the following:
	- an *identified* sender and receiver
	- common language and grammar
	- speed and timing of delivery
	- confirmation/acknowledgment requirements
##### Network Protocol Requirements
- common protocols must be in agreement and include the following:
	- message encoding
	- message formatting and encapsulation
	- message size
	- message timing 
	- message delivery options
##### Message Encoding
- This is the process of converting information into another *acceptable* form for transmission
- Decoding is the opposite of above
- A famous example is [base 64 encoding](https://en.wikipedia.org/wiki/Base64)
- Below is an example flowchart:
![[Pasted image 20250116200043.png]]
##### Message Formatting and Encapsulation
- *Every* time a message is sent, it **must** use a specific format/structure
	- this depends on the type of message and the channel used to deliver the message
- Without the change in formatting (and subsequent encapsulation), "raw" files would take too much data
##### Message Size
- Encoding between the devices is agreed which means that the encoding of messages has a *fixed* size
	- messages are converted into bits
	- bits are encoded into electrical impulses, light or sound (depending on the media)
	- the destination host must decode these patterns
##### Message Timing
- Timing is made up of three elements:
	- **flow control** - manages the rate of transmission and defines *how* much data can be sent
	- **response timeout** - manages how long a device waits for a reply from the destination
	- **access method** - manages when someone *can* send a message
		- there may be rules governing issues like *"collisions"*  
		- some protocols are proactive and attempt to prevent collisions whilst some are reactive and establish a recovery method after the collision occurs
			- proactive == **SLOW**
##### Message Delivery Options
- **Unicast** - one to one communication
- **Multicast** - one to many (typically not all)
- **Broadcast** - one to all
- (below is a visual aid explaining them all)
![[Pasted image 20250116201816.png]]

#### Protocols
##### Network Protocol Overview
- Defined as a common set of rules that can be implemented in:
	- software
	- hardware
- Each protocol has its own:
	- function
	- format 
	- rules
- (below is a table showing a few protocol types and their description)

| ==Protocol Type==      | ==Description==                                                                              |
| ---------------------- | -------------------------------------------------------------------------------------------- |
| Network Communications | enable two or more devices to communicate over one or more networks                          |
| Network Security       | secure data to provide authentication, data integrity, and data encryption                   |
| Routing                | enable routers to exchange route information, compare path information, and select best path |
| Service Discovery      | used for the automatic detection of devices or services                                      |
##### Protocol Interaction

| ==Protocol==                        | ==Function==                                                                                                                                                                                        |
| ----------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Hypertext Transfer Protocol (HTTP)  | Governs the way a web server and a web client interact                Defines content and format                                                                                                    |
| Transmission Control Protocol (TCP) | Manages the individual conversations                                          Provides guaranteed delivery                                                                     Manages flow control |
| Internet Protocol (IP)              | Delivers messages globally from the sender to the receiver                                                                                                                                          |
| Ethernet                            | Delivers messages from one NIC to another NIC on the same Ethernet Local Area Network (LAN)                                                                                                                                                                                                    |
#### Protocol Suites
##### TCP/IP Protocol Suites
- This is the main protocol used by the internet
- It houses other protocols (see image below)
- It is freely available to the public and can be used by any vendor
- It is endorsed and approved by a standards organisation to *ensure interoperability*
	![[Pasted image 20250116202943.png]]
##### TCP/IP Communication Process
- First the web server decides whether to use TCP or UDP
- Then it adds the user's IP packet
- The diagram below shows this encapsulation of data from a web page to a client
![[Pasted image 20250116203546.png]]
#### Reference Models
##### The Benefits of Using a Layered Model
- How a network operates is a *complex* concept and thus we use visual aids (like a layered model) to help explain and understand how it works
- Below is the open system interconnection (OSI) model and the TCP/IP model
![[Pasted image 20250116203817.png]]
- The OSI is a *theoretical* model (high-level abstraction)
- **Prof stated BOTH should be memorised**
- There are some benefits to using *layered models:*
	- it assists in protocol design as protocols operate at certain levels, this means that when you make a change to a protocol it **should not** affect any other protocol
	- fosters competition as different vendors can work together
	-  provides a *common* language to help describe the network functions and capabilities
##### OSI REFERENCE MODEL
![[Pasted image 20250116204204.png]]
##### TCP/IP REFERENCE MODEL
![[Pasted image 20250116204230.png]]

#### Data Encapsulation
##### Protocol Data Units
- Encapsulation is the process where protocols add their information to the data
- At each stage, a protocol data unit (PDU) has a different name to reflect its new functions
- ***THERE IS NO UNIVERSAL NAMING CONVENTATIONS***
	- *for this course only* - the PDUs are named according to TCP/IP protocols
![[Pasted image 20250116205519.png]]

#### Data Access
##### Layer 3 Logical Address
- IP packets contains *two* IP addresses
	- source IP address
	- destination IP address
- addresses may be on the same link or remote
- 10.0.0, 192.168 and 172.16 are all indications that its a private network
- **EVERY** IP address contains two parts:
	- Network portion (IPv4) or Prefix (IPv6)
		- left-most part indicates the network group of which the IP address is a member
		- EACH LAN AND WAN will have the **same** network portion
	- Host portion (IPv4) or Interface ID (IPv6)
		- the remaining parts identify the device within the network
		- this portion **must** be unique for *every* device
##### Role of the Data Link Layer Addresses: Same IP Network
- If devices are on the same *ethernet network*, the data link frame will use the MAC address of the destination NIC
- See [[#Definitions]] for more information