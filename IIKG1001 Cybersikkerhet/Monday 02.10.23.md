# Subnetting, CIDR, DHCP, NAT, Routing, ARP

## Subnetting
- An IP address range is *a series of IOP addresses*
	- For example, 0.0.0.0 - 255.255.255.255 is the entire IPv4 address range.
- For allow multiple organizations and users to use IP addresses, *subnetting* is used.
	- Subnetting refers to breaking an IP address range into smaller  pieces to that multiple 
	  smaller networks can be created and user to multiple organizations
	  - For example classfil addressing is a subnetting approch to break IPv4

## Classless inter-Domain routing (CIDR)
- CIDR was introduced in 1993 to replace classful addressing.
- It can be sued for both IPv4 and IPv6
- CIDR is based on variable length subnet masking(VLSM)
	- Enables an IP address space for further....

## CIDR Notation 
- In CIDR, any 32-bit IP address is expressed in a dotted-decimal format a,b,c,d/x
	- "a-b-c-d" represents an IPv4 address.
	- "/x" is called **CIDR block prefix** and it indicates **how many bits from the left of the IP address are the net ID.**
- Given a CIDR notation, we can easily know the corresponding **net ID** and **Host ID** using the **AND** Operation. 

## The Structure of an IP Address in CIDR
- By taking *x bits* from the original host ID part, **2^x subnets** can be created.
	- IF x=1 bit, 2^1 subnets can be crated.
	- IF x=2 bit, 2^2 subnets can be crated.
	- IF x=3 bit, 2^3 subnets can be crated.
- Each crated subnet can be **Assigned** to an organization.

## CIDR subnetting example
- Suppose a company bought a class-C IP address range (200.250.180.0/24) from an ISP
- The IP address range is from **200.250.180.0** to **200.250.180.255
- Assume that the company needs **four** networks with **a minimum of a 25 IP addresses** in  each one.
- How do we make it happen?
	- IF x=1, then 2^1 subnetworks can be created. But two subnetworks don't meet the requirement.
	- IF x=2, then 2^2 subnetworks can be created
		- Each subnetwork can offer 2^(8-2) (i.3.,64) host IDs
- in other word, a network of 200.250.180.0/26 provides 4 subnets.
- Each subnets provides 62 available host IDs

## CIDR blocks 
- A CIDR block consists of an IP address, followed by a forward slash (/), and a CIDR block prefix.
- A CIDR block is **a group of IP addresses** that share **the same net ID**.
- Example: 192.269.1.0/24 is a CIDR block.
- **The size of a CIDR block** is determined by **the length of the CIDR block prefix**.
	- A long prefix length provides less host ID's.
	- A short prefix length provides more host ID's.

## How are IP addresses allocated in the real world?
![[Pasted image 20231002084726.png]]

## Recap - Public IP Addresses Vs Private IP Addresses

### public
- Public IP addresses are IP addresses that are **directly reachable** from the internet.
- They are used to **identify** a specific device or network on the internet.
- Provided by internet service providers(ISP).
- They come with a cost.

### Private
- Private IP addresses **cannot** be directly reachable from the internet.
- They are **reserved** and used for **internal communication** within a private network.
	- E.g., home network or an organization's intranet.
- Private IP addresses can be **freely used** within any private network.

## Questions 
1.  How do computer devices get a private IP address
2. Who is responsible for translating between a private IP address and a public IP address? 
3. How does a router know the next hop to send a data packet?
4. How does a router send the packet to the "correct" machine within its local area network.

## Two ways to assign  private IP address to a computer device

- **Manually**
	- Less often used
	- The private IP address is called the "static" private IP address.
	- The computer device will always use the same private IP address.

- **Dynamically using DHCP
	- Most often used

## Network Address Translation (Nat)
- NAT is a protocol operating typically on a **router** between a **private network** and **the Internet.**
	• Hence, NAT belongs to the Internet layer of TCP/IP model.
- **NAT** is responsible for **translating** between a private IP address and public IP address.
- NAT allows **multiple computers on a private network** to connect to the internet by **using just one public IP address. 

## Nat used today 
• It is called **Port Address Translation (PAT)**. Also known as **NAT Overload**.
• PAT works on routers by creating **dynamic NAT mapping**.
• It allows multiple devices to access the internet simultaneously using the same public IP address but with different port numbers.
• It uses different port numbers to keep track of which internal device a specific outbound network request belongs to.

## Benefits of NAT
- with NAT, we don't need to purchase one public IP address for each computer inside a network to access the internet.
	- They can **share** just one public IP address
- In addition, NAT provides a layer of protection because **all computers on a network** are **hidden** from the internet.
	- Because of private IP addresses, these computers aren't easy to be attacked from the internet.

## Steps taken by a router
1. Extract the net ID of the destination IP address of the data packet.
2. Compare the net ID with its routing table to see if there is any matching route.
3. if there is a match, the router sends the data packet to the next hop via the corresponding interface.
4. Otherwise, the router chooses the default route and forwards the packet.