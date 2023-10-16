# Secure protocols 
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

## How does HTTPS work exactly ![[Pasted image 20231016085346.png]]

## OpenSSL
- OpenSSL is **an open source software library** that offers a range of cryptog
