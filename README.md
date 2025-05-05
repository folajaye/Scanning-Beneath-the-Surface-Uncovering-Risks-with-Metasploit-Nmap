# Network Scanning-Uncovering Risks with Metasploit Nmap
A Technical Exploration of Network Vulnerabilities Using Integrated Security Tools

## Objective
The project's aim was to carry out a network scan as a proactive measure to determine and assess the target system's network-based attack vulnerabilities. Metasploit's connection to Nmap was employed to deliver an efficient framework for scanning and data connection during network scanning to identify open ports and services susceptible to exploitation.

## Tool used and its objective
The tool used was Nmap, through Metasploit, and its objective was to scan the local IP address with the following flags: 
	 -sC for default script execution,
	 -sV for service version detection,
	 -vv for increased verbosity,
	 and to identify open ports and service misconfiguration

## Tool Configuration
###	Metasploit and Nmap Configuration: 
- Metasploit framework was launched on the Kali Linux terminal using the “msfconsole” command
- Nmap was integrated through the “db_nmap” command within Metasploit.
- The following Nmap flags were used: -sC (script scan), -sV (version detection), and -vv (very verbose output).   
- And the local IP address
### Target IP: 
- The target IP address for the scan was the local IP: 192.168.0.100, which can be obtained using the command prompt and the syntax “ipconfig” for Windows and “ifconfig” for Linux. 
### Command: msf6 > db_nmap -sC -sV -vv 192.168.0.100

## Key Findings
Metasploit Nmap identified the local machine showed multiple open ports alongside operational services during the Nmap scan. The discovered information creates an important understanding of attack points while demonstrating why proper security settings need to be enabled.

## Recommendation
### Immediate Remediation Actions
- Immediate assessment of active services on ports 135, 139, 445, 902, 912, and 8089 is necessary; deactivate non-essential services.
- Enhance firewall policies to impose restrictive filters for the mentioned ports.
- Limit access to ports 902, 912 (VMware), and 8089 (Splunk) to approved networks and IP addresses only.
- Urgent configuration strengthening is required for SMB services operating on ports 139 and 445.
- Implement strong password policies for all accounts accessing SMB; guest access to SMB file shares must be prohibited.
- Use SMB signing technology for business-critical operations to safeguard against unauthorized data modifications.

### Long-Term Mitigation
- Network Segmentation
- Principle of Least Privilege
- Regular Vulnerability Scanning
- Security awareness training
- Endpoint Detection and Response (EDR)
- Zero Trust security models

[Full Report on Medium](https://medium.com/@folajayeabdulrahman/scanning-beneath-the-surface-uncovering-risks-with-metasploit-nmap-2b63234d8d22)











  
