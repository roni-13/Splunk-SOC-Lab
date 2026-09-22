# Authentication Monitoring Dashboard

## Purpose

This dashboard monitors authentication activities in Windows environment using Splunk.

## Data Source

Windows Security Event Logs


## Dashboard Panels

### 1. Successful Login Monitoring

Event ID:
4624

Purpose:
Track successful user authentication.


### 2. Failed Login Monitoring

Event ID:
4625

Purpose:
Identify failed authentication attempts.


### 3. Top Users with Failed Login Attempts

Query:

```spl
index=windows EventCode=4625
| stats count by Account_Name
| sort -count
