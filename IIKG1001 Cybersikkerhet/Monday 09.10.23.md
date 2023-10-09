# Threats, vulnerability and software security 

## Threats 
- What is a threat?
	- What is the differences between a conscious and unconscious threat?
	- What or who is a threat actor?
	- What does advanced persistent...

`If you know the enemy and know yourself, you need not fear the result of a hundred  
`battles  
``Sun Tzu

### What is a threat?
**ISO 27002**
- Threat - a potential cause of an unwanted incident that may occur to an asset or organization

- Incident - A single or a series of unwanted or unexpected events that have a significant probability of compromising business operations and threatening information security.

- Event - An identified occurrence of a system, service or network state indicating a possible breach of policy or failure of controls, or an unknown relevant situation.

- Asset - Anything that has value to the organization.

- Any circumstance or event with the potential to adversely impact organizational operations (including mission, functions, image, or reputation),organizational assets, individuals, other organizations, or the Nation through an information system via unauthorized access, destruction, disclosure, modification of information, and/or denial of service. *NIST*

- Any circumstance or event with the potential to adversely impact an asset through unauthorized access, destruction, disclosure, modification of data, and/or denial of service. *ENISA*

- A threat can be anything, whether physical or abstract, if it has the potential to adversely affect an object or system. *DS2020*


### Types of threat
- _Unconscious_ - Hurricanes, rain, accidents and mistakes.
- _Conscious_ - An actor is behind the threat.
- Attacks can originate from within an organization or from outside of the organization.
- *internal threats* 
	- Mishandle confidential data. 
	- Threaten the operations of servers or network devices
	- Facilitate attacks by connecting infected USB media.
	- Accidentally invite malware via malicious email or websites
- *External threats*
	-  External threats increase when you are connected
	- 5,4 billion potential attackers worldwide ([June'22](https://www.internetworldstats.com/stats.htm))
	
| Compromises to intellectual property     |
|-----------------------------------------|
| Deviations in quality of service         |
|-----------------------------------------|
| Espionage or trespass                   |
|-----------------------------------------|
| Forces of nature                         |
|-----------------------------------------|
| Human error or failure                  |
|-----------------------------------------|
| Information extortion                    |
|-----------------------------------------|
| Sabotage or vandalism                    |
|-----------------------------------------|
| Software attacks                         |
|-----------------------------------------|
| Technical hardware failures or errors   |
|-----------------------------------------|
| Technical software failures or errors   |
|-----------------------------------------|
| Technological obsolescence               |
|-----------------------------------------|
| Theft                                   |

### Threat actors
-   Opportunity
	 - Targetted actors: determined to find and exploit opportunities in a specific goal
	 - Stuxnet, Ukraine-Russia conflict
- Opportunistic, but later targeted
- Opportunistic: often interested in values they can obtain from more than one company, in the form of financial gain.
- Chaos actors: Not targeting their victims
	-  Wannacry.

#### Intention
- **Pure curiosity
- **Financially motivated
	- Extortion of ransom, CEO fraud.
- **Politically motivated
	- Spread a political message, against a specific issue.
- **State-motivated
	- Highest motives and highest privileges.

#### Capability
- **Advanced skills
	- Can develop very advanced tools and create exploits.
- **Generic, open access skills
	- Using available, open source tools.
	- Possible defense mechanisms to detect the tools used.
- **The gray zone
	- People with high capabilities choose low-quality tools.
	- People with low to average capabilities get advanced tools.

#### Categories
-  **Amateurs**, limited skills, use existing tools to attack.
	- Script kiddies - just curious, or try to demonstrate their skills.
-  **Hackers**, break into computers/networks to gain access.
	- White hats aim to discover weaknesses in the system.
		- They take prior permission and results are reported to the owner.
- **Black hats** take advantage of any vulnerability for illegal personal, financial or political gain.
- **Gray hats** are between white and black hat attackers.
	- Some may report the vulnerability to the owners, others publish it online so that other attackers can exploit it.

##### Organized hackers
- Cyber criminals - groups of professional criminals focused on control, power, and wealth.
	-  Highly sophisticated and organized, cybercrime as a service
- Hacktivists make political statements to create awareness to issues that are important to them.
- State-sponsored attackers gather intelligence or commit sabotage on behalf of their government.
	-  Espionage, sabotage
	-  Highly trained and well-funded
	-  Their attacks are focused on specific goals beneficial to their government.

### APT
- Threat actors.
- Prober tools and skills to practice a range of (advanced) techniques.
- Logistics and resources to exercise adaptability and persistence.
- Choose the attack vector in the easiest way possible.


#### Cyber attacks 
##### Passwords 
-  **Social engineering** - using social skills to convince people to reveal access credentials or other valuable information to an attacker.
- **Brute force password** attack - guessing a password by trying all combinations of characters and numbers.
-  **Dictionary attack** - Attempts to narrow the range of possible passwords by using a list of common ones, including attempts based on the target's personal information.
- **Phishing** - when a malicious party sends a fraudulent email disguised as a legitimate, trusted source
	- *Spear-phishing*: highly targeted phishing attack
- **Smishing (Short Message Service phishing)** - phishing using text messaging on mobiles
	- Criminals impersonate a legitimate source in order to gain trust
- **Pharming** - impersonation of a legitimate website in an effort to deceive users into entering their credentials.
-  **Whaling** - a phishing attack that targets high profile targets within an organization
	- Senior executives, politicians or celebrities.

##### Networks
- **Sniffing** - online version for eavesdropping
	- Helps examine all network traffic, even if not addressed to them
	- Can target a specific protocol, service, or even char. string
	- Might be used by network administrators for troubleshooting
-  **Spoofing** - impersonation attack on a trusted relationship between two systems
	- If two systems accept the authentication accomplished by each other, a logged on user may access the other one
-  **Man-in-the-middle (MitM) attack** - steal information while intercepting communications between computers
	- Might also manipulate messages and relay false information
	- Full control over a device without the user's knowledge
-  **Man-In-The-Mobile (MitMo)** - the mobile version

### Vulnerabilities

#### Definitions 
- **ISO 27002**
	- Vulnerability - a weakness of the system, through which a threat can harm an asset
- **Generally speaking**
	- An asset is what we're trying to protect.
	- A threat is what we're trying to protect against
	- A vulnerability is a weakness or gap in our protection efforts.

Threats are always present, whereas attacks are only
related to actual events.

#### Heartbleed
- OpenSSL vulnerability,
- Associated with heartbeat functionality march 2012
	- Checks if the message is still on the other end.
![[Pasted image 20231009090133.png]]
- Discovered only in April 2014 - unintentional???

![[Pasted image 20231009090233.png]]

#### What is a vulnerability?
- A vulnerability is a weakness that could compromise the security of an ICT system.
	- Several definitions define different categories of vulnerabilities
- Can originate from various stages and aspects of a system
	- Acquisition, design, implementation, administration, upgrade, use or termination.
- It also depends on which threat actors we realistically face.
	- Defining vulnerability as the probability that a threat capability exceeds the resistance capability.
- Today's advanced threats could potentially be used by less advanced threat actors in the future
	- Intentions of advanced threat actors may change.

##### Timeline
![[Pasted image 20231009091832.png]]
Complexity is security's worst enemy
- Zero-day: when the system supplier or the like first became aware of the vulnerability
	- 0-day attack: attacks that exploit such 0-day vulnerabilities
- Attack surface: sum of everything an attacker can use to influence or extract information from the system
	- Depends on the starting point

##### How severe is a vulnerability
-  Common Vulnerability Scoring System (CVSS)
	- a standard for expressing the severity of vulnerabilities
	- a numerical score, translated into a qualitative representation (such as low, medium, high, and critical)
- CVSS gives a baseline score
	- Based on how easy it is to exploit the vulnerability and the consequences of this for the security level overall
	- Can be time-dependent
		- Quality and availability of the attack code through time
		- Security fixes available
- Can be environment-dependent
	- The available effective countermeasures.
	- Consequences from the vulnerable system.