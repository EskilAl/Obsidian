- [[#Outline|Outline]]
- [[#How is our data transmitted across networks?|How is our data transmitted across networks?]]
- [[#Recap- The OSI model|Recap- The OSI model]]
- [[#Recap - Encapsulation vs De-encapsulation|Recap - Encapsulation vs De-encapsulation]]
	- [[#Recap - Encapsulation vs De-encapsulation#Encapsulation|Encapsulation]]
	- [[#Recap - Encapsulation vs De-encapsulation#De-encapsulating|De-encapsulating]]
- [[#Recap - TCP/IP Model|Recap - TCP/IP Model]]
- [[#Why is TCP important?|Why is TCP important?]]
- [[#Transmission Control Protocol (TCP)|Transmission Control Protocol (TCP)]]
- [[#TCP Three-way Handshake|TCP Three-way Handshake]]
- [[#More about the TCP Three-way Handshake|More about the TCP Three-way Handshake]]
- [[#Sequence numbers|Sequence numbers]]
- [[#Acknowledgment|Acknowledgment]]
- [[#TCP header|TCP header]]
- [[#User Datagram Protocol (UDP)|User Datagram Protocol (UDP)]]
- [[#TCP vs UDP|TCP vs UDP]]
- [[#Prerequisite knowledge before you move on|Prerequisite knowledge before you move on]]
- [[#Physical Addresses|Physical Addresses]]
- [[#Logical addresses|Logical addresses]]
- [[#Internet Protocol (IP)|Internet Protocol (IP)]]
- [[#IPv4|IPv4]]
- [[#Problems with IPv4|Problems with IPv4]]
- [[#IPv6|IPv6]]
- [[#IP Addressing|IP Addressing]]
- [[#Classful Addressing|Classful Addressing]]
- [[#What class does an IP address belong to?|What class does an IP address belong to?]]
	- [[#What class does an IP address belong to?#The number of networks and the size of each network in different classes|The number of networks and the size of each network in different classes]]
	- [[#What class does an IP address belong to?#Why is the number of available host IDs in each network always 2 less?|Why is the number of available host IDs in each network always 2 less?]]
- [[#Subnet mask|Subnet mask]]
	- [[#Subnet mask#What are the subnet mask for class A, B and C?|What are the subnet mask for class A, B and C?]]
	- [[#Subnet mask#Summary Table of Classful Addressing|Summary Table of Classful Addressing]]
- [[#IP ranges that are set aside for various uses|IP ranges that are set aside for various uses]]
- [[#Problems with Classful Addressing|Problems with Classful Addressing]]
- [[#Summing UP|Summing UP]]

## Outline 
- Transmission Control Protocol ( #TCP)
- User Datagram Protocol (UDP)
- Physical addresses vs Logical addresses
- Internet Protocol (IP)
	- IPv4
	- IPv6
- IP addressing
	- Classful Addressing


## How is our data transmitted across networks?
- it is transferred based on the concept of **Packet Switching 
- Packet switching refers to a method of transferring data to one computer to another computer inn form of **packets.
- Before transmission, the data is **broken** into several small pieces called **packets.
- Each packet might travel through **a different path** to the destination computer.
- At the destination computer, there packets are **put together** into the original data.
![[Pasted image 20230913115317.png]]

## Recap- The OSI model
- OSI stands for **Open System Interconnection
- The OSI model was created by the international standard organization 
- the OSI model was created as a framework and reference model, rather than a standard that all network protocols must follow. 
- it consist of 7 layers. Each serving a specific purpose.
- All layers must work together  in the correct order to move data around the network. 

## Recap - Encapsulation vs De-encapsulation

![[Pasted image 20230913103010.png]]

### Encapsulation
- The process of taking data from the application layer to the physical layer.
- During encapsulation, information is added to the data

### De-encapsulating
- The process of taking data from the Physical layer to the Application layer.
- During decapsulation, information is removed from the data. 


## Recap - TCP/IP Model
- **TCP/IP Model** is another important model
- Most networks nowadays use the **TCP/IP protocol suite** for transmitting data.
- The TCP/IP protocol suite is made up of a **large number of network protocols** that **all work together** to enable computers in a network to communicate with each other.
- It gets the name because the two most important protocols in this suite are TCP (Transmission Control Protocol) and IP (Internet Protocol).


## Why is TCP important?
- Some packets might get lost during transmission due to many reasons.
- Due to packet loss, the original data is unable to be reassembled at the receiving site.

## Transmission Control Protocol (TCP)
- **TCP** is one of the most important protocols on the **transport layer** of the TCP/IP model.
- TCP provides **reliable connection** and **reliable data transfer**
	- It guarantees that data can be successfully received by the destination computer
	- Some popular application layer service/protocols that use TCP: Email, WWW, FTP.
	- What makes TCP work?
		- **TCP three-way-handshake.
		- **Sequence numbers**
		- **Acknowledgment 


## TCP Three-way Handshake
- Before two application processes can begin to send data to each other, they must establish a TCP connection using a process called **three-way-handshake**
	- This is why TCP is called **connection-oriented**

![[Pasted image 20230913103957.png]]

## More about the TCP Three-way Handshake 

![[Pasted image 20230913103907.png]]

## Sequence numbers
- TCP assigns **a sequence number** to **each segment** of the data. 
	- 1 to the first segment, 2 to the second segment, ...
- By doing so, the receiving computer can collect these segments, reorder the correctly, and see if any segment is missing. 

![[Pasted image 20230913104552.png]]


## Acknowledgment
- Whenever the receiving computer receives a segment, it sends an acknowledgment message to the sender computer.
![[Pasted image 20230913104638.png]]
- if the receiving computer finds a missing segment, it requests the sender computer to **re-transmit** the segment.


## TCP header 
![[Pasted image 20230913104717.png]]

## User Datagram Protocol (UDP)
- UDP is another important protocol on the **transport layer** of the TCP/IP model 
- However, unlike TCP, UDP is **connectionless.**
	• Any two processes **don’t** need to handshake with each other in advance.
	• They just keep sending data without caring if the other end receives the data or not.
 • UDP **doesn’t** offer reliable data transfer.
	• There is **no guarantee** of data delivery, ordering, or duplicate protection.
	• UDP is **simpler** and **faster** than TCP.
![[Pasted image 20230913104931.png]]
- **Voice chat, Video chat, and online games** are examples of application that often use UDP.


## TCP vs UDP
![[Pasted image 20230913105340.png]]

## Prerequisite knowledge before you move on
- Decimal 
- Binary 
- Hexadecimal 
- Conversion between decimal to binary 
- Conversion between binary to hexadecimal 
- AND operation 

## Physical Addresses 
- A physical address is a string used to **identify a network interface.
- This address is know as a **MAC address.
	- MAC stands for **Media Access Control.
- Every network interface controller (NIC) is assigned **a MAC address** by its **manufacturer**
	- The MAC address is **binding** on the NIC.  
	- it is stored in hardware, such as read-only memory, and usually cannot be changed. 
		- However, some drivers and tools allow the MAC address to be changed. This is called **MAC spoofing**.
- In human analogy, physical addresses are like our **personal IDs**.
	- Our personal ID don’t change no matter where we go.
	- The physical address of a NIC **is always the same** regardless of the location of the NIC.
- Every network device **in the same network** must have a **unique** MAC address.
	- because MAC addresses are used to move data frames from one computer/device **to the next adjacent** computer/device.
- A traditional MAC address **is 48 bits** long.
	- a bit represents two possible values: **0** and **1**.
	- 48 bits is equivalent to 48 of 0s and 1s.
- MAC addresses are expressed in **hexadecimal** format.
	- **Hexadecimal** is a **base 16 numbering system**, which uses **4** bits to represent the numerals **0-9** and the alphabetic letters **A-F**
	- Hence, a MAC address can be shortened to **12** hexadecimal numbers.
- Examples: 91-FC-5D-D9-A2-B0 or 91:FC:5D:D9:A2:B0
- **A dash (-)** or **a colon (:)** is placed every **two** hexadecimal numbers.
![[Pasted image 20230913110732.png]]
- EUI-60: A MAC address with a serial number extended to 36 bits long.
- EUI-64: A MAC address with a serial number extended to 40 bits long.

## Logical addresses
- Also known as **IP addresses.
- IP addresses are assigned to a NIC by **ISP (Internet Service Provider).
	- For example, when you purchases an internet service from an ISP, you are assigned an IP address.
- A NIC might use a different IP address when it is moved to a different place.
- **Every computer or device on the internet needs to have a unique IP address.
	- IP addresses are like our **home addresses**. Each is unique in the entire world.
	- IP addresses are used to make sure that data packets can be transmitted **over the internet** to the intended destination computer.

## Internet Protocol (IP)
- All IP addresses are managed by the internet protocol.
- The internet protocol is **the most important** protocol on **the internet layer** of the TCP/IP model.
- In addition of IP management, the internet protocol is responsible for **routing** data packets from on device to another device **across one or more networks.
- There are two versions of IP in use today:
	- **IP version 4 (IPv4)
	- **IP version 6 (IPv6)

## IPv4
- IPv4 was the first version deployed from production in the ARPANET in 1983
	- IPv4 used a **32-bit addressing** scheme, implying that each IPv4 address is **32-bit** long. 
	- IPv4 theoretically provides **2^32** (around 4 billions) IP addresses.
- Each IPv4 address is written in **dotted-decimal notation,** in which **each byte** of the address is written in a **decimal form** in the range [0...255] and is separated by a **period (dot)** from other bytes in the address 
- ![[Pasted image 20230913111919.png]]

## Problems with IPv4
- **IP address depletion
	- The number of devices connected to the internet grows exponentially.
- **Internet routing table expansion
	- A routing table is used by routers to make best path determination.
	- As the number of devices connected to the internet increases, the number of routers increases as well.
	- these IPv4 routes consume a great deal of memory and CPU resources on routers. 
- **Security wasn't considered in IPv4
	- IPv4 was designed with a network of relatively trusted users in mind where the network infrastructure was likely to be relatively secure.

## IPv6
- IPv6 was proposed in 1998 which uses **128-bit addressing.
	- Each IPv6 address is **128-bit** long.
- IPv6 theoretically provides **2^128** IP addresses.
- 340,282,366,920,938,000,000,000,000,000,000,000,000 unique IP addresses.
- An IPv6 address is represented as **eight groups** of **four hexadecimal digits.
	- Example: 2001:0db8:0000:0000:0000:8a2e:0370:7334
- Compared with IPv4, IPv6 can handle packets more efficiently, and is offers more security (due to the mandatory inclusion of IPsec)
- Note: IPsec stands for IP security, which is a group of protocols to ensure the the integrity, confidentiality and authentication of data communications over the Internet. 

## IP Addressing 
- As mentioned, IPv4 offers 2^32 addresses.
- How are these IP addresses allocated to organizations, companies, and users?
- Two methods for allocating IPv4 addresses:
	- 1. **Classful Addressing**
		- Introduced in 1981.
		- in use between 1981 and 1993.
	- 2. **Classless Inter-Domain Routing(CIDR)**
		- Introduced in 1993
		- Designed to slow the rapid exhaustion of IPv4 addresses.

## Classful Addressing
- Any IPv4 address in class A, B and C consists of two parts:
	- **1. Net ID** (also called Network ID/prefix/identifier)
		- It identifies which network a NIC belongs to.
	- **2. Host ID**(also called host identifier/number)
		- it is used to identify individual NICs.
- The **first byte** of each IP address in class **A** is used to indicate **a net ID**. The **First bit** is always 0.
- The **first two bytes** of each IP address in class **B** is used to indicate a **a net ID**. The **first two bits** are always 10.
- The **first three bytes** of each IP address in class **C** is used to indicate **a net ID**. The **first three bits** are always 110.
- The **first four bit** of each IP address in class **D** are always 1110.
- The **first five bits** of each IP address in class **E** are always 1111.

## What class does an IP address belong to?

![[Pasted image 20230913113658.png]]
### The number of networks and the size of each network in different classes 

![[Pasted image 20230913113801.png]]

### Why is the number of available host IDs in each network always 2 less?

![[Pasted image 20230913113838.png]]

## Subnet mask
- Computers and routers can only understand IP addresses in the binary format.
- How do they know what portion of an IP address is the net ID and what portion is the host ID?
- This is where **subnet mask** comes in.
	- A subnet mask is a sequence of ones(1) *followed by a block of zeros(0)**.
	- The **ones** indicate that  **the corresponding bits in the IP address** are **the net ID.**
	- The **zeros** indicate that **the corresponding bits in the Ip address** are **the host ID.**
![[Pasted image 20230913114203.png]]
- The Net ID can be determined by the **AND** operation.

### What are the subnet mask for class A, B and C?

![[Pasted image 20230913114302.png]]

### Summary Table of Classful Addressing 
![[Pasted image 20230913114331.png]]

## IP ranges that are set aside for various uses
- What are Private IP address?
	- They are used **within a local network.
	- They are **not** directly reachable from the internet.
	- But they enable **more devices** to connect to the internet. 
- ![[Pasted image 20230913114542.png]]

## Problems with Classful Addressing
- **Inflexibility
	- IP addresses **cannot** be assigned according to user requirements since the allocation unit must be an entire network in Class A, B or C.
	- A class-A or class-B network is to large for almost all organizations.
	- A class-C network is too small for most organizations/companies.
- **Wastage of IP addresses** due to the inflexibility.

## Summing UP
- In this lecture, we have learned 
	- Transmission Control Protocol (TCP)
	- User Datagram Protocol (UDP)
	- Physical addresses vs Logical addresses
	- Internet Protocol (IP)
		- IPv4
		- IPv6
	- Classful Addressing
	- Problems with Classful Addressing.