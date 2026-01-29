# Wazuh

## What It Is

Wazuh is an open-source SIEM and XDR platform used for threat detection, integrity monitoring, vulnerability detection, and log analysis.

It collects and analyzes logs from endpoints, servers, and network devices.

---

## What I Use It For

- Centralized log collection  
- Alert triage and investigations  
- File Integrity Monitoring (FIM)  
- Monitoring endpoint activity  
- Learning real SOC workflows  

Wazuh is the backbone of my home SOC lab.

---

## Basic Setup

1. Install Wazuh server or all-in-one stack  
2. Deploy agent to endpoint  
3. Register agent with manager  
4. Confirm agent appears in dashboard

---

## Core Concepts

Wazuh works based on:

- Agents (endpoints sending logs)  
- Rules (detect suspicious activity)  
- Decoders (parse logs into readable data)  
- Alerts (triggered detections)

Understanding rules and alerts is critical for detection work.

---

## Common Workflow

### Basic Investigation Flow

1. Identify alert in Wazuh dashboard  
2. Review alert rule and severity  
3. Check source agent  
4. Analyze related logs  
5. Determine if activity is normal or suspicious

---

## Troubleshooting

Agent not connecting:
- Verify agent is running  
- Check manager IP in agent config  
- Confirm firewall is not blocking port 1514

No alerts appearing:
- Verify logs are being collected  
- Check rules are enabled  
- Confirm agent is active

---

# Commands

---

## Agent Management

List agents:

/var/ossec/bin/agent_control -l

Check agent status:

/var/ossec/bin/agent_control -i <agent_id>

Restart agent:

systemctl restart wazuh-agent

---

## Manager Control

Restart Wazuh manager:

systemctl restart wazuh-manager

Check manager status:

systemctl status wazuh-manager

---

## Log Locations

Manager logs:

/var/ossec/logs/ossec.log

Alerts log:

/var/ossec/logs/alerts/alerts.json

---

## Rules & Config

Main config file:

/var/ossec/etc/ossec.conf

Rules directory:

/var/ossec/ruleset/rules/

Restart after config changes:

systemctl restart wazuh-manager

---

## Lessons Learned

- Alert tuning is critical to reduce noise  
- FIM is great for detecting changes  
- Agent health monitoring matters  
- Wazuh + endpoint telemetry provides strong visibility
