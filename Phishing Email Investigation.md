# Phishing Email Investigation – SOC Tier 1 Simulation

## 📄 Executive Summary

A suspicious email claiming to require urgent account verification was reported for investigation. Analysis of the sender details, email content, embedded links, and header information revealed multiple phishing indicators including spoofed branding, urgency tactics, and a suspicious destination URL. The message was classified as a phishing attempt, and containment actions were recommended.

## 🚨 Alert Trigger

A user reported receiving an unexpected email requesting immediate password verification to avoid account suspension. The message appeared to impersonate a legitimate company and included a clickable link.

## 🔍 Investigation Steps

1. Reviewed sender email address and display name for impersonation indicators.
2. Examined subject line and message body for urgency, threats, or social engineering tactics.
3. Hovered over embedded links to inspect destination URLs.
4. Reviewed email headers for sender path, reply-to discrepancies, and originating domains.
5. Checked domains and URLs for suspicious naming patterns.
6. Assessed whether the message aligned with known phishing behaviors.

## 📊 Findings

* Sender display name mimicked a legitimate company, but the actual email domain was unrelated.
* Email used urgent language requesting immediate action.
* Embedded link redirected to a suspicious non-corporate domain.
* Grammar and formatting inconsistencies were present.
* Header review indicated sender information inconsistent with legitimate business email practices.

## 🧠 Analysis

The combination of spoofed branding, urgency-based messaging, suspicious link destinations, and inconsistent sender information strongly indicates a phishing attempt. The objective was likely credential theft through a fake login page or malware delivery through user interaction.

## 🎯 Conclusion

The email was determined to be a true positive phishing attempt. No user interaction was confirmed at the time of review. Immediate blocking and user awareness actions were recommended.

## 🛡️ Mitigation & Recommendations

* Block sender domain and associated URLs in email security tools.
* Warn impacted users and advise deletion of the message.
* Reset credentials immediately if any user clicked the link.
* Enable MFA for affected accounts.
* Continue monitoring for similar phishing campaigns.
* Provide phishing awareness reminders to users.

