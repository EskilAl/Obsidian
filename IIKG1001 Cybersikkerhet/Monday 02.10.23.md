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