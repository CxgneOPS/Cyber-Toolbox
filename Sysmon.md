# Sysmon

## What It Is

Sysmon (System Monitor) is a Windows system service from Microsoft that logs detailed system activity to the Windows Event Log.

It provides visibility into process creation, network connections, file changes, and more.

---

## What I Use It For

- Monitoring process creation and parent/child relationships  
- Tracking network connections from endpoints  
- Detecting suspicious behavior and persistence methods  
- Feeding high-quality telemetry into my SIEM (Wazuh)  

Sysmon is one of the most valuable tools for endpoint visibility in a SOC environment.

---

## Basic Setup

1. Download Sysmon from Microsoft Sysinternals  
2. Install with a configuration file: sysmon -i config.xml
3. Verify its running
4. Confirm logs apear in : Event Viewer → Applications and Services Logs → Microsoft → Windows → Sysmon
---

## Core Concepts

Sysmon works based on **Event IDs**.

Some key ones:

- Event ID 1 — Process creation  
- Event ID 3 — Network connections  
- Event ID 7 — Image loads (DLLs)  
- Event ID 11 — File creation  
- Event ID 13 — Registry changes  

Understanding these is critical for detection work.

---

## Common Workflow

### Basic Investigation Flow

1. Identify a suspicious alert in SIEM  
2. Check Sysmon Event ID 1 for process details  
3. Review parent/child processes  
4. Check Event ID 3 for network activity  
5. Look for unusual behavior patterns

## Troubleshooting
No logs appearing:
- Ensure Sysmon service is running  
- Verify config file loaded correctly  
- Check Event Viewer path  

Too many logs:
- Tune config to reduce noise  
- Exclude known safe processes  

---

# Commands

---

## Config Management

Update config:
sysmon -c config.xml

Show current config: 
sysmon -c

Reset to Defult config:
sysmon -c --

---

## Service Control:

Uninstall Sysmon:

sysmon -u

Force Uninstall:

sysmon -u force

---

## Status Checks:

Show sysmon schema:

sysmon -s

Check if sysmon service is running:

sc query sysmon

---

## Log Hunting (Power Shell)

View Recent sysmon events:

Get-WinEvent -LogName "Microsoft-Windows-Sysmon/Operational" -MaxEvents 20

Process Creation:

Get-WinEvent -FilterHashtable @{LogName="Microsoft-Windows-Sysmon/Operational"; ID=1}

Network Connections:

Get-WinEvent -FilterHashtable @{LogName="Microsoft-Windows-Sysmon/Operational"; ID=3}

Searcg by Process Name

Get-WinEvent -LogName "Microsoft-Windows-Sysmon/Operational" | Where-Object {$_.Message -like "*powershell.exe*"}

---

## Lessons Learned

- Default configs are noisy — tuning matters  
- Parent/child process analysis is extremely valuable  
- Network telemetry reveals a lot about behavior  
- Sysmon + SIEM integration is where the real power is

---
