# Investigation Summary

This project simulates Tier-1 SOC log triage by analyzing Linux authentication and web server logs to identify malicious activity and benign events. The investigation focused on distinguishing true security threats from false positives using raw log data and analytical reasoning.

The analysis identified two primary security concerns: repeated SSH authentication failures consistent with brute-force attempts, and web server requests targeting common administrative and configuration paths indicative of automated reconnaissance. These events were assessed based on frequency, timing, source IP behavior, and targeted resources.

In parallel, the project documented false positives such as isolated failed logins followed by successful authentication from internal IP addresses, which were correctly classified as normal user behavior requiring no escalation.

Overall, this project demonstrates foundational SOC analyst skills including event triage, noise reduction, evidence-based decision making, and clear security documentation without reliance on SIEM tools.
