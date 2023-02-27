# Network-Security-Implementation
Group Project to create secure Cisco modules that can transfer data to provincial offices and then to the head office in Ottawa.

Collaboratively worked on submitting a network design outlining a secure wired\wireless network resistant to cyberattacks, that can connect various IOT equipment for monitoring conditions across each province/territory back to their capital office and then to the main office in Ottawa. 

•	Design Considerations:
o	Each modular package should be able to connect 24 wired and 24 wireless devices. Traffic from the IOT devices is expected to be FTP\HTTP based with TELNET\SSH\HTTP being used to provide remote control.

•	What We Implemented:
o	Configured IP Addressing for each provincial offices: IP ranges, subnet masks, and WAN IDs.
o	Each module was configured with the following:
	1 WLC
	RADIUS Server
	1 Firewall
	1 Router
	2 Switches
	1 Wireless Access Point
o	Designed a network diagram showing interfaces/IPs for all provincial head offices connected to the main (Ottawa Office)
o	The cost of all hardware was estimated per module and province and turned out to be $3470 per module, which was pretty affordable in terms of scalability.

•	Security Considerations:
o	Static ARP tables, switch security, encryption, network isolation to avoid ARP Poisoning Attacks.
o	PortFast feature and enabling BPDU Guard to prevent STP attacks.
o	Port Security and MAC assigning to prevent MAC Address Flooding/Spoofing.
o	DHCP Snooping to prevent DHCP Spoofing.
o	VLAN tagging and removing unused trunk ports to prevent VLAN Hopping attacks.
o	Zone Based Firewalls to disable data going to public.
o	ACLs for increased security and disabling unwanted protocols.
o	IPSec Remote Access VPN using HMAC-MD5 algorithm to keep our IPSec standards updated without the need to patch existing IPSec standards.
o	AES-256 encryption to maintain cryptography standards.
o	Cisco IOS Login Enhancements to block DoS attacks.
o	Restricted Physical Access
o	Change SSIDs instead of using defaults.
o	ASA Firewall set up in each module.
o	Principle of Least Privilege
o	Using IDS/IPS and following Cybersecurity frameworks.

•	Wireless Considerations: 
o	Site-to-Site VPNs and using OpenVPN for users.
o	WLC in each province and AP in each module.
o	2 networks: one for employees and one for guests.
o	Atleast WPA2 authentication to accommodate for legacy devices, WPA3 recommended.
o	Securing of Aps to prevent attacks like piggybacking.

•	Authentication:
o	Recommended RADIUS Server authentication over TACACS+ authentication due to the following reasons:
o	It supports a wide range of devices. In a big enterprise network like ours, we’d by limited by just Cisco devices if we opt for TACACS+.
o	Encrypts all communication.
o	Authentication and Authorization is recorded.
o	Secure and protocol exchanges are encrypted.
o	Logging for warnings, and more critical events was enabled.

Achieved 97%, highest in the class.

