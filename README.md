# microsoft-defender-lab06-custom-antivirus-scan
## Overview

This lab demonstrates how Microsoft Defender performs a Custom Antivirus Scan against a selected directory and how scan activity is logged inside Windows Event Viewer.

The objective is to understand:

- Running a Custom Scan
- Monitoring Windows Defender activity
- Reviewing Operational logs
- Investigating Event ID 1001
- Documenting scan results from a SOC analyst perspective

---

## Lab Objectives

- Perform a Microsoft Defender Custom Scan
- Scan a specific folder
- Observe scan completion
- Investigate Defender Operational Logs
- Analyze Event ID 1001
- Document investigation findings

---

## Lab Environment

| Component | Value |
|-----------|-------|
| Operating System | Windows 10 x64 |
| Security Solution | Microsoft Defender Antivirus |
| Log Source | Windows Defender Operational |
| Event Viewer | Windows Logs |
| VM Platform | VMware Workstation |

---

## Scenario

A SOC analyst receives confirmation that a user manually initiated an antivirus scan on a suspicious directory.

The analyst must verify:

- Was the scan completed?
- What scan type was used?
- Was malware detected?
- Were any errors reported?
- What evidence exists in Defender logs?

---

## Steps Performed

1. Created a test folder containing multiple text files.
2. Opened Windows Security.
3. Selected **Virus & Threat Protection**.
4. Opened **Scan Options**.
5. Selected **Custom Scan**.
6. Chose the test folder.
7. Waited for scan completion.
8. Opened Event Viewer.
9. Navigated to:

```

Applications and Services Logs
→ Microsoft
→ Windows
→ Windows Defender
→ Operational

```

10. Reviewed Event ID 1001.
11. Documented investigation findings.

---

## Key Event

| Event ID | Description |
|----------|-------------|
|1001|Microsoft Defender Antivirus scan completed|

---

## Investigation Summary

The antivirus scan completed successfully.

Microsoft Defender generated Event ID 1001 indicating:

- Scan Type: Antivirus
- Scan Parameters: Custom Scan
- Scan completed successfully
- No malware detected
- No remediation required

The event confirms Defender successfully scanned the selected directory.

---

## Skills Practiced

- Microsoft Defender
- Windows Security
- Event Viewer
- Windows Defender Operational Logs
- Event ID Investigation
- SOC Documentation
- Endpoint Security Monitoring

---

## MITRE ATT&CK Mapping

| Technique | Description |
|-----------|-------------|
|T1083|File and Directory Discovery|
|T1518|Software Discovery|

*(Defensive validation activity rather than attacker behavior.)*

---

## Learning Outcomes

After completing this lab, you can:

- Perform Microsoft Defender custom scans
- Verify scan completion
- Investigate Defender Operational logs
- Analyze Event ID 1001
- Document endpoint scan activity like a SOC analyst

---
