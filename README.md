# CyberSecurity-Internship-Task1

Task 1 – Scan Local Network for Open Ports
Objective
To perform network reconnaissance by scanning my local network and identifying open ports to understand network exposure.

Tools Used
Nmap
Command Prompt (Windows)

Step 1: Verified Nmap Installation

Command used:
nmap -v
Nmap was successfully installed and verified.

Step 2: Identified Local Network Range

Command used:
ipconfig
Network scanned:
172.20.10.0/24

Step 3: Performed TCP SYN Scan

Command used:
nmap -sS 172.20.10.0/24

Scan Summary:
256 IP addresses scanned
Active hosts detected
Open ports identified
Open Ports Discovered
Host: 172.20.10.1
Port	State	Service
21	Open	ftp
53	Open	domain (DNS)
49152	Open	unknown
62078	Open	iphone-sync
Host: 172.20.10.2
Port	State	Service
135	Open	msrpc
139	Open	netbios-ssn
445	Open	microsoft-ds

Service Analysis

FTP (21) – Used for file transfer. Can be vulnerable if not secured properly.
DNS (53) – Used for domain name resolution. Misconfiguration can lead to attacks.
MSRPC (135) – Used for Windows remote procedure calls.
NetBIOS (139) – Used for file and printer sharing.
SMB (445) – Used for Windows file sharing. Often targeted in ransomware attacks.

Security Risks Identified

Open FTP may allow unauthorized file access if not secured.
Open SMB (445) is commonly targeted by ransomware (e.g., WannaCry).
NetBIOS exposure may reveal shared resources.
Unnecessary open ports increase attack surface.
Misconfigured services may allow remote exploitation.

Conclusion

This task helped me understand:
Port scanning concepts
TCP SYN scanning
Network reconnaissance
Identification of o
