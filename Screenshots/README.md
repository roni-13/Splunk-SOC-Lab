# Screenshots

This folder contains screenshots from my SOC lab investigations using Splunk.

## Splunk Evidence

### 1. Failed Login Detection

Query:
```spl
index=windows EventCode=4625
| table _time Account_Name Source_Network_Address Failure_Reason


### 1. Top Failed Login Users

Query:

index=windows EventCode=4625
| stats count by Account_Name
| sort -count

3. Sysmon Process Creation Monitoring

Query:

index=sysmon EventCode=1
| table _time Image CommandLine User
