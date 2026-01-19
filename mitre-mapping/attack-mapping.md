# MITRE ATT&CK Mapping – SOC Alert Triage Playbook

## Purpose
This document maps common SOC alerts and detection rules in this repository to the **MITRE ATT&CK framework**.

MITRE ATT&CK helps analysts:
- Understand attacker intent
- Classify adversary behavior
- Improve detection and response consistency

---

## Brute Force Login Attempts

### Alert Type
Brute Force Authentication Attempts

### Related Detection
- Sigma Rule: Windows Brute Force Logon Attempt
- Log Source: Windows Security Logs
- Event ID: 4625

### MITRE ATT&CK Mapping
- **Tactic:** Credential Access
- **Technique:** Brute Force (T1110)

### Analyst Context
Attackers may attempt to guess passwords to gain unauthorized access.  
If successful authentication follows repeated failures, this may indicate account compromise.

---

## How Analysts Use This Mapping

SOC analysts use MITRE mappings to:
- Understand the attacker’s goal
- Identify potential next steps in the attack chain
- Prioritize alerts based on threat context
- Communicate findings using a common language

---

## Notes
MITRE mappings may evolve as detection logic improves or new threat intelligence is incorporated.
