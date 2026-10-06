# SOC176 — RDP Brute Force Detected

**Severity:** Medium  
**Type:** Brute Force  
**Result:** True Positive  
**Host:** Matthew (172.16.17.148)  
**Source:** 218.92.0.56  
**Event ID:** 234  
**Risk:** 20/25 — Critical

## 1. What Happened

An external attacker performed repeated RDP login attempts against Matthew's endpoint. Multiple usernames were attempted before a successful login occurred.

After access was obtained, command-line activity showed the attacker performing system and account enumeration.

## 2. Evidence

### Investigation Details
![Investigation Details](./images/SOC176-investigation-details.png)

### Investigation Results
![Investigation Results](./images/SOC176-investigation-results.png)

### Supporting Evidence

- Source IP: `218.92.0.56`
- Multiple RDP attempts were observed.
- The source was associated with malicious/abusive activity.
- A successful RDP login provided desktop access.
- `cmd.exe` was launched from the desktop environment.
- Commands included `whoami`, `net user letsdefend`, `net localgroup administrators` and `netstat -ano`.
- `net user letsdefend` was enumeration activity; the compromised user context was Matthew.

## 3. MITRE ATT&CK

- **T1110** — Brute Force
- **T1078** — Valid Accounts
- **T1059.003** — Windows Command Shell
- **T1033** — System Owner/User Discovery
- **T1087** — Account Discovery
- **T1069.001** — Permission Groups Discovery: Local Groups
- **T1049** — System Network Connections Discovery

## 4. Actions

- Isolate Matthew's endpoint.
- Escalate to Tier 2.
- Block the source IP.
- Reset the affected account credentials.
- Review RDP exposure and enforce MFA.
- Hunt for additional activity from the same source.

## Final Verdict

**True Positive — RDP brute force led to successful access and post-login enumeration.**
