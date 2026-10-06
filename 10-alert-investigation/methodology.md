# Investigation Methodology

The investigations followed a structured SOC alert investigation process.

## 1. Alert Review
Reviewed severity, event time, affected host, source/destination information, alert type and available MITRE ATT&CK mappings.

## 2. Evidence Collection
Depending on the alert, reviewed Log Management, Endpoint Security, Email Security, network activity, process history, browser history, terminal history, Threat Intelligence and VirusTotal.

## 3. Timeline Analysis
Compared timestamps to understand the order of events and reconstruct the activity.

## 4. Indicator Investigation
Investigated relevant IP addresses, domains, URLs, file hashes, processes, email addresses and malicious files.

## 5. Attack Chain Reconstruction
Connected related events to understand the attack path, including initial access, execution, discovery, privilege escalation and command-and-control activity where applicable.

## 6. Attack Success Assessment
Determined whether activity was attempted, blocked or successful based on the available evidence.

## 7. Response
Recommended containment, indicator blocking, credential resets, malware removal, patching, account review and Tier 2 escalation where appropriate.

## 8. Final Classification
Compared the evidence with the LetsDefend playbook and recorded the final disposition.

## 9. Documentation
Each alert is documented using:

- What Happened
- Evidence
- MITRE ATT&CK
- Actions
- Final Verdict / Risk
