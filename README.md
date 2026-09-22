# Windows Event Log Investigations

This repository contains practical investigations of Windows Event Logs focused on authentication activity, process creation, event analysis, timeline reconstruction, event correlation, and forensic documentation.

The investigations are performed in controlled laboratory environments and follow a host-based log analysis approach relevant to Security Operations (SOC) and Digital Forensics and Incident Response (DFIR).

## Investigations

### 01. Windows Logon Activity Investigation

**Focus:** Event ID 4624 and Event ID 4625

This investigation examines successful and failed Windows logon activity using Windows Event Viewer. It analyzes authentication-related fields, including Logon Type, Status/Sub Status, account information, source information, and Logon ID.

The investigation also demonstrates how failed and successful authentication events can be correlated by account and timestamp to construct an authentication timeline.

**Environment:**

- Windows 10 Virtual Machine
- VMware Workstation
- Windows Event Viewer
- Windows Security Log

**Investigation areas:**

- Event ID 4624 — Successful Logon
- Event ID 4625 — Failed Logon
- Logon Type analysis
- Status and Sub Status analysis
- Authentication event correlation
- Evidence table
- Authentication timeline
- Findings and limitations
- MITRE ATT&CK relevance

[**View the full investigation →**](https://github.com/Mishdfir/windows-event-investigation/blob/main/Windows%20Logon%20Activity%20Investigation.pdf)

---

### 02. Windows Process Creation Investigation

**Focus:** Event ID 4688

This investigation examines Windows Security Event ID 4688, **"A new process has been created,"** to understand how process creation activity is logged and how it can be used to reconstruct user and system behavior on a Windows endpoint.

The investigation analyzes process, user, and session-level information and examines the relationship between a creator/parent process and the newly created child process.

It also examines command-line information where process creation auditing permits and investigates the relationship between Event ID 4688 process creation events and Event ID 4624 logon events.

**Environment:**

- Windows 10 Virtual Machine
- VMware Workstation
- Windows Event Viewer
- Windows Security Log
- Process Creation Auditing

**Investigation areas:**

- Event ID 4688 — Process Creation
- Process name and Process ID analysis
- Creator/parent process analysis
- Parent-child process relationships
- Command-line analysis
- Process tree reconstruction
- Event ID 4624 correlation
- Process activity timeline
- Evidence analysis
- Findings and limitations
- MITRE ATT&CK relevance

**Observed process relationship:**

```text
svchost.exe (PID 0x394)
├── TaskHost.exe (PID 0x1D24)
└── UserOOBEBroker.exe (PID 0x1FB0)

* Microsoft Learn — Windows Security Event ID 4624
* Microsoft Learn — Windows Security Event ID 4625
* Microsoft Learn — Audit Logon Events
* MITRE ATT&CK
