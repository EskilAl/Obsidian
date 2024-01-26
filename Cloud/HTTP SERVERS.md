
## Client - Server Model
- Server:
	- Provider of data and services
	- may serve one or more services 
	- typically servers multiple clients
	- can operate on local networks or vie the internet 

- Client
	- Sends requests for data or services to server 
	- Primarily concerned with presentation or post-processing 

- Typical for modern network/web applications:
	- Server may be a client itself (to some other server)
	- Client may likewise be a server to other clients

## How does the communication work?
- What information do we need on a client to connect to a server?

## ISO OSI Reference Model & TCP/IP Model 
- TCP/ IP MODEL
	- Application -> Application-specific data -> Service specific protocol(s)
		- HTTP, FTTP, TELNET, NTP, DHCP, PING
	- Transport -> Service -> Service endpoints(s)
		- TCP,UDP
	 - Network -> Host -> Server address(es)
		 - IP,ARP,ICMP,IGMP
	- Network Interface -> Infrastructure -> Establishing Physical connections
		- Ethernet

### ISO Open System Interconnect Model
- Application -> Data
- Presentation  -> Data
- Session -> Data
- Transport -> Segments
- Network -> Packets
- Data Link -> Frames
- Physical -> Bits

### Which Protocols do we need to know for web applications?

## Back To the roots
- Central web protocol: Hyper Text Transfer Protocol
- Hyper text?
- Principles?
	- Uniform Resource Locator (URL)
	- Request/response protocol (HTTP)
		- GET / HHTP/1.1
		- HOST www.example.com
	- Document structure
		- HTML
