# Nmap (Network Mapper)

## Submitted By
- **Qusai Sakerwala** (16010122231)  
- **Himanshu Garg** (16010122238)  
- **Ayush Nayak** (16010122243)  
- **Mourvi Joshi** (16010122279)  

## Guide
**Zaheed Shaikh**  
Department of Computer Engineering  

---

## Contents
- [Introduction](#introduction)
- [Features/Characteristics](#featurescharacteristics)
- [Methodology and Results](#methodology-and-results)
- [Conclusion](#conclusion)
- [References](#references)

---

## Introduction
Nmap (Network Mapper) is a powerful tool used by network administrators and cybersecurity professionals for network exploration and security auditing. Originally developed by Gordon Lyon (Fyodor) in 1997, Nmap is an open-source utility that enables network scanning, vulnerability detection, and penetration testing. 

Nmap can:
- Discover devices connected to a network.
- Identify open ports, running services, and operating systems.
- Detect network vulnerabilities and security misconfigurations.
- Be used for penetration testing and security assessments.

With continuous updates and an active open-source community, Nmap remains a critical tool for ensuring network security.

---

## Features/Characteristics
- **Host Discovery:** Identifies active devices on a network using ICMP (ping) requests or other methods.
- **Port Scanning:** Detects open ports using various scanning techniques (TCP, UDP, SCTP).
- **Service and Version Detection:** Identifies running services and their versions to detect outdated or vulnerable software.
- **OS Detection:** Uses TCP/IP fingerprinting to determine the operating system of target devices.
- **Security Auditing:** Identifies network vulnerabilities and unauthorized access points.
- **Stealth Scanning:** Uses techniques like SYN and FIN scanning to avoid detection by firewalls and IDS.
- **Nmap Scripting Engine (NSE):** Automates vulnerability detection and security testing.
- **Zenmap (GUI for Nmap):** Provides a graphical interface for ease of use.

---

## Methodology and Results
Below are the commands used in our study to perform network scanning with Nmap:

### Checking Network Configuration
```sh
ifconfig
```
**Purpose:** Displays network interface details including IP address and subnet mask.

### IP Address Calculation
```sh
ipcalc <IP Address>
```
**Purpose:** Provides subnet mask, broadcast, and host range.

### Scanning Live Hosts on a Network
```sh
nmap -sP <Network IP>
```
**Purpose:** Identifies active devices in a subnet.

### Scanning a Range of IP Addresses
```sh
nmap <start-IP>-<end-IP>
```
**Purpose:** Scans a specified IP range.

### Scanning an Entire Subnet
```sh
nmap <subnet>
```
**Purpose:** Scans all devices within a subnet.

### Scanning Top N Common Ports
```sh
nmap --top-ports 10 scanme.nmap.org
```
**Purpose:** Scans the top 10 most used ports.

### Scanning Specific Ports Using Different Methods
```sh
sudo nmap -sT -p 80,443 <Network IP>   # TCP Connect Scan
sudo nmap -sS -p 80,443 <Network IP>   # Stealth Scan
```
**Purpose:** Checks if specific ports (80, 443) are open.

### Aggressive Scan for Detailed Information
```sh
nmap -A <IP Address>
```
**Purpose:** Performs a comprehensive scan, including OS detection, version detection, and script scanning.

### Saving Scan Output
```sh
nmap -oA output scanme.nmap.org
```
**Purpose:** Saves scan results in different formats for further analysis.

### Scanning Multiple Targets from a File
```sh
nmap -iL input_ips.txt
```
**Purpose:** Reads target IPs from a file and performs scanning.

### Using Zenmap (GUI for Nmap)
**Purpose:** Provides a graphical interface for performing and visualizing scans.

---

## Conclusion
Nmap is an essential tool for network security analysis, penetration testing, and cybersecurity research. Its ability to perform host discovery, port scanning, service identification, and OS detection makes it invaluable for security professionals. Our study demonstrated its efficiency in identifying vulnerabilities and assessing network configurations. 

With advanced scanning techniques like stealth and aggressive scans, Nmap proves to be a versatile tool for cybersecurity assessments. Its continuous updates and scripting capabilities make it a crucial resource for modern network security.

---

## References
- FreeCodeCamp - What is Nmap and How to Use It
- Official Nmap Website: [https://nmap.org](https://nmap.org)
