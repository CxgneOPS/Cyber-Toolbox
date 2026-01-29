# Metasploit

## What It Is

Metasploit is a penetration testing framework used to test, validate, and demonstrate security vulnerabilities in systems.

It provides tools for exploitation, payload delivery, and security testing in controlled environments.

---

## What I Use It For

- Practicing exploitation in lab environments  
- Understanding how attacks work  
- Learning how vulnerabilities are abused  
- Testing detection visibility in my lab  
- Improving defensive awareness  

Metasploit is useful for understanding attacker behavior in a controlled SOC lab environment.

---

## Basic Setup

1. Install Metasploit  
2. Launch Metasploit console  
3. Select lab target systems only  
4. Load modules for testing  
5. Review results safely

---

## Core Concepts

Metasploit works through **modules**.

Key concepts:

- Exploit modules  
- Auxiliary modules  
- Payloads  
- Sessions  

Understanding module structure is critical.

---

## Common Workflow

### Basic Investigation Flow

1. Identify lab target  
2. Search for relevant module  
3. Configure module options  
4. Run module in lab  
5. Observe behavior and logs

---

## Troubleshooting

Module not working:
- Verify correct target  
- Check required options  
- Confirm lab connectivity  

No session created:
- Validate payload settings  
- Check firewall rules

---

# Commands

---

## Console

Start Metasploit:

msfconsole

---

## Module Searching

Search for modules:

search <keyword>

---

## Module Usage

Use module:

use <module_name>

Show options:

show options

Set option:

set <option> <value>

Run module:

run

---

## Sessions

List sessions:

sessions -l

Interact with session:

sessions -i <id>

---

## Lessons Learned

- Understanding exploits improves defense  
- Many attacks rely on misconfigurations  
- Detection visibility is key  
- Lab testing builds defensive insight
