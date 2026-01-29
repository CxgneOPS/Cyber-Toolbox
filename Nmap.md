# Nmap

## What It Is

Nmap (Network Mapper) is a network scanning tool used to discover hosts, open ports, services, and operating systems on a network.

It is widely used for network discovery, security auditing, and exposure assessment.

---

## What I Use It For

- Discovering live hosts  
- Identifying open ports and services  
- Mapping lab environments  
- Checking network exposure  
- Validating segmentation and firewall rules  

Nmap is one of the most valuable tools for understanding network visibility in a SOC environment.

---

## Basic Setup

1. Install Nmap  
2. Choose a target (lab systems only)  
3. Run basic scans  
4. Review open ports and services

---

## Core Concepts

Nmap works through **port scanning and service detection**.

Key concepts:

- Port states (open, closed, filtered)  
- Service/version detection  
- Host discovery  
- Scan types (SYN, TCP, UDP)

Understanding scan types is critical for accurate results.

---

## Common Workflow

### Basic Investigation Flow

1. Identify target system  
2. Run host discovery  
3. Scan for open ports  
4. Detect services and versions  
5. Review findings for exposure

---

## Troubleshooting

No hosts found:

- Check network connectivity  
- Verify correct subnet  
- Try disabling host discovery (-Pn)

Slow scans:

- Reduce scan scope  
- Adjust timing options

---

# Commands

---

## Basic Scanning

Scan a single host:

nmap XXX.XXX.XXX.XXX

Scan a subnet:

nmap XXX.XXX.XXX.XXX/24

---

## Host Discovery

Ping scan only:

nmap -sn XXX.XXX.XXX.XXX/24

---

## Port Scanning

Scan specific ports:

nmap -p 22,80,443 XXX.XXX.XXX.XXX

Scan all ports:

nmap -p- XXX.XXX.XXX.XXX

---

## Service Detection

Service/version detection:

nmap -sV XXX.XXX.XXX.XXX

OS detection:

nmap -O XXX.XXX.XXX.XXX

---

## Output Options

Save output to file:

nmap -oN scan.txt XXX.XXX.XXX.XXX

Save XML output:

nmap -oX scan.xml XXX.XXX.XXX.XXX

---

## Lessons Learned

- Start small before large scans  
- Service detection adds valuable context  
- Exposure awareness is key in SOC work  
- Scanning helps understand attack surface
