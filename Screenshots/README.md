# Screenshots

This folder contains screenshots from my SOC lab investigations using Splunk.

## Splunk Evidence

### 1. Failed Login Detection

Query:
```spl
index=windows EventCode=4625
| table _time Account_Name Source_Network_Address Failure_Reason
