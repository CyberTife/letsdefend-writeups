# SOC153 — Suspicious PowerShell Script Executed

**Severity:** Medium  
**Type:** Malware  
**Result:** True Positive  
**Host:** Tony (172.16.17.206)  
**Event ID:** 238  
**Risk:** 20/25 — Critical

## 1. What Happened

A PowerShell script named `payload_1.ps1` was downloaded and executed on Tony's endpoint. Endpoint security detected the activity but did not quarantine the payload.

The investigation also showed DNS and HTTPS communication with infrastructure associated with the malicious activity and evidence of a possible second-stage payload.

## 2. Evidence

### Investigation Details
![Investigation Details](./images/SOC153-investigation-details.png)

### Investigation Results
![Investigation Results](./images/SOC153-investigation-results.png)

### Supporting Evidence

- `payload_1.ps1` was downloaded from the LetsDefend file server.
- VirusTotal identified the script as malicious and associated it with a trojan downloader.
- EDR detected the payload but did not block/quarantine it.
- Sysmon DNS telemetry resolved `kionagranada.com`.
- Network logs showed HTTPS communication to the resolved IP.
- VirusTotal sandbox evidence showed a possible second-stage executable named `beauty.exe`.

## 3. MITRE ATT&CK

- **T1189** — Drive-by Compromise
- **T1204.002** — User Execution: Malicious File
- **T1059.001** — PowerShell
- **T1071.001** — Web Protocols
- **T1105** — Ingress Tool Transfer

## 4. Actions

- Contain and escalate the endpoint.
- Block the malicious domain and IP.
- Remove `payload_1.ps1` and investigate `beauty.exe`.
- Reset potentially exposed credentials.
- Hunt for the file hash and C2 indicators across the environment.

## Final Verdict

**True Positive — malicious PowerShell execution with suspicious network activity.**
