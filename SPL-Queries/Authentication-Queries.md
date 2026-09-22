# Authentication Detection Queries

## 1. Failed Login Detection

### Objective
Detect failed login attempts in Windows environment.

### Windows Event ID
4625 - Failed Logon

### Splunk Query

```spl
index=windows EventCode=4625
| table _time Account_Name Source_Network_Address
