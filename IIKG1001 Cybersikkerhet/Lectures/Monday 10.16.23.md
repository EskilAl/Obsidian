# Secure protocols 
- [[#Outline|Outline]]
- [[#World Wide Web (WWW)|World Wide Web (WWW)]]
- [[#HTTP ()|HTTP ()]]
- [[#Main problem with HTTP|Main problem with HTTP]]
- [[#Another problem with HTTP|Another problem with HTTP]]
- [[#HTTPS|HTTPS]]
- [[#Transport Layer Security (TLS)|Transport Layer Security (TLS)]]
- [[#How HTTPS Provide Website Authentication|How HTTPS Provide Website Authentication]]
- [[#How HTTPS Provides Data Integrity via MAC|How HTTPS Provides Data Integrity via MAC]]
- [[#How does HTTPS work exactly|How does HTTPS work exactly]]
- [[#OpenSSL|OpenSSL]]
- [[#Secure socket shell (SSH)|Secure socket shell (SSH)]]
- [[#Differences between SSH and TLS|Differences between SSH and TLS]]
- [[#Secure File Transfer Protocol (SFTP)|Secure File Transfer Protocol (SFTP)]]
- [[#Virtual Private Network (VPN)|Virtual Private Network (VPN)]]
- [[#How does a VPN work?|How does a VPN work?]]
- [[#How a VPN provides Online Security|How a VPN provides Online Security]]
- [[#How a VPN offers Online Freedom|How a VPN offers Online Freedom]]
- [[#Some Commonly Used VPN Protocols|Some Commonly Used VPN Protocols]]
- [[#Summing Up|Summing Up]]

## Outline
• World Wide Web (WWW)
• Hypertext Transfer Protocol (HTTP)
• HTTPS
• Transport Layer Security (TLS)
• OpenSSL
• Secure Socket Shell (SSH)
• Differences between SSH and TLS
• Secure File Transfer Protocol (SFTP)
• Virtual Private Network (VPN)

## World Wide Web (WWW)
- www short for **world wide web**. it is often called "**the web**".
- WWW is a network of online content that is accessible over the internet.
	- in other words, WWW refers to all interlinked web pages on the internet.
- A web page consists of **objects.
	- Each object is **a file** (e.g., an image, a video, a HTML file) addressable by a single web
address or URL (Uniform Resource Locator).

## HTTP ()
- HTTP (**Hyper Text Transfer Protocol**) is an **application layer protocol** for the web.
- HTTP is implemented in two types of programs:
	1. Client programs, run by **web browser.**
	2. Server programs, run by **web servers.**
- HTTP defines
	- How clients request web pages from web servers.
	- How the web servers transfers web pages to the
clients.
- HTTP is a **stateless protocol**
	- Web servers do not retain or store information or status about each client for the duration of multiple requests. 
	- Reason: it simplifies webs server design.
- However, clients' state information are required for some web applications (e.g., online stores or online banks)
	- Several techniques cab be used to maintain such information.
	- For example: Cookies
		• A cookie is small piece of data stored on a user’s computer by the web browser.
		• It is used to remember users’ status information, browsing activity, and any data entered by users.
		• Web browsers will automatically include the cookie in all its subsequent requests to the web sever.
- Non-persistent HTTP connection
	- Only one object can be sent over a connection.
		- The connection is then closed.
	- Downloading multiple objects requires establishing multiple TCP connections.
	- Used by HTTP 1.0.
Persistent HTTP connection
	• Multiple objects can be sent over a single. connection between a client and a server.
	• Used by HTTP 1.1 and later versions.

## Main problem with HTTP
- HTTP is **insecure**
	- All data is sent **Plaintext without any protection.**
	- **No confidentiality** and **no privacy**
	- The data might be captured, eavesdropped, and misused by bad guys. 

## Another problem with HTTP
- Cannot tell if a website is authentic or phishing.
	- HTTP provides **no mean** to figure it out. No authentication mechanism at all. 
	- Users might be trapped to enter their personal sensitive information.

## HTTPS 
- The S in HTTPS stands for “**Secure**”.
• HTTPS provides **secure communication** over insecure networks.
	HTTPS = HTTP + TLS
	• TLS: Transport Layer Security
• HTTPS provides
	• Website Authentication
		• via **Public-key Cryptography (TLS Certificates)**
	• Data Confidentiality
		• via **Symmetric Cryptography**
	• Data Integrity
		• via **Message Authentication Code**

## Transport Layer Security (TLS)
- TLS is a cryptographic protocol designed to provide **communication security** over a computer network.
- Not only used by WWW, but also used by many other applications such as email, instant messaging, and VoIP. ![[Pasted image 20231016084041.png]]

## How HTTPS Provide Website Authentication
- HTTPS provides website authentication via **TLS certificates**.
- TLS certificates are digital certificates used to **authenticate the identify of a web site,** and they are issued by **trusted certificate authorities (CAs).
- A TLS certificate mainly contains:
	- The Domain name to which the certificate is issued. 
	- Info of the issuing CA
	- Valid dates
	- **The website's public key**
	- **The digital signature**, created by the issuing CA, that **vouches for the authenticity of this TLS certificate.
- if a website has a valid TLS certificate from a trusted CA, it means that the website is **authentic, legitimate,** and **trustable**.

## How HTTPS Provides Data Integrity via MAC
- Message Authentication Code (MAC) is a **symmetric key cryptographic technique** to verify the authenticity and integrity of a message based on hash functions.
	- a hash function is a mathematical function that takes an input and returns a fixed-size string of characters (called a hash value or a digest).
- The sender and receiver must **share a symmetric key in advance.** The key is used for both **generating** and **verifying** MAC values. 

## How does HTTPS work exactly 
![[Pasted image 20231016085346.png]]

## OpenSSL
- OpenSSL is **an open source software library** that offers a range of cryptographic functions to secure data and communications and supports both SSL and TLS.
- It is widely used for **implementation secure communication** in various applications, including web servers, email servers, virtual private networks (VPN).
- What can we do with OpenSSL?
	- **Securing Websites:** Implementing HTTPS (HTTP Secure) on web servers to encrypt data transmissions between clients and servers.
	- **Digital Certificates**: Generating and managing digital certificates, which are essential for authenticating the identity of servers and clients in secure communications. 
	- **Cryptography** Utilizing cryptographic functions for data encryption and decryption.
	- **Implementing SSL/TLS:** Supporting SSL and TLS protocols to create secure, encrypted connections in various applications, including web servers, email servers, and VPNs.
	- **Cross-Platform Secure Communication**: Enabling secure communication in software applications on multiple platforms, including Unix, Linux, Windows, and macOS.
	- **VPN implementation:** Supporting VPN protocols like OpenVPN, enabling the establishment of secure connections between clients and servers in virtual private networks. 

## Secure socket shell (SSH)
- known also as **Secure Shell.**
- Created in 1995 by Tatu Ylonen, a Finnish computer scientist. 
- SSH is a protocol designed for **secure remote access** and **administration.** 
- Key features:
- **Secure remote access:** Users can log in to remote systems and executes commands securely.
- **Authentication:** SSH uses cryptographic key pairs for user authentication. Only the user with the private key can log in.
- **Encrypted communication:** SSH encrypts data exchanged between the client and the sever. 
- **Secure File Transfer**: SSH supports secure file transfers using tools like SCP (Secure Copy Protocol) and SFTP (SSH File Transport Protocol) These allow for the transfer of files between the local and remote system securely.

## Differences between SSH and TLS 
![[Pasted image 20231016091442.png]]

## Secure File Transfer Protocol (SFTP)
- it is a network protocol designed by **IETF** (Internet Engineering Task Force) to provide **secure file access, file transfer, and file management**.
- SFTP uses the **SSH** protocol to authenticate and establish a secure connection for file transfer. With SFTP, both commands and data are encrypted.
- It is a popular and widely-used protocol transferring important, sensitive, and confidential data and files.

## Virtual Private Network (VPN)
- A Virtual Private Network (VPN) works by creating **a secure and encrypted connection,** often called **a tunnel**, between a device and a VPN server.
- This tunnel allows the clients' internet traffic to pass through the VPN server before reaching its final destination on the internet.
- Clients can get a VPN service from many VPN providers.
- Each VPN provider provides a user a VPN client software.

## How does a VPN work?
1. *VPN Client initiation* The user initiates the VPN connection by running VPN client software on his device (computer, smartphone, tablet) by specifying a VPN server to which he wants to connect.
2. *Establishing a Secure Connection:* A secure tunnel is established between the user's device and the VPN server. This tunnel is encrypted, ensuring that all data transmitted between the user and the server is protected from eavesdropping.
3. *Data Encryption*: Before the user's data leaves his device, it is encrypted.
4. *Routing Data to the VPN server:* Encrypted data packets are sent through the secure tunnel to the VPN server.
5. *Server Decryption:* The VPN server receives the encrypted data and decrypts it, returning it to its original form.
6. *Anonymization:* When the user's data exits the VPN server, it appears to originate from the server's IP address, rather than the user's IP address, thereby concealing the user's true IP address and location.
7. *Data Routing to the internet:* The VPN server sends the user's data to its intended destination on the internet. 
8. *Receiving Data:* As data returns from the internet, it is sent first to the VPN server.
9. *Encrypting Before Returning to the users:* The VPN server encrypts the data to protect it during the journey back to the user's device.
10. *Data Reaching Your Device:* The encrypted data packets are sent back to the user's device through the secure tunnel.
11. *Data Decryption:* Upon reaching the user's device, the data is decrypted, making it accessible and readable to the user.

## How a VPN provides Online Security 
- Recalled that VPN client software encrypts all users' internet traffic before it reaches the VPN server, VPN provides **online security** even when users use public Wi-Fi networks.![[Pasted image 20231016093151.png]] 
## How a VPN offers Online Freedom 
- A VPN can offer users a lot of online freedom.
- When users connect to a VPN server in certain country, they can access the internet as if they were **physically** in that country.
- This is useful because **the internet is not freely accessible everywhere.
	- Some countries censor part of the internet or impose restrictions on social media sites or online streaming services. 
	- Example:
		- China's Great Firewall blocks access to foreign websites and apps. Facebook, Google and several of the world's top news sites are all blocked in the country.
		- VPNs are the most common tools used in China to hop the county's Great Firewall
		- However, only approved VPNs are allowed.
		- Some people have already been arrested for selling VPN services in China.
		- A man was arrested for it in 2017, where he was sentenced to five and a half year in prison and fined US$76,000.

## Some Commonly Used VPN Protocols
- OpenVPN: OpenVPN is an open-source protocol known for its flexibility and strong security features.
- *L2TP/IPsec (Layer 2 Tunneling Protocol/Internet Protocol Security)*: L2TP is often used in combination with IPsec for enhanced security.
• *PPTP (Point-to-Point Tunneling Protocol):* PPTP is one of the earliest VPN protocols and is known for its ease of setup and speed. However, it is considered less secure today due to vulnerabilities, and it's not recommended for sensitive data or highsecurity use cases.
• *IKEv2/IPsec (Internet Key Exchange version 2/Internet Protocol Security)*: IKEv2 is a modern protocol known for its stability and ability to quickly re-establish connections if they are interrupted.
• *SSTP (Secure Socket Tunneling Protocol)*: SSTP is a proprietary protocol developed by Microsoft. It is designed to operate over SSL/TLS and can be used on Windows-based systems. It is often considered a secure choice for Windows users.
• *WireGuard*: WireGuard is a newer, open-source protocol known for its simplicity and efficiency.
• *SSL/TLS (Secure Sockets Layer/Transport Layer Security)*: SSL and its successor, TLS, are often used for securing web traffic (HTTPS) but can also be used as VPN protocols.
• *Shadowsocks*: Shadowsocks is a lightweight and open-source protocol designed for circumventing censorship and providing secure communication. It is popular in regions with strict internet censorship.

## Summing Up
In this lecture, we have learned:
- WWW, the Web, web pages, URL
- HTTP: Client-server model, stateless, cookies, persistent and non-persistent connections.
- HTTPS: The combination of HTTP and TLS.
- TLS
	- TLS Certificates: Signed by trusted CAs, used to provide website authenticity.
	- Message Authentication code
- Difference between SSH and TLS
- SFTP
- VPN: online security, privacy, and freedom. 