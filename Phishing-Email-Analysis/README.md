# Phishing Email Analysis

## Overview

This exercise focused on analyzing a phishing email using the same investigative process followed by Security Operations Center (SOC) analysts. Rather than relying on a single indicator, I learned how to evaluate multiple pieces of evidence before determining whether an email is malicious.

---

# Learning Objectives

After completing this exercise, I was able to:

- Verify the authenticity of an email sender.
- Analyze email headers.
- Identify suspicious links and domains.
- Perform static and dynamic analysis safely.
- Understand how attackers abuse trusted services.
- Apply critical thinking during phishing investigations.

---

# Email Authentication

One of the first steps in phishing analysis is verifying whether the sender is who they claim to be.

Email authentication relies on three important technologies:

| Technology | Purpose |
|------------|---------|
| SPF | Verifies that the sending mail server is authorized. |
| DKIM | Confirms that the email has not been altered during transmission. |
| DMARC | Defines how receiving mail servers should handle failed authentication checks. |

Although these checks improve trust, they do not guarantee an email is safe. If an attacker compromises a legitimate email account, authentication checks may still pass.

---

# Email Header Analysis

The email header contains routing information that reveals how an email traveled before reaching the recipient.

## From vs Reply-To

A mismatch between the **From** address and the **Reply-To** address is a common phishing indicator.

An email may appear to come from a trusted sender while directing replies to an attacker-controlled mailbox.

## Received Headers

The **Received** fields show the path an email followed through different mail servers.

Analysts read these entries from the bottom upward to identify the email's true origin.

---

# Determining the Scope

Analysts investigate whether:

- One user received the email.
- Multiple users received it.
- The entire organization was targeted.

This helps determine whether the attack is targeted spear phishing or a broader phishing campaign.

---

# Static Analysis

Static analysis involves inspecting suspicious content without executing it.

Common activities include:

- Hovering over links to reveal their actual destination.
- Checking domain registration dates.
- Reviewing reputation using VirusTotal.
- Looking for spelling errors and suspicious URLs.

Even if VirusTotal reports a link as clean, analysts should consider rescanning it because newly created phishing sites may not yet be detected.

---

# Dynamic Analysis

When further investigation is required, suspicious links or attachments should be opened only inside a secure sandbox environment.

This allows analysts to observe malicious behavior without risking production systems.

Some malware delays execution to avoid detection, so patience is important during analysis.

---

# Abuse of Trusted Services

Threat actors frequently abuse legitimate platforms such as:

- Google Drive
- Google Forms
- Microsoft OneDrive
- Dropbox

Using trusted services helps attackers bypass user suspicion and some security controls.

---

# Key Lessons Learned

- No single indicator proves an email is malicious.
- Email authentication improves trust but is not sufficient on its own.
- Email headers provide valuable forensic evidence.
- Static analysis should always be performed before interacting with suspicious content.
- Dynamic analysis should only be conducted in isolated environments.
- Effective phishing analysis requires evaluating multiple indicators together.

---

# Skills Developed

- Phishing Analysis
- Email Header Analysis
- Threat Intelligence
- Static Analysis
- Dynamic Analysis
- SOC Investigation
- Critical Thinking

---

# Reflection

This exercise changed how I evaluate suspicious emails. Instead of making decisions based on a single indicator, I learned to combine multiple pieces of evidence, such as authentication results, header analysis, domain reputation, and link inspection, before reaching a conclusion.

I also gained a deeper appreciation for the investigative mindset required of a SOC analyst, where careful observation and evidence-based reasoning are more valuable than assumptions.

---

> **Platform:** LetsDefend  
> **Category:** Phishing Analysis  
> **Documented in my own words for educational and portfolio purposes.**
