# Sysmon Threat Detection Notes

## About Sysmon

Sysmon (System Monitor) is a Windows tool that provides detailed information about system activity and helps SOC analysts detect suspicious behavior.


## Important Sysmon Event IDs


## Event ID 1 - Process Creation

Purpose:
Monitor newly created processes.

Used for detecting:
- Suspicious executables
- Command execution
- Malware activity


Example Investigation:

Check:
- Process name
- Command line
- User account
- Parent process


---

## Event ID 3 - Network Connection

Purpose:
Monitor network connections created by processes.

Used for detecting:
- Suspicious outbound connections
- Malware communication


---

## Event ID 7 - Image Loaded

Purpose:
Monitor DLL loading activity.

Used for detecting:
- Suspicious DLL injection


---

## Event ID 10 - Process Access

Purpose:
Monitor process-to-process access.

Used for detecting:
- Credential dumping attempts


---

## SOC Investigation Workflow

1. Identify suspicious event
2. Check process details
3. Review user activity
4. Analyze network connection
5. Determine if escalation is required
