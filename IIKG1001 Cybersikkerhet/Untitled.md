# IIKG1001 
## Week 41 
### 
Lab Exercise  **Goals:** 
1. Become familiar with nmap commands. 
2. Scan and analyze networks. Learn about connected devices. 
3. Enjoy and have fun!  **Description:** In this week's lab, you will learn basic usage of nmap and analyze your network with it. Videos are provided in this week’s lab under Resources, but you will need to use the Nmap scan profiles to solve the tasks.  **Disclaimer:** Nmap is a powerful tool, but it has legal limitations. You must have permission from the owner or manager before using nmap on the network, thus you can use it on your own private network. This also means you must not use the tool on public networks. In our lab, we will use SkyHigh to practice with nmap. Please use your SkyHigh VM for the exercises.  **Installation:** Update your local repository: ```shell sudo apt update`

Install nmap:

shell

`sudo apt install nmap`

**Commands:** Syntax: `nmap [ <Scan Type> ] { <target specification> }` Scan types:

- Ping scan: `-sn`
- Quick scan: `-F`
- Intense scan: `-A –v`
- Learn more about the settings: `man nmap`
- The ‘-Pn’ option might be necessary to complete/receive feedback. It is used to skip host discovery and will treat every host as online. Useful with clients that may not respond to pings. For more about scan types, visit [nmap.org](https://nmap.org)

**Resources:**

- [What is nmap?](https://youtu.be/3Ab1gw8vQjg)
- [More nmap commands](https://youtu.be/5tzp9QzwnUQ?t=112)

**Task 1. Port States** Find your local IP address and use nmap with it:

Nmap scan report for 192.168.10.2
Host is up (0.00056s latency).
Not shown: 999 closed ports
PORT   STATE SERVICE
53/tcp open  domain

Nmap scan report for 192.168.10.3
Host is up (0.00060s latency).
Not shown: 999 closed ports
PORT   STATE SERVICE
53/tcp open  domain

Nmap scan report for host-192-168-10-149.openstacklocal (192.168.10.149)
Host is up (0.00035s latency).
Not shown: 999 closed ports
PORT   STATE SERVICE
22/tcp open  ssh

`nmap [IP address]`

Explain what the following port states mean:

- open
	this indicated that nmap where able to establish a connection to the port on the system, this means that the system is actively listening and accepting connections.   
- closed
	seeing as it is closed it can indicate that there is a firewall or security policy blocking the signal to reach the port. 
- filtered
	it means that nmap was unable to determined if the port is open or closed, it does not receive any information back.  
- unfiltered
	nmap was able to determined the state of the port and it is neither closed or filtered.

**Task 2. Scan Types** For this task, it is useful to look up the available scan types or the man page. 

Use the scan types to complete the following tasks: a. Using the CIDR notation, scan the first 64 IP addresses and see which hosts are up. 

`nmap -v 192.168.10.0-63`

b. Perform a quick scan on one of the VMs in your group or to this lab’s responsible TA’s IP (10.212.168.186). How many hops were performed to reach the target IP, and how long did that take?

`TRACEROUTE (using port 80/tcp)
`HOP RTT     ADDRESS
`1   4.27 ms host-192-168-10-1.openstacklocal (192.168.10.1)
`2   4.20 ms 10.212.168.186

c. Suppose we have an unidentified device on our network that behaves abnormally. We do not know exactly what the device’s IP address is. Which scan type(s) can we use to identify the device? You can use more than one nmap command to identify and analyze the device.

1. **Ping Scan (-sn)**:
    
    - This is the simplest and fastest scan. It can be used to discover live hosts on the network without scanning open ports.
    - It helps you identify which IP addresses are active on the network.
    - Example: `nmap -sn 192.168.1.0/24`
2. **OS Fingerprinting (-O)**:
    
    - This scan type tries to identify the operating system running on the device based on various characteristics.
    - It can help you determine the type of device based on the OS fingerprint.
    - Example: `nmap -O [target]`
3. **Service Version Detection (-sV)**:
    
    - This scan attempts to identify the specific services and their versions running on open ports of the target device.
    - It can give you information about the applications or services the device is running.
    - Example: `nmap -sV [target]`
4. **Aggressive Scan (-A)**:
    
    - This is a comprehensive scan that includes OS detection, version detection, and script scanning.
    - It can provide extensive information about the target device.
    - Example: `nmap -A [target]`
5. **Full Port Scan (-p-)**:
    
    - Scanning all 65,535 ports on a device can help you identify any open ports and services that might not be discovered with a standard port scan.
    - Example: `nmap -p- [target]`
6. **Script Scanning (--script)**:
    
    - Nmap has a variety of built-in scripts that can be used to gather additional information about a device.
    - You can use specific scripts to identify services, vulnerabilities, or other characteristics of the device.
    - Example: `nmap --script=default [target]`


**Task 3. Scanning a Target Device** 
Our target device has the following IP address: 10.212.168.186. This target runs a service (not ssh) on an unknown port between port 1 and 100. Scan the device to find the following: 

a. What port number does the service run on? 
	80/tcp open  http

b. What service is it? Figure out what software might be running on this port and its version. 
	80/tcp open  http    Apache httpd 2.4.52 ((Ubuntu))

c. What operating system does this device use? 
	Aggressive OS guesses: Linux 3.1 - 3.2 (94%), Linux 4.1 (93%), Linux 3.12 (92%), Linux 2.6.36 - 2.6.39 (91%), Linux 3.10 (91%), Crestron XPanel control system (90%), Linux 2.6.32 - 3.2 (89%), Linux 3.14 (88%), Linux 3.16 (88%), ASUS RT-N56U WAP (Linux 3.4) (87%)

d. Download the file this service provides. (Hint: use curl or wget)
	wget 


**Task 4 Legality** Some argue that port scanning should be illegal, while others argue that it should be legal. Answer the following questions. 

a. Why should using Nmap be legal? 
	it provide a good tool to monitor a network and keep it safe.
b. Why should using Nmap be illegal? 
	it provide a tool for people who have ill intent to monitor illegally and find 
c. What are your personal thoughts about Nmap’s legality? Write a sentence or two explaining them.
i think it it should be legal as it provide a good tool to understand and monitor the network, it's powerful so it has to be used with care. so not everyone should be able to use it without some kind of understanding. so in my opinion it should be legal but not for everyone.      