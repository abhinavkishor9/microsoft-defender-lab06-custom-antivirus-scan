# Troubleshooting Notes

## Issue 1

### Problem

Custom Scan option not available.

### Cause

Microsoft Defender disabled by another antivirus solution.

### Resolution

Remove third-party antivirus or re-enable Microsoft Defender.

---

## Issue 2

### Problem

Operational logs are empty.

### Cause

Windows Defender Operational logging disabled.

### Resolution

Enable:

Applications and Services Logs

→ Microsoft

→ Windows

→ Windows Defender

→ Operational

---

## Issue 3

### Problem

Event ID 1001 not generated.

### Cause

Scan did not finish or was cancelled.

### Resolution

Allow the scan to complete before reviewing Event Viewer.

---

## Issue 4

### Problem

Unable to select folder for Custom Scan.

### Cause

Folder permissions or incorrect path.

### Resolution

Select an accessible local directory.

---

## Issue 5

### Problem

Scan reports "Last Scan Not Available."

### Cause

No successful scan completed previously.

### Resolution

Run a Quick Scan or Custom Scan again.

---

## Issue 6

### Problem

Defender service not running.

### Resolution

Verify:

```

WinDefend

```

using:

```

Get-Service WinDefend

```

or

```

sc query WinDefend

```

---

## Lessons Learned

- Event ID 1001 confirms scan completion.
- Custom scans provide targeted endpoint validation.
- Defender Operational logs are valuable forensic artifacts.
- Successful scans should always be correlated with Windows Security status.
- Manual scans help validate endpoint protection during investigations.
