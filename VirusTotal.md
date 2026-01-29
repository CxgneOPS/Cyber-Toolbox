# VirusTotal

## What It Is

VirusTotal is an online threat intelligence platform used to analyze files, hashes, domains, and IPs for malicious activity.

It aggregates results from multiple security vendors to provide reputation and detection insights.

---

## What I Use It For

- Checking file and hash reputation  
- Investigating suspicious domains and IPs  
- Gathering threat intelligence context  
- Supporting alert triage decisions  
- Practicing SOC investigation workflows  

VirusTotal is one of the most valuable tools for quick threat intelligence lookups.

---

## Basic Setup

1. Create a free VirusTotal account  
2. Access web interface  
3. Submit file, hash, domain, or IP  
4. Review detection results and details

---

## Core Concepts

VirusTotal works through **multi-engine analysis and reputation data**.

Key concepts:

- Hash lookups  
- File scanning  
- Domain/IP reputation  
- Vendor detections  

Understanding reputation vs. confirmed maliciousness is critical.

---

## Common Workflow

### Basic Investigation Flow

1. Identify suspicious indicator  
2. Search hash/domain/IP in VirusTotal  
3. Review detection ratio  
4. Check behavior and relations tabs  
5. Use results to guide investigation

---

## Troubleshooting

No results found:
- Try alternate hash type  
- Submit file for analysis  

Conflicting results:
- Review vendor details  
- Look at behavior data, not just score

---

# Commands

---

## Web Usage

Search hash:

Paste hash into search bar

Upload file:

Upload file via web interface

---

## VT CLI (if installed)

Scan file:

vt scan file.exe

Get report:

vt report <hash>

---

## Lessons Learned

- Detection ratios require context  
- One vendor detection does not confirm malware  
- Relations tab provides valuable pivots  
- Threat intel enrichment improves investigations
