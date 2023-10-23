# Organizational aspects

### Organizations
Technical definition
- Stable, formal social structures that take resources from the environment and process them to produce outputs
	- Capital & labor as production factors
	- Transformed into products/services
	- Consumed by environments in return for supply inputs
- Behavioral definition 
	- · A collection of rights, privileges, obligations, and responsibilities balanced over a period of time through conflict and conflict resolution.
- **Differences between the views
	- Technical view focuses on how inputs are combined when technology changes are introduced
	- Behavioral view suggests involving much more than a technical rearrangement of machines or workers.
		- Implementing a new system
	- Technical and behavioral views are not contradictory.
#### Features of an organization
- Organizations are devoted to the principle of efficiency
	- Maximizing output using limited inputs
- Other features:
  ![[Pasted image 20231023084323.png]]
- **Routines and Business Processes
	- · Precise rules, procedures, practices, developed to cope with all expected situations.
		- Standard operating procedures.
	- Business processes are collections of such routines.
- **Organizational culture 
	- Foundational, unquestioned assumptions that define organization's goals and products.
	- A powerful unifying force that restrains political conflict and promotes common understanding.
	- *Example: University life
		- Professors know more than students.
		- The reason students attend college is to learn.
		- Classes follow a regular schedule.
	- Organizational culture vs new technologies/systems.
		- Technology is often stalled while the culture slowly adjusts.
- **Organizational Environment
	- A reciprocal relationship
	- Organizations are open to, and dependent on, the social and physical environment
	- Organizations can influence their environments
	- Environmental vs organizational change
		- 10% of the Fortune 500 companies from 1919 do exist today
- Organizational Structures
![[Pasted image 20231023085140.png]]

#### Competitive advantage 
- These firms have a competitive advantage
	- Access to special resources, that the others do not
	- Able to use common resources more efficiently
- Higher revenue growth, profitability or productivity
*How do organizations achieve competitive advantage?

**Competitive strategies
- **Low-cost leadership
	- Achieving lowest operational costs and prices
		- Walmart and its inventory replenishment system
- **Product differentiation
	- Enable new products/services or improve convenience for existing ones to the customers > Amazon 1-click shopping.
- **Focus on market niche
	- Enable a specific market focus, serve to that market better
- **Connect better with customers and suppliers.

#### Protecting the organization
- **To protect against every cyberattack is not feasible
	- The expertise needed can be expensive
	- Attackers will always find new ways to target networks.
	- The priority will be how quickly the security team can respond
- **Consequences.
	- Vandalism.
		- Posting untrue information.
	- Reputation ruined.
	- Revenue lost.
	- Information lost or theft.
	- Leaked confidential documents, trade secrets and IP.
- **Total costs are difficult to access.

#### Security appliances and tools 
- **No single security technology will solve all security needs
	- A whole variety of tools and appliances to implement
	- All security appliances and tools need to work together
		- Most effective when they are part of a system
- **Categories of security appliances
	- Routers
	- Firewalls
	- Intrusion Prevention Systems
	- Virtual Private Networks
	- Antivirus/Antimalware
	- Other devices
		- web & email, access control, decryption, management system
- **Firewalls
	- · Firewall - designed to control, or filter communications that are allowed in or out a device or network
 ![[Pasted image 20231023090446.png]]
- **Two main categories
	- Host-based firewall - installed on a single computer with the purpose of protecting that one computer.
	- Network-based firewall - stand-alone network device that protects an entire network of computers and all of the host devices there.
- **Port scanning
	- Probe a computer, server or any network host for open ports.
		- Each application running on a device has an identifier.
			- Port number, used on both ends of the transmission.
- Port-scanning can be used maliciously or harmlessly.
	- Reconnaissance tool to identify the OS and services running.
	- Network administrators verify the network security policies.
- Port-scanning, a precursor to a network attack.
	- Should not be done on public servers on the Internet or on acompany network without permission.
- Zenmap
	- Includes Nmap, a port-scanning tool.

#### Chasing the threats
- **Cyber Kill Chain
  ![[Pasted image 20231023091530.png]]
- **Stages
	- Reconnaissance - gathering information about the target
	- Weaponization - creating the exploit and malicious payload
	- Delivery - sending the exploit and malicious payload
	- Exploitation - The exploit is executed
	- Installation - Malware and backdoors are installed
	- Command and Control - Remote control of the target
	- Action - information theft or additional attacks on other devices from within the network
- **Important questions
	- What are the attack indicators at each stage of the Kill Chain?
	- Which security tools are needed to detect the attack indicators at each of the stages?
- Are there gaps in the company's ability to detect an attack?
**Increasing efforts and costs after each stage.

#### Behavioral approach 
- **Behavior-based security
	- A threat detection form that uses informational context to detect anomalies in the network.
		- Not relying on known malicious signatures
	- Involves capturing and analyzing the flow of communication between a network user and a local, or remote destination.
		- Reveal context and patterns of behavior
		- Discover attack presence by a change from normal behavior
	- Honeypots, behavior-based detection tools
		- Lure the attacker in by appealing to his predicted behavior
		- When inside, the network administrator use the captured information to gain more knowledge and build a better defense.
- **Intrusion Detection System (IDS)
	- A dedicated network device, or a single tool in a server or firewall that scans data, looking for malicious traffic.
		- IDS will log the detection and alert the network administrator.
	- It does not take action
		- The job of the IDS is merely to detect, log and report.
	- The scanning process creates latency
		- Usually placed offline, separate from regular network traffic.
		- Data is copied by a switch and then forwarded to the IDS.
	- IDS can be installed on top of a host operating system.
- **Intrusion Prevention System (IPS)
	- Able to block/deny traffic based on a rule or signature match.
	- Example: Snort.
		- Commercial version, Cisco's Sourcefire.
	- Features
		- Perform real-time traffic and port analysis,
		- Logging, content searching and matching,
		- Can detect probes, attacks, and port scans.
		- Integrates with reporting, performance and log analysis tools.
- **Others
	- Security Information and Event Management (SIEM)
		- Software that collects and analyzes security alerts, logs and other real time and historical data from security devices on the network
- **Data Loss Prevention (DLP) Software
	- Software or hardware system designed to stop sensitive data from being stolen from or escaping a network.
	- May focus on file access authorization, data exchange, data copying, user activity monitoring, and more.
	- Designed to monitor and protect data in all states:
- data in-use, data in-motion and data at-rest.

#### A Continuous Learning Framework
- In 2016, Gartner released a security model
	- based on four key principles that continuously inform one another to create a proactive process for securing applications.
- This approach does not focus on one specific threat; it's a mindset that allows IT to keep evolving along with threats.
- It starts with Prevent and completes with trying to Predict.

#### The security Playbook
- Collection of repeatable queries (reports) against security event data sources that lead to incident detection and response
- Used to accomplish following actions
	- Detect malware infected machines.
	- Detect suspicious network activity.
	- Detect irregular authentication attempts.
	- Describe and understand inbound and outbound traffic.
	- Provide summary information (trends, statistics, and counts)
	- Provide usable and quick access to statistics and metrics.
	- Correlate events across all relevant data sources.

#### Building for the future
- Computer Security Incident Response Team (CSIRT)
	- Receive, review, and respond to security incident reports
		- US-CERT
		- APCERT
		- Asia Pacific Computer Emergency Response Team
		- FiRST
		- CERT-EU
		- UNITED STATES COUPUTER EMERGENCY READINESS TEAM

- Primary mission - help ensure company, system, and data preservation by performing comprehensive investigations into computer security incidents
	- NORCERT