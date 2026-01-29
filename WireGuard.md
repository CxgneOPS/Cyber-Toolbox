# WireGuard

## What It Is

WireGuard is a lightweight and fast VPN protocol used to create secure encrypted tunnels between systems.

It is commonly used for secure remote access and private network connections.

---

## What I Use It For

- Creating secure tunnels between lab machines  
- Securing remote access to systems  
- Isolating lab traffic  
- Practicing VPN configuration and troubleshooting  

WireGuard is a valuable tool for secure network communication in lab and real-world environments.

---

## Basic Setup

1. Install WireGuard  
2. Generate public/private keys  
3. Configure server and client configs  
4. Start WireGuard interface  
5. Verify tunnel connectivity

---

## Core Concepts

WireGuard works using:

- Public/private key pairs  
- Encrypted tunnels  
- Peer-to-peer configuration  
- Interface-based setup

Understanding keys and peer configs is critical.

---

## Common Workflow

### Basic Investigation Flow

1. Configure server peer  
2. Configure client peer  
3. Start WireGuard interface  
4. Test connectivity  
5. Monitor tunnel traffic

---

## Troubleshooting

No connection:
- Verify keys match  
- Check firewall rules  
- Confirm endpoint IP/port  

Handshake failing:
- Ensure both peers are running  
- Verify allowed IPs configuration

---

# Commands

---

## Key Generation

Generate private key:

wg genkey > privatekey

Generate public key:

wg pubkey < privatekey > publickey

---

## Interface Control

Start interface:

wg-quick up wg0

Stop interface:

wg-quick down wg0

---

## Status Checks

Show WireGuard status:

wg show

---

## Configuration Files

Main config location:

/etc/wireguard/wg0.conf

---

## Lessons Learned

- Key management is critical  
- Small config mistakes break tunnels  
- WireGuard is fast and simple once configured  
- VPN knowledge is valuable in SOC/network roles
