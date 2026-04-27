# Suspicious PowerShell Persistence Investigation – SOC Tier 1 Simulation

## 📄 Executive Summary

Suspicious PowerShell activity was identified on a Windows endpoint during routine alert monitoring. Investigation revealed an encoded PowerShell command launching from a user context and creating a scheduled task designed to execute at logon. The behavior was consistent with persistence techniques commonly used by attackers. The activity was classified as a true positive security incident, and containment actions were recommended.

## 🚨 Alert Trigger

A security alert was generated after PowerShell executed with encoded command-line arguments on a Windows workstation. Additional telemetry indicated a newly created scheduled task.

## 🔍 Investigation Steps

1. Reviewed endpoint telemetry for PowerShell process execution details.
2. Identified use of encoded command-line arguments commonly associated with obfuscation.
3. Checked parent-child process relationships to determine how PowerShell was launched.
4. Reviewed Windows Task Scheduler activity for newly created scheduled tasks.
5. Examined task name, trigger conditions, and execution path.
6. Assessed whether the activity aligned with legitimate administrative behavior or persistence tactics.

## 📊 Findings

* PowerShell executed using encoded command parameters.
* Process launched from a standard user context rather than an approved admin workflow.
* A new scheduled task was created to run at user logon.
* Task executed a script from a suspicious user-accessible directory.
* No approved maintenance activity was associated with the event.

## 🧠 Analysis

Encoded PowerShell commands are frequently used to conceal malicious intent and evade simple detection methods. The creation of a scheduled task configured to run at logon strongly suggests an attempt to establish persistence on the endpoint. Because the activity did not align with normal administrative operations, it was assessed as malicious or unauthorized behavior requiring immediate response.

## 🎯 Conclusion

The activity was determined to be a true positive suspicious persistence event involving PowerShell abuse. The combination of obfuscation techniques and scheduled task creation indicated a likely attempt to maintain unauthorized access.

## 🛡️ Mitigation & Recommendations

* Isolate the affected endpoint for further review.
* Disable and remove the unauthorized scheduled task.
* Collect the referenced script or payload for malware analysis.
* Reset credentials associated with the impacted user account.
* Review additional endpoints for similar PowerShell and task creation activity.
* Strengthen monitoring rules for encoded PowerShell execution.
