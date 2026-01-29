# Volatility

## What It Is

Volatility is a memory forensics framework used to analyze RAM dumps from systems.

It helps investigators extract processes, network connections, loaded modules, and other artifacts from memory images.

---

## What I Use It For

- Investigating memory dumps  
- Identifying suspicious processes  
- Reviewing network connections in memory  
- Extracting forensic artifacts  
- Practicing DFIR workflows  

Volatility is one of the most valuable tools for memory forensics in DFIR work.

---

## Basic Setup

1. Install Volatility  
2. Obtain a memory dump from a lab system  
3. Identify the memory profile  
4. Run analysis plugins  
5. Review findings

---

## Core Concepts

Volatility works through **plugins** that analyze memory artifacts.

Key concepts:

- Memory profiles (OS identification)  
- Process analysis  
- Network artifact analysis  
- Artifact extraction  

Understanding plugin usage is critical.

---

## Common Workflow

### Basic Investigation Flow

1. Identify memory image info  
2. List running processes  
3. Check network connections  
4. Look for suspicious activity  
5. Extract relevant artifacts

---

## Troubleshooting

Plugins not working:
- Verify correct OS profile  
- Confirm memory image integrity  

No results:
- Try alternate plugins  
- Double-check image type

---

# Commands

---

## Image Info

Identify OS profile:

volatility -f memory.img imageinfo

---

## Process Analysis

List processes:

volatility -f memory.img --profile=PROFILE pslist

Process tree view:

volatility -f memory.img --profile=PROFILE pstree

---

## Network Analysis

Network connections:

volatility -f memory.img --profile=PROFILE netscan

---

## DLLs and Modules

Loaded DLLs:

volatility -f memory.img --profile=PROFILE dlllist

---

## File Extraction

Dump files:

volatility -f memory.img --profile=PROFILE dumpfiles

---

## Lessons Learned

- Memory contains valuable artifacts  
- Correct profile selection is critical  
- Process and network analysis reveal a lot  
- Memory forensics builds strong DFIR skills
