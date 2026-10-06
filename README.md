# LetsDefend SOC Investigation Write-ups

Hands-on SOC Analyst investigations completed through **LetsDefend**.

This repository documents 10 security alerts investigated from alert validation through evidence collection, attack-chain reconstruction, MITRE ATT&CK mapping, response actions, and final classification.

## 🎯 Project Goal

The goal of this project is to demonstrate practical SOC Analyst skills, including:

- Alert triage and validation
- Log analysis and event correlation
- Endpoint investigation
- Phishing and malware analysis
- Web attack investigation
- Threat intelligence enrichment
- MITRE ATT&CK mapping
- Incident response and containment
- Tier 2 escalation decisions
- Security documentation

## 🔎 Investigation Methodology

**Validate → Collect Evidence → Correlate Events → Reconstruct the Attack → Assess Success/Impact → Respond → Classify → Document**

For each alert, I reviewed the alert details, identified relevant indicators, correlated available logs and security-tool evidence, assessed whether the attack succeeded, and documented recommended response actions.

## 📂 10-Alert Investigation Project

| Alert | Investigation | Result |
|---|---|---|
| SOC335 | [CVE-2024-49138 Exploitation](./10-alert-investigation/SOC335-CVE-2024-49138) | True Positive |
| SOC336 | [Windows OLE Zero-Click RCE – CVE-2025-21298](./10-alert-investigation/SOC336-CVE-2025-21298) | True Positive |
| SOC342 | [SharePoint ToolShell Auth Bypass & RCE – CVE-2025-53770](./10-alert-investigation/SOC342-CVE-2025-53770) | True Positive |
| SOC274 | [PAN-OS Command Injection – CVE-2024-3400](./10-alert-investigation/SOC274-CVE-2024-3400) | True Positive |
| SOC127 | [SQL Injection](./10-alert-investigation/SOC127-SQL-Injection) | True Positive |
| SOC338 | [Lumma Stealer / ClickFix Phishing](./10-alert-investigation/SOC338-Lumma-Stealer) | True Positive |
| SOC153 | [Suspicious PowerShell](./10-alert-investigation/SOC153-Suspicious-PowerShell) | True Positive |
| SOC282 | [Deceptive Phishing Mail](./10-alert-investigation/SOC282-Phishing) | True Positive |
| SOC176 | [RDP Brute Force](./10-alert-investigation/SOC176-RDP-Brute-Force) | True Positive |
| SOC257 | [Unauthorized-Country VPN Attempt](./10-alert-investigation/SOC257-Unauthorized-VPN) | True Positive |

## 🖼️ Evidence

Each investigation uses two primary screenshots:

1. **Investigation Details** — alert metadata and investigation information.
2. **Investigation Results** — LetsDefend playbook answers, outcome and response decisions.

Additional supporting screenshots are included where useful, such as Log Management, Threat Intelligence, VirusTotal, endpoint and network evidence.

## 🛠️ Skills Demonstrated

- SOC alert triage
- Security event correlation
- Windows investigation
- RDP investigation
- PowerShell analysis
- Phishing investigation
- Malware analysis
- Web attack analysis
- Threat intelligence
- IOC investigation
- MITRE ATT&CK
- Incident response
- Containment and escalation

## ⚠️ Disclaimer

These investigations were performed in an authorized cybersecurity training environment on LetsDefend. The repository is for educational and portfolio purposes.
