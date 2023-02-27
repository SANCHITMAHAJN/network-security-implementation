# Network-Security-Implementation
Group Project to create secure Cisco modules that can transfer data to provincial offices and then to the head office in Ottawa.

Collaboratively worked on submitting a network design outlining a secure wired\wireless network resistant to cyberattacks, that can connect various IOT equipment for monitoring conditions across each province/territory back to their capital office and then to the main office in Ottawa. 

## Design Considerations:
* Each modular package should be able to connect 24 wired and 24 wireless devices. 
* Traffic from the IOT devices is expected to be FTP\HTTP based with TELNET\SSH\HTTP being used to provide remote control.

##	How We Implemented:
*	Configured IP Addressing for each provincial offices: IP ranges, subnet masks, and WAN IDs.
*	Each module was configured with the following:
*	1 WLC
*	RADIUS Server
*	1 Firewall
*	1 Router
*	2 Switches
*	1 Wireless Access Point
*	Designed a network diagram showing interfaces/IPs for all provincial head offices connected to the main (Ottawa Office)
*	The cost of all hardware was estimated per module and province and turned out to be $3470 per module, which was pretty affordable in terms of scalability.

##	Security Considerations:
*	Static ARP tables, switch security, encryption, network isolation to avoid ARP Poisoning Attacks.
*	PortFast feature and enabling BPDU Guard to prevent STP attacks.
*	Port Security and MAC assigning to prevent MAC Address Flooding/Spoofing.
*	DHCP Snooping to prevent DHCP Spoofing.
* VLAN tagging and removing unused trunk ports to prevent VLAN Hopping attacks.
*	Zone Based Firewalls to disable data going to public.
* ACLs for increased security and disabling unwanted protocols.
* IPSec Remote Access VPN using HMAC-MD5 algorithm to keep our IPSec standards updated without the need to patch existing IPSec standards.
*	AES-256 encryption to maintain cryptography standards.
*	Cisco IOS Login Enhancements to block DoS attacks.
*	Restricted Physical Access
*	Change SSIDs instead of using defaults.
*	ASA Firewall set up in each module.
*	Principle of Least Privilege
*	Using IDS/IPS and following Cybersecurity frameworks.

##	Wireless Considerations: 
*	Site-to-Site VPNs and using OpenVPN for users.
* WLC in each province and AP in each module.
*	2 networks: one for employees and one for guests.
*	Atleast WPA2 authentication to accommodate for legacy devices, WPA3 recommended.
*	Securing of Aps to prevent attacks like piggybacking.

##	Authentication:
*	Recommended RADIUS Server authentication over TACACS+ authentication due to the following reasons:
*	It supports a wide range of devices. In a big enterprise network like ours, we’d by limited by just Cisco devices if we opt for TACACS+.
*	Encrypts all communication.
*	Authentication and Authorization is recorded.
*	Secure and protocol exchanges are encrypted.
*	Logging for warnings, and more critical events was enabled.

Achieved 97%, highest in the class.

