# Brute Force Attack Investigation Report

## Alert Name

Multiple Failed Login Attempts Detected


## Severity

Medium


## Detection Tool

Splunk SIEM


## Log Source

Windows Security Event Log


## Detection Event

Event ID: 4625

Failed Logon


## Detection Query

```spl
index=windows EventCode=4625
| stats count by Account_Name, Source_Network_Address
| where count > 10
