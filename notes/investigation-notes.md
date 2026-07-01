# Investigation Notes

## Incident Summary

A manual Microsoft Defender Custom Scan was executed against a selected directory to validate endpoint protection functionality and review Defender logging.

---

## Investigation Details

### Scan Type

Custom Scan

---

### Target

SOC-Lab folder

---

### Log Source

Microsoft-Windows-Windows Defender/Operational

---

### Event Reviewed

Event ID 1001

---

## Event Details

Scan Type:
Antimalware

Scan Parameters:
Custom Scan

Scan Status:
Completed Successfully

Threats Detected:
None

User:
SYSTEM

---

## Timeline

| Time | Activity |
|------|----------|
|06:40|Created test files|
|06:43|Started Custom Scan|
|06:43|Scan completed|
|06:43|Event ID 1001 generated|
|06:48|Reviewed Operational logs|

---

## Findings

- Defender successfully completed the scan.
- Event ID 1001 confirms successful completion.
- No malware was detected.
- No remediation actions were required.
- Endpoint protection operated as expected.

---

## Indicators of Compromise (IoCs)

None observed.

---

## Impact Assessment

No malicious activity identified.

Endpoint remained healthy.

---

## Analyst Conclusion

The Defender Custom Scan completed successfully without detecting malicious files.

Operational logs accurately recorded the scan lifecycle, demonstrating Defender's logging capabilities and providing valuable forensic evidence for SOC investigations.
