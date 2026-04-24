# SOC Analyst Portfolio – Matthew Anton

This repository contains hands-on cybersecurity projects demonstrating skills in SIEM monitoring, incident response, and log analysis.

---

# 🛡️ Incident Report #1 – Suspicious Login Attempt

## Alert Summary

* Alert Name: Suspicious Login Activity
* Source: SIEM (Splunk)
* Severity: Medium
* Date: [Insert Date]

## Initial Findings

* Multiple failed login attempts detected from IP: 192.168.1.100
* Target account: admin
* Activity occurred within a short timeframe

## Investigation Steps

* Reviewed authentication logs in SIEM
* Correlated login attempts across timestamps
* Identified pattern consistent with brute force attack
* Checked IP reputation using OSINT tools

## Indicators of Compromise (IOCs)

* Suspicious IP: 192.168.1.100
* Repeated failed logins
* Abnormal login behavior

## Analysis

The activity indicates a likely brute-force attack attempting unauthorized access. No successful login observed.

## Action Taken

* Recommended account lockout policy
* Suggested blocking IP at firewall
* Escalated for further monitoring

## Tools Used

* Splunk
* OSINT tools

## MITRE ATT&CK Mapping

* T1110 – Brute Force

## Conclusion

No confirmed breach, but attack behavior detected. Continued monitoring recommended.
