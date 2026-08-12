# Windows Event Log Investigations

This repository contains practical investigations of Windows Event Logs focused on authentication activity, event analysis, timeline reconstruction, correlation, and forensic documentation.

The investigations are performed in controlled laboratory environments and follow a host-based log analysis approach relevant to Security Operations (SOC) and Digital Forensics and Incident Response (DFIR).

## Investigations

### 01. Windows Logon Activity Investigation

**Focus:** Event ID 4624 and Event ID 4625

This investigation examines successful and failed Windows logon activity using Windows Event Viewer. It analyzes authentication-related fields, including Logon Type, Status/Sub Status, account information, source information, and Logon ID.

The investigation also demonstrates how failed and successful authentication events can be correlated by account and timestamp to construct an authentication timeline.

**Environment:**

* Windows 10 Virtual Machine
* VMware Workstation
* Windows Event Viewer
* Windows Security Log

**Investigation areas:**

* Event ID 4624 — Successful Logon
* Event ID 4625 — Failed Logon
* Logon Type analysis
* Status and Sub Status analysis
* Authentication event correlation
* Evidence table
* Authentication timeline
* Findings and limitations
* MITRE ATT&CK relevance

**[View the full investigation →](./Windows%20Logon%20Activity%20Investigation.pdf)**

## Future Investigations

Additional Windows Event Log investigations will be added as the practical investigation work progresses, including event correlation and analysis of other security-relevant Windows events.

## Scope

This repository focuses on practical Windows Event Log analysis and documentation. All activities are conducted in controlled laboratory environments for learning, research, and defensive security analysis.

## References

* Microsoft Learn — Windows Security Event ID 4624
* Microsoft Learn — Windows Security Event ID 4625
* Microsoft Learn — Audit Logon Events
* MITRE ATT&CK
