# Authentication Log Analysis

## Objective
Identify suspicious authentication behavior and differentiate between attacks and normal user activity.

## Method
- Searched for failed SSH login attempts
- Identified frequency, source IPs, and usernames
- Analyzed timing patterns

## Commands Used
grep "Failed password" auth.log  
grep "Failed password" auth.log | awk '{print $(NF-3)}' | sort | uniq -c | sort -nr

## Findings
- IP 203.0.113.45 attempted multiple logins in a short time
- Targeted several invalid usernames
- Pattern indicates automated brute-force attempt
