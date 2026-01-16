# Web Server Log Analysis

## Objective
Detect reconnaissance and scanning activity in web access logs.

## Method
- Searched for common admin and configuration paths
- Analyzed HTTP status codes
- Reviewed request frequency per IP

## Commands Used
grep -E "wp-admin|phpmyadmin|\.env|/admin" access.log  
awk '{print $1}' access.log | sort | uniq -c | sort -nr

## Findings
- IP 198.51.100.23 requested multiple sensitive paths
- Requests resulted in 404 responses
- Behavior consistent with automated web scanning
