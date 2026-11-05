Task 1: Scan Your Local Network for Open Ports Using Nmap

Objective

To discover active devices and open ports on a local network using Nmap and understand basic network reconnaissance and security risks.

Tools Used

- Nmap 7.98
- Windows 11
- Command Prompt

Network Information

- Local IP Address: 192.168.1.34
- Subnet Mask: 255.255.255.0
- Default Gateway: 192.168.1.1
- Network Range: 192.168.1.0/24

Procedure

1. Installed Nmap on Windows.

2. Identified the local IP address and network range using the "ipconfig" command.

3. Performed a TCP SYN scan using the following command:
   
   "nmap -sS 192.168.1.0/24"

4. Identified active devices and their open ports.

5. Saved the scan results using:
   
   "nmap -sS 192.168.1.0/24 -oN scan_results.txt"

6. Researched common services running on the discovered open ports.

7. Identified potential security risks associated with exposed services.

Open Ports Identified

Port| Protocol| Service
135| TCP| MSRPC
139| TCP| NetBIOS-SSN
445| TCP| Microsoft-DS (SMB)
3306| TCP| MySQL
5432| TCP| PostgreSQL
7070| TCP| RealServer

Potential Security Risks

- Port 135: May expose Windows remote procedure call services.
- Port 139: May expose NetBIOS network services.
- Port 445: May create risks related to unauthorized file sharing and SMB vulnerabilities.
- Port 3306: May expose MySQL database services.
- Port 5432: May expose PostgreSQL database services.
- Port 7070: May expose an application service that requires further investigation.

Security Recommendations

- Close unnecessary open ports.
- Use firewall rules to restrict access to required services.
- Use strong passwords and authentication.
- Keep operating systems and applications updated.
- Restrict database access to trusted devices.
- Disable unused network services.

Result

Successfully performed a TCP SYN scan on the local network using Nmap, identified active devices and open TCP ports, researched the associated services, and saved the scan output in a text file.

Note

Wireshark packet analysis was optional and was not performed.

The scan was conducted on my own local network.

Repository Contents

- "scan_results.txt" – Contains the saved Nmap scan results.
- "Screenshots/" – Contains screenshots documenting the practical steps.
- "README.md" – Contains the task description, procedure, findings, and security recommendations.
