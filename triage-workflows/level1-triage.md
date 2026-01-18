# Level 1 SOC Alert Triage Workflow

## Purpose
This document defines the **standard Level 1 (Tier 1) SOC triage process** used to analyze incoming security alerts.

The goal of Level 1 triage is to **quickly validate alerts**, identify false positives, and escalate confirmed threats for deeper investigation.

---

## Step 1: Alert Validation
- Confirm alert source (SIEM, EDR, IDS, email gateway)
- Verify alert type and severity
- Ensure alert data is complete and readable

Questions to ask:
- Is this a trusted detection source?
- Has this alert fired correctly?

---

## Step 2: Identify Affected Assets
- Identify affected user(s)
- Identify affected host(s)
- Identify source IP addresses
- Determine business criticality of the asset

---

## Step 3: Initial Log Review
- Review event logs related to the alert
- Validate timestamps
- Check for repeated activity
- Look for known indicators of compromise (IOCs)

---

## Step 4: Contextual Analysis
- Is the activity normal for this user?
- Does it occur during business hours?
- Has this alert occurred before?
- Is there a change from baseline behavior?

---

## Step 5: False Positive Assessment
Common false positives include:
- User error
- Misconfigured services
- Legitimate administrative activity
- Security tools generating noise

Decision:
- **False Positive** → Document and close
- **True Positive** → Escalate

---

## Step 6: Escalation Criteria
Escalate the alert if:
- Malicious intent is suspected
- Activity persists or escalates
- Successful compromise indicators exist
- Multiple systems are affected

---

## Documentation Requirements
Every alert must include:
- Summary of findings
- Evidence reviewed
- Decision taken
- Time spent
- Next steps

---

## Key Principle
Level 1 SOC analysts **do not fix incidents**.  
They **validate, document, and escalate**.
