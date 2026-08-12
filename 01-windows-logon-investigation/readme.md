# Windows Logon Activity Investigation

A controlled host-based log analysis investigation of Windows authentication activity using Security Event IDs 4624 and 4625.

## Objective

This investigation analyzes successful and failed Windows logon events to understand how authentication activity is recorded and how an analyst can use these events to identify and correlate suspicious access attempts.

## Environment

- Windows 10 Virtual Machine
- VMware Workstation
- Windows Event Viewer
- Windows Security Log
- Event ID 4624 — Successful Logon
- Event ID 4625 — Failed Logon

## Methodology

The investigation was performed in an isolated lab environment using controlled logon attempts. The resulting Security events were filtered, examined field-by-field, correlated by account and timestamp, and used to construct an authentication timeline.

## Key Areas Investigated

- Event ID 4625 — Failed Logon
- Event ID 4624 — Successful Logon
- Logon Type
- Status and Sub Status codes
- Account information
- Source and workstation information
- Authentication details
- Evidence correlation
- Authentication timeline
- MITRE ATT&CK relevance

## Findings

The investigation demonstrated how repeated failed logons followed by a successful logon can provide a behavioral indicator of a possible password-guessing scenario. It also demonstrated the importance of fields such as Logon Type, Sub Status, and Logon ID during authentication investigations.

## Full Investigation

**[Read the Full Investigation (PDF)](./Windows%20Logon%20Activity%20Investigation.pdf)**

## Investigation Status

**Completed**

## References

- Microsoft Learn — Event ID 4624
- Microsoft Learn — Event ID 4625
- Microsoft Learn — Audit Logon Events
- MITRE ATT&CK — T1110: Brute Force
- MITRE ATT&CK — T1078: Valid Accounts
