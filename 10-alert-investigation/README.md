# LetsDefend 10-Alert Investigation Project

## Overview

This project documents 10 security alerts investigated as part of hands-on SOC Analyst practice on LetsDefend.

The investigations cover endpoint compromise, phishing, malware execution, brute-force activity, SQL injection, command injection, remote code execution, authentication bypass and unauthorized VPN access.

## Investigation Method

For each alert, I followed a practical SOC workflow:

1. Review the alert and understand why it triggered.
2. Identify the affected host, account, source and destination.
3. Collect supporting evidence from available security tools.
4. Correlate timestamps, processes, network connections and indicators.
5. Reconstruct the likely attack sequence.
6. Determine whether the activity was attempted, blocked or successful.
7. Decide on containment, escalation and remediation actions.
8. Map relevant activity to MITRE ATT&CK.
9. Document the investigation and final verdict.

## Investigations

| Alert | Investigation |
|---|---|
| SOC335 | [CVE-2024-49138 Exploitation](./SOC335-CVE-2024-49138/) |
| SOC336 | [Windows OLE Zero-Click RCE](./SOC336-CVE-2025-21298/) |
| SOC342 | [SharePoint ToolShell Auth Bypass and RCE](./SOC342-CVE-2025-53770/) |
| SOC274 | [PAN-OS Command Injection](./SOC274-CVE-2024-3400/) |
| SOC127 | [SQL Injection](./SOC127-SQL-Injection/) |
| SOC338 | [Lumma Stealer / ClickFix Phishing](./SOC338-Lumma-Stealer/) |
| SOC153 | [Suspicious PowerShell](./SOC153-Suspicious-PowerShell/) |
| SOC282 | [Deceptive Phishing Mail / AsyncRAT](./SOC282-Phishing/) |
| SOC176 | [RDP Brute Force](./SOC176-RDP-Brute-Force/) |
| SOC257 | [Unauthorized-Country VPN Attempt](./SOC257-Unauthorized-VPN/) |

## Evidence

Each investigation includes two primary screenshots:

- **Investigation Details** — alert metadata, affected host/source information and investigation details.
- **Investigation Results** — LetsDefend playbook outcome, classification and response decisions.

## Full Report

The complete PDF report is stored in this folder:

`LetsDefend-10-Alert-Investigation-Report.pdf`

## Methodology

See [methodology.md](./methodology.md) for the full investigation workflow used across the 10 alerts.

## Disclaimer

These investigations were performed in an authorized cybersecurity training environment on LetsDefend. This project is for educational and portfolio purposes.
