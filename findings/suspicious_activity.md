# Suspicious Activity Findings

## SSH Brute-Force Attempt
- Source IP: 203.0.113.45
- Evidence:
  - Multiple failed login attempts
  - Multiple invalid usernames
  - High frequency in short time window
- Assessment: Likely brute-force attack
- Recommended Action:
  - Block IP
  - Enable fail2ban
  - Enforce key-based SSH authentication

## Web Reconnaissance
- Source IP: 198.51.100.23
- Evidence:
  - Requests to /wp-admin, /.env, /phpmyadmin
  - Known scanning paths
- Assessment: Automated reconnaissance
- Recommended Action:
  - Monitor for escalation
  - Apply rate limiting
