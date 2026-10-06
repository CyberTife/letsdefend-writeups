# SOC282 — Phishing Alert: Deceptive Mail Detected

**Severity:** Medium  
**Type:** Exchange  
**Result:** True Positive  
**Host:** Felix  
**Source:** 103.80.134.63  
**Event ID:** 257  
**Risk:** 25/25 — Critical

## 1. What Happened

Felix received a phishing email from a deceptive domain offering a free coffee voucher. The email was delivered and the user downloaded `free-coffee.zip`.

The investigation showed that the downloaded file was associated with **AsyncRAT** and that the endpoint communicated with an external C2 address.

## 2. Evidence

### Investigation Details
![Investigation Details](./images/SOC282-investigation-details.png)

### Investigation Results
![Investigation Results](./images/SOC282-investigation-results.png)

### Supporting Evidence

- Sender: `free@coffeeshooop.com`
- Subject: **Free Coffee Voucher**
- The email was delivered.
- Felix downloaded `free-coffee.zip`.
- Network activity connected to `37.120.233.226`.
- Threat Intelligence associated the activity with AsyncRAT and C2.
- Terminal activity included `systeminfo`, `hostname`, `wmic logicaldisk`, `net user`, `tasklist /svc`, `ipconfig /all` and `route print`.

## 3. MITRE ATT&CK

- **T1566** — Phishing
- **T1204.002** — User Execution: Malicious File
- **T1059.003** — Windows Command Shell
- **T1082** — System Information Discovery
- **T1033** — System Owner/User Discovery
- **T1087** — Account Discovery
- **T1057** — Process Discovery
- **T1016** — System Network Configuration Discovery
- **T1071** — Application Layer Protocol

## 4. Actions

- Contain Felix's endpoint and escalate.
- Delete the phishing email.
- Block the malicious domain and C2 IP.
- Reset affected credentials.
- Remove the malware or reimage the endpoint if required.
- Hunt for the C2 indicator across the environment.

## Final Verdict

**True Positive — phishing led to malware execution and suspicious C2 activity.**
