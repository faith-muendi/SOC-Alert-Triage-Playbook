## How This Alert Is Generated

This alert is generated using a **Sigma detection rule** that monitors Windows Security logs for repeated failed authentication attempts.

### Detection Logic Summary
- Log Source: Windows Security Event Logs
- Event ID: 4625 (Failed Logon)
- Threshold: 5 or more failed attempts
- Time Window: 5 minutes

### Detection File


## Common Causes
- User entering incorrect password multiple times
- Forgotten password
- Service account misconfiguration
- Automated attack attempting password guessing

---

## Severity
**Medium**  
May escalate to **High** if successful authentication is observed.

---

## Level 1 Triage (Initial Analysis)

### 1. Validate the Alert
- Confirm log source is legitimate (Windows Security logs)
- Verify Event ID 4625
- Identify:
  - Target username
  - Source IP address
  - Target host

### 2. Check Frequency
- How many failed attempts?
- Over what time period?
- Single user or multiple users?

### 3. Look for Patterns
- Same IP attempting multiple logins
- Same account targeted repeatedly
- Attempts outside normal working hours

---

## Level 2 Investigation (If Escalated)

- Check for **successful login events (Event ID 4624)** following failures
- Review historical login behavior for the account
- Correlate with:
  - VPN logs
  - Firewall logs
  - EDR telemetry
- Determine if lateral movement occurred

---

## Indicators of Compromise (IOCs)
- Repeated failed logins from unknown IPs
- Login attempts from unusual geolocations
- Multiple accounts targeted from same source

---

## Recommended Response Actions
- Temporarily lock affected account (if required)
- Block malicious IP address
- Reset compromised credentials
- Notify affected user
- Escalate to Incident Response if compromise confirmed

---

## MITRE ATT&CK Mapping
- **Tactic:** Credential Access
- **Technique:** Brute Force (T1110)

---

## Notes
False positives are common.  
Always validate context before escalating.
