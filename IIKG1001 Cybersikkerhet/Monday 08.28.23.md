
# Introduction to computer network.

- [[#What is a computer network?|What is a computer network?]]
- [[#A brief history|A brief history]]
- [[#Different Types of Networks|Different Types of Networks]]
	- [[#Different Types of Networks#Wide Area Networks(WANs)|Wide Area Networks(WANs)]]
	- [[#Different Types of Networks#Local Area Networks (LANs)|Local Area Networks (LANs)]]
	- [[#Different Types of Networks#Metropolitan Area Network  (MANs)|Metropolitan Area Network  (MANs)]]
- [[#==The internet==|==The internet==]]
	- [[#==The internet==#==Wired NIC==|==Wired NIC==]]
	- [[#==The internet==#==Wireless NIC==|==Wireless NIC==]]
	- [[#==The internet==#==Repeaters==|==Repeaters==]]
	- [[#==The internet==#==Hubs==|==Hubs==]]
	- [[#==The internet==#==Bridges==|==Bridges==]]
	- [[#==The internet==#==Switches==|==Switches==]]
	- [[#==The internet==#==Routers==|==Routers==]]
	- [[#==The internet==#Wireless Access Points & Wireless Routers|Wireless Access Points & Wireless Routers]]
- [[#What is network Topology?|What is network Topology?]]
	- [[#What is network Topology?#Bus Topology|Bus Topology]]
	- [[#What is network Topology?#Star topology|Star topology]]
	- [[#What is network Topology?#Ring topology|Ring topology]]
	- [[#What is network Topology?#Mesh topology|Mesh topology]]
	- [[#What is network Topology?#Full mesh topology|Full mesh topology]]
	- [[#What is network Topology?#Hybrid topology|Hybrid topology]]
- [[#What are network protocols?|What are network protocols?]]
	- [[#What are network protocols?#SMTP: Simple mail transfer protocol.|SMTP: Simple mail transfer protocol.]]
	- [[#What are network protocols?#POP3: post office protocol|POP3: post office protocol]]
	- [[#What are network protocols?#IMAP: internet message access protocol|IMAP: internet message access protocol]]
	- [[#What are network protocols?#FTP:|FTP:]]
	- [[#What are network protocols?#Telnet|Telnet]]
- [[#Summing up|Summing up]]


## What is a computer network?

A Computer network is a group of computers systems and computing devices that are linked together and able to communicate with each other.

## A brief history

The very first network is called sneaker net.

It refers to the transfer of electronic information by physically moving media (such as floppy disks, optical discs) between computers, rather than transmitting it over a computer network.

The first solution was to connect dumb terminals to a mainframe computer.

In parallel to the mainframe solution, researchers and the military in US worked together to develop ARAP.Net

ARAP : Advanced Research projects Agency

In the mid-1980s, personal computers(pcs) became popular everywhere.

By the late 1980, Pcs are linked to servers for data sharing.  

Later on the networking technology became more and more mature.

Companies and individuals wanted to use the internet and access the information on the internet.

This was when the World wide web(WWW) was invented.

WWW is a service running on top of the infrastructure of the internet

Many different protocols were also developed

All of these make today's internet.

## Different Types of Networks

Computer networks are divided into two types:

### Wide Area Networks(WANs)

A WAN can stretch across large geographical areas.

The biggest WAN is the internet.

A Wan used by a enterprise is called an enterprise network

### Local Area Networks (LANs)

It is a network limited to a local area(such as a room, a house, a building, or several nearby buildings)

### Metropolitan Area Network  (MANs)

Larger than LAN, Smaller than WAN

Not used anymore

## #The-Internet

The internet is the largest computer network that interconnects billions of computing devices throughout the world

An internet service provider (ISP) is an organization that provides different services for accessing, using, or participating the internet.

Network interface Cards (NICs)

NICs enable computers to communicate over a network

'Every computer needs a NIC in order to connect to a network or the internet.

Also known as Network interface controller or network adapter.

### #Wired-NIC

Used to connect to a wired network.

Expansion cards or built into a motherboard

### #Wireless-NIC

Used to connect toa wireless network

Expansion card, built into a motherboard, or built into a portable device, such as a USB stick.

### #Repeaters

A repeater is a device that repeats or amplifies any signal it receives before transmission.

The purpose is to extends the range of a particular cable run or enlarge the coverage area of a Wi-Fi network

### #Hubs

A hub is a networking device with multiple ports that can connect multiple computers/devices together into a network.
When a computer sends a signal, the hub will broadcast the signal to all the other ports of the hub.
If two or more computers send signals at the same time, their signals will interfere with each other.
This is called a collision.
Therefore, with a hub, only one computer can send a signal at a time.
A network built by a hub is called a collision domain.
More computers connected to a hub, more signals might collide.
Hence, a hub is suitable for building a small network.

### #Bridges

A bridge is a device to interconnect two network segments together but separate them into independent collision domains.

How does a bridge control network traffic

If a computer (e.g., computer1) sends data to another computer in the same segment (e,.g.,computer4), the bridge doesn't broadcast the data to another segment, thereby reducing signal collision.

Traditional bridges have only two ports. Newer bridges have more ports, but people stop calling them "bridges". Instead, they call them "switches".

### #Switches

Switches are network devices designed to connect multiple network devices (usually computers) together to from a local area network

The simplest and most common types of switches is the basic switch

A basic switch has several ports/interfaces.

It is also called multiport bridge

Because each port is considered as a collision domain.

A collision domain between any two ports can be dynamically created to establish communication, and of course be automatically removed when the communication ends.


### #Routers

A router is used to move data packets around a larger network.

Routers are smart

They know how to send a data packet to the next stop so that it can arrive at the intended remote destination.

Routers use routing tables to determine the best route for each packet.

### Wireless Access Points & Wireless Routers

Wireless Access Points is also known as access point (AP).

It is a device that allows wireless devices to connect to a wired network.

Wireless routers include not only the functions of a wireless access point, but also the functions of a router.

They have several ports for wired devices to connect to the network.

## What is network Topology?

A network topology refers to the shape of a network.

Basic Network topology

### Bus Topology

All computers are linked to each other through one main cable, called backbone cable.

Only once computers can send a signal at a time when the bus is free. Otherwise, signals might collide with each other.

Pros: 
	\-East to build
	\-Cheap

Cons:
	\-If the main cable breaks at any point, the whole network fails and difficult to isolate the problem.'
	\-Data Collision
	\-This topology was used to be important, but now is not longer used.

### Star topology

Computers are connected into a network, via one central device such as a hub or a switch.
It is the most commonly used topology.

Pros:
	\-If the cable to one of the attached computers breaks, only that associated computer will be affected.
	\-Easy to isolate a network problem.

Cons:
	\-The central device is a single point of the failure.
	\-It requires more cables, so it is more expensive than the bus topology.

### Ring topology

One cable is formed into a ring to connect all computers.
A signal known as a Token is constantly circulating (in one direction) in the network.
If a computer wants to send date, it needs to take control of the token so that it can send the data to the destination computer.

Pros:
	\-No data collision (due to the use of the token).

Cons:
	\-A single break in the cable can bring down the entire network.
	\-No longer used in modern networks.

### Mesh topology

This topology is often used to build a wide area network.

Each node is the topology can be a computer or a building.

Two types:

### Full mesh topology

Every node is connected directly to every other node in the network.
Total number of connections is (n(n-2))/2, where n is the number of nodes in the network.
Great reliability but expensive.

Partial mesh topology.
Each node directly connects to at least two other nodes.
Less reliability and less expensive. 

### Hybrid topology

A mix of combination of two or more network topologies.

How do computers communicate with each other over the internet?

They need to a wat to understand each other. they need to speak the same language(I.e., network protocols)

They also need each other's contact information!

## What are network protocols?

Network protocols are sets of established rules that network needs to follow in order to be able to communicate with each other.

Without network protocols, computers are unable to talk to each other

Many diff types:

#IP, #SFTP, #DNS, #HTTP, #FTP, #UDP, #SSH, #TI, #ICMP, #IMAP,etc.

### #SMTP: Simple mail transfer protocol.

It is used to transmit emails from one client to a mail server or from one mail sever to another mail server.

### #POP3: post office protocol

It is used by email clients to retrieve emails from their mail servers.

After the emails are downloaded they will be deleted to save the storage space of the mail server.

### #IMAP: internet message access protocol

Similar to POP3, but IMAP doesn't delete emails for the mail server 

### #FTP:

Ftp stands for file transfer protocol

It is used for transferring files between computers on a computer network, such as the internet.

A client-server model.

It enables people to easily share files.

Not secure since data is transferred in plain text.

It has been replaced by STFP(SSH file transfer protocol) and FTPS(file transfer protocol over SSL/TLS).

### Telnet

Telnet is one of the earliest remote login protocols on the internet.

Telnet allows users to log in to a remote host and issue commands.

It has a security problem.

The telnet session between the client and the server is not encrypted.

It has been replaced by secure shell (SSH).

## Summing up

In this lecture, we have learned

What a computer network is

How computer network evolves

Different types of networks

LANs, MANs, WANs, and the internet

Common network devices

NICs, repeaters, hubs, bridges, switches, routers, wireless access points, wireless routers.

Basic network topologies

Bus,star,ring,full mesh, pertial mesh, hybrid

Definition of network protocols

Some basic network protocols

SMTP, POP3, IMAP, FTP, Telnet