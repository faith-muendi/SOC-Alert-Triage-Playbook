# SOC Alert Escalation Criteria

## Purpose
This document defines **when and how alerts are escalated** from Level 1 (Tier 1) SOC analysts to Level 2 (Tier 2) or Incident Response teams.

Clear escalation criteria ensure:
- Faster response to real threats
- Reduced analyst confusion
- Consistent decision-making across shifts

---

## General Escalation Triggers

An alert **must be escalated** if any of the following conditions are met:

- Evidence of confirmed malicious activity
- Successful authentication following failed attempts
- Malware execution or persistence observed
- Lateral movement indicators detected
- Data exfiltration suspected
- Multiple systems or users affected

---

## Alert Severity-Based Escalation

### Low Severity
- Likely false positives
- No malicious indicators
- Document findings and close

### Medium Severity
- Suspicious activity requiring correlation
- Escalate if activity persists or escalates
- Monitor closely if isolated

### High Severity
- Confirmed malicious behavior
- Immediate escalation required
- Notify SOC Lead or Incident Response

---

## Brute Force Alert Escalation Example

Escalate a brute force alert if:
- Event ID 4624 (successful login) follows multiple 4625 failures
- Same source IP targets multiple accounts
- Attempts originate from suspicious geolocation
- Account is privileged or high-value

---

## Required Information for Escalation

When escalating, include:
- Alert summary
- Timeline of events
- Affected assets
- Source IPs and user accounts
- Logs and evidence reviewed
- Analyst assessment and recommendation

---

## Communication Channels
- SOC ticketing system
- Secure messaging platform
- Incident response hotline (if applicable)

---

## Key Principle
Escalation is **not failure**.  
It is a **controlled handoff to deeper expertise**.
