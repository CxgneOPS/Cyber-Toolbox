# Investigation Methodology

This page documents how I approach alerts, investigations, and suspicious activity in my home SOC lab.

My focus is not just using tools, but developing a repeatable and logical investigation process.

---

## Mindset

- Assume nothing at first  
- Validate before escalating  
- Focus on evidence, not assumptions  
- Look for patterns, not single events  
- Stay calm and methodical  

The goal is to understand what happened, not to jump to conclusions.

---

## Alert Triage Process

1. Review alert details  
   - Rule triggered  
   - Severity level  
   - Source host  

2. Validate the alert  
   - Check related logs  
   - Confirm activity actually occurred  
   - Rule out obvious false positives  

3. Gather context  
   - What user was involved?  
   - What process executed?  
   - What system was affected?  

4. Determine intent  
   - Normal behavior?  
   - Misconfiguration?  
   - Suspicious activity?  

5. Document findings  

---

## Investigation Workflow

### Step 1 — Identify the Indicator
Start with the alert, hash, IP, or behavior that triggered concern.

---

### Step 2 — Collect Logs
Review:
- Endpoint logs  
- Network traffic  
- SIEM alerts  
- System events  

---

### Step 3 — Correlate Events
Look for:
- Timeline patterns  
- Repeated behavior  
- Related activity across systems  

---

### Step 4 — Validate Suspicion
Ask:
- Is this normal in this environment?  
- Has it happened before?  
- Does it match known attack patterns?  

---

### Step 5 — Document Results
Record:
- What was observed  
- What was verified  
- Final conclusion  

---

## What I Look For

- Unusual parent/child processes  
- Unexpected outbound connections  
- Privilege escalation attempts  
- Persistence behavior  
- Abnormal login patterns  

---

## Continuous Improvement

After each investigation I ask:

- What did I miss?  
- What could I detect earlier?  
- How can rules be tuned?  
- What did I learn?  

---

## Philosophy

Tools support investigations — they don’t replace thinking.

A good analyst:
- Stays curious  
- Verifies evidence  
- Documents clearly  
- Keeps improving  

Consistency beats complexity.
