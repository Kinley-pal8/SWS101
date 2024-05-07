# CAP 1: Network Penetration Testing

## Introduction

As a summary, the given scenario by sir involves the following:

1. As a Senior Penetration Tester of the Research and Utilization Branch (RUB), you will facilitate the development and implementation of procedures for cyber-attacks coordination, which will then be used for training and testing by the personnel. 
2. You may be assigned to test a server installed by instructors or college IT team in its network, prior to its release in the coming days throughout the firm. 
3. As an experienced tester, you need to leave no stone unturned and follow these steps:3.  As an experienced tester, you need to leave no stone unturned and follow these steps:
    - Search the server's opening ports for possible ways to gain access, then investigate protocols and techniques that might do so. 
    - Develop how the escalation of privileges is stealthily made and the server root access is got. 
    - Develop a report, which will contain resulting of the penetration testing, and then submit it to the Head of ICT RUB. 
 
The main goal here is to audaud the server for potential vulnerabilities, to lose control of the server gaining access to any unauthorized and gaining access by privilege escalation, in a structured way and the findings in a comprehensive report to be presented to the relevant authorities. 

## Instructions
1. Unfortunately, the server is not public accessible through the internet or local networks such as Bmobile or TashiCell. This information is being shared within GCBS college's internal network. 
2. The IP address of the given server is 10. 3.  21.  140 but in case of a change of IP address, the new IP will be announced in the Google Space Chat and recorded in the relevant document. 
3. The activity in the SWS101 course before the midterms was similar to those on the HackTheBox and TryHackMe machines; the task here is to obtain unauthorized access into college within the network. 
4. Internal organization network membership is a mandatory condition for undertaking the identified pentest engagement. 
5. The practical side of penetration testing should follow the methodologies that are used in SWS101 course exploiting the knowledge gained from TryHackMe and HackTheBox exercises. 

Finally, the main points are that the target server must be in the GCBS network, you need to know the current IP address of that server (as it may change), and use the penetration testing techniques that you have gained from following the SWS101 course to breach that internal server's security and get unauthorized access. 

# Executive Summary

The purpose of the analysis was to find out what may compromise either authorization or privilege escalation that could occur before the server public release. By performing a comprehensive assessment, several attack ways were discovered that would allow one to get the initial access to the server through the abuse of some misconfiguration or unpatched software vulnerabilities. Furthermore, a variety of privilege escalation paths were also discovered that could lead to system level takeover.
Discovered vulnerabilities at this stage of the engagement can lead to serious problems like data breaches, malware deployment, denial of service, and other threats. Those problems will happen if all the vulnerabilities are not eliminated during the engagement before going live. Immediate risk mitigation measures are strongly suggested on the class-insight and the remediations recommended in the report.


## Approach

### Methodology
1. Reconnaissance Phase
 - Nmap was used during the active reconnaissance together with other discovery tools to determine open ports, services, and their version on target server. 
 - Get hold of exploits and vulnerabilities by browsing vulnerability databases and Metasploit repository through queries. 
 
2. Exploitation Phase
 - Tried out the Metasploit Framework and its huge module library of auxiliary modules and exploits to confirm vulnerabilities and to get initial entry to the target server. 
 - I tried to be the first to identify and work on the weaknesses such as misconfigurations, unpatched software, default credentials, or other security loopholes. 
 - Carried out internal scanning and continuous reconnaissance through which additional attack vectors and privilege escalation paths were established. 
 
3. Privilege Escalation Phase
 - With leveraged manual exploitation techniques like creating custom exploits, this can alter critical software components, explore OS-level vulnerabilities and flaws in a kernel. 
 - Gained elevated privileges to attain the highest levels of access i. e.  root SYSTEM control by using different privilege escalation methods. 
 
4. Reporting Phase
 - Founding out the findings, including the identified vulnerabilities, exploitation techniques, and probable effect. 
 - Wrote a comprehensive report which gave a description of the risk mitigation and remediation plan including an overview and scope of the assessment. 
 
### Scope 

The activity carried out is a simple internal penetration test of the server at IP 10. 3. 21. on College Network, we are simulating a malicious insider who has no credentials. The specific objectives included: 

 - Revealing open live servers addresses/ports that a target server is hosting. 
 - Deciding on the appropriate visages of the services that directly interact with customers. 
 - Exploitation of vulnerabilities by mapping and scanning operations 
 - To gaining access and raising privileges are some of the attempts. 
 - The attacker connected to many Wi-Fi connection points within the College Campus, and the exposure of the ports/service varied across the segments. 

In the rules of engagement, explicitly outlawed were any acts resulting in Denial-of-Service (DoS) or data destruction. Scans and attacks were narrowed to the specific server 10. 3. 21.


### Tools
1. Nmap 
 - Assisted in the identification of a network and mapping out target network/host.
 - The scanning of TCP and UDP ports was done to detect open ports and the services that was running on the target machine. 
 - Inferred service/verson information and operating system from different Nmap scripts. 
 - The gathered data will tell us about open ports, running services, versions, and the potential vulnerabilities. 

2. Metasploit Framework 
 - Exploited an enormous database of exploits and payload users for different vulnerabilities viruses. 
 - Injected the auxiliary modules for conducting reconnaissance, scanning, and vulnerability scanning. 
 - Deployed exploit modules to gain initial access and establish a foothold on the target
 - After the exploitation phase, the attacker applies privilege escalation, pivoting and evasion modules to stay stealthy. 
 - Delivered customized payloads (e. g. Meterpreter) for remote control in these different environments. 

3. Gobuster 
- While the web scraper is designed for web content discovery and enumeration. 
- The brute forces the directories and files of a web server aiming at. 
- Discovered hidden web directories, files, and prospective door-twists. 
- Exploited the wordlist and the client-specific fuzzing techniques for better enumeration. 

Additionally, other tools and techniques were utilized, including:
 - Privilege Escalation Tools (e.g., LinEnum, WinPEAS) for identifying and exploiting misconfigurations and vulnerabilities leading to privilege escalation
 - Social Engineering Techniques for gathering sensitive information and exploiting human vulnerabilities
 - Manual Exploitation involving developing custom exploits, shellcode, and leveraging publicly available proof-of-concept code



## Network Penetration Test Assessment Summary

### Exploitation List

- PHP CGI Argument Injection (Port 80 - HTTP)
- UnrealIRCd 3.2.8.1 Backdoor Command Execution (Ports 6667 and 6697 - UnrealIRCd)
- PostgreSQL Payload Execution (Port 5432 - PostgreSQL)
- VSFTPD 2.3.4 Backdoor Command Execution (Port 21 - FTP)
- "username map script" Command Execution (Ports 139 and 445 - SMB)
- VNC Brute Force Login (Port 5900 - VNC)
- Java RMI Server Insecure Deserialization (Ports 1099 and 49104 - Java RMI)

## Conclusion and Remediation Summary

This test has uncovered many serious deficiencies and discrepancies in the company’s server setup, which spans across various Wi-Fi segments. Exploitation was interchangeably obtained via multiple undefended ways that were made possible due to the old software vulnerabilities, logic flaws, and the use of weak/default credentials. The internal security configuration was overwhelmingly notional at all as there were uncountable open ports/services opened internally for use by the employees that actually raised many questions as to how effective the security was and how vulnerable it was to both internal and possibly external threats. Before introducing production deployment, remediation steps are necessary, which consist of consistent firewall rules, credentials management, patching, server hardening and additional safeguards. 

Additionally, some suggestions include updating all software to the latest secure versions, using strong authentication methods, encryption of services with SSL/TLS and network security with firewalls, web application firewalls, and network segmentation, conducting active monitoring of logs for suspicious activities, hardening system configuration, establishing vulnerability management process, and verifying software integrity. These inclusive remedies that touch on software updates, authentication, encryption, network control, monitoring, hardening, vulnerability management and integrity verification, are providing a high level of mitigation and some improvement to the overall security posture. 











