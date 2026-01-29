# Wireshark

## What It Is

Wireshark is a network protocol analyzer used to capture and inspect network traffic in real time.

It allows deep visibility into packets, protocols, and communications between systems.

---

## What I Use It For

- Inspecting network traffic  
- Investigating suspicious connections  
- Learning protocol behavior  
- Validating detection ideas  
- Analyzing potential C2 traffic  

Wireshark is one of the most valuable tools for network visibility in a SOC environment.

---

## Basic Setup

1. Install Wireshark  
2. Launch and select network interface  
3. Start capture  
4. Apply filters to narrow results

---

## Core Concepts

Wireshark works around **packet capture and filtering**.

Key concepts:

- Capture filters (filter before capture)  
- Display filters (filter after capture)  
- Protocol analysis  
- Packet inspection  

Understanding filters is critical for efficient investigations.

---

## Common Workflow

### Basic Investigation Flow

1. Start packet capture  
2. Apply display filters  
3. Identify suspicious traffic  
4. Follow TCP/UDP streams  
5. Review payload and endpoints

---

## Troubleshooting

No packets captured:
- Verify correct interface selected  
- Check permissions  
- Ensure traffic exists on network  

Too much noise:
- Use capture or display filters  
- Focus on specific IPs or protocols

---

# Commands

---

## Capture Basics

Start capture:

Select interface → Click Start

Stop capture:

Click Stop button

---

## Display Filters

Filter by IP:

ip.addr == XXX.XXX.XXX.XXX

Filter by protocol:

tcp  
udp  
dns  
http

Filter by port:

tcp.port == XXXX

Filter DNS traffic:

dns

---

## Stream Analysis

Follow TCP stream:

Right-click packet → Follow → TCP Stream

Follow UDP stream:

Right-click packet → Follow → UDP Stream

---

## Exporting Data

Export objects:

File → Export Objects → HTTP

Save capture:

File → Save As

---

## Lessons Learned

- Filters make or break investigations  
- Following streams reveals hidden details  
- DNS traffic can expose suspicious behavior  
- Packet analysis builds strong intuition
