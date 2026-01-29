# auditd

## What It Is

auditd (Linux Audit Daemon) is a Linux system service that logs detailed system activity for monitoring and investigations.

It provides visibility into command execution, file access, user activity, and system changes.

---

## What I Use It For

- Monitoring command execution  
- Tracking file access and modifications  
- Detecting privilege escalation or persistence  
- Feeding Linux telemetry into my SIEM (Wazuh)

auditd is one of the most valuable tools for Linux endpoint visibility in a SOC environment.

---

## Basic Setup

1. Install auditd  
2. Start and enable the service  
3. Add basic monitoring rules  
4. Confirm logs appear in: /var/log/audit/audit.log

---

## Core Concepts

auditd works based on **rules** instead of event IDs.

Rules tell auditd what activity to log.

Some key rule types:

- File watch rules  
- Syscall monitoring  
- User activity tracking  
- Command execution logging

Understanding rules is critical for detection work.

---

## Common Workflow

### Basic Investigation Flow

1. Identify suspicious behavior or alert  
2. Search logs using ausearch  
3. Review command or file activity  
4. Check user account involved  
5. Look for unusual behavior patterns

---

## Troubleshooting

No logs appearing:
- Ensure auditd service is running  
- Verify rules are loaded  
- Check audit.log path

Too many logs:
- Tune rules to reduce noise  
- Remove unnecessary file watches

---

# Commands

---

## Config Management

View active rules:

auditctl -l

Clear all rules:

auditctl -D

Add file watch:

auditctl -w /etc/passwd -p wa -k passwd_changes

---

## Service Control

Start auditd:

systemctl start auditd

Enable at boot:

systemctl enable auditd

Restart auditd:

systemctl restart auditd

---

## Status Checks

Check auditd status:

systemctl status auditd

Confirm audit logs exist:

ls /var/log/audit/

---

## Log Hunting

Search by key:

ausearch -k passwd_changes

Search by user:

ausearch -ua 1000

Search recent activity:

ausearch -ts recent

Summary report:

aureport

---

## Lessons Learned

- Default rules are minimal — tuning matters  
- File monitoring is extremely valuable  
- Command execution logs reveal a lot about behavior  
- auditd + SIEM integration is where the real power is
