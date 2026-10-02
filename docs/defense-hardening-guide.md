# Vulnerability Analysis Guide

This guide explains a practical process for analyzing vulnerabilities in an operational environment.

## 1. What Is a Vulnerability?

A vulnerability is a weakness in a system, process, or implementation that an attacker may exploit to gain unauthorized access, escalate privileges, or disrupt services.

## 2. Vulnerability Triage Process

### Step 1: Identify the Asset
- Host or service name
- Operating system and version
- Application stack and version
- Exposure level
- Business criticality

### Step 2: Understand the Weakness
- Is it a code issue, configuration issue, or missing control?
- What CWE or CVE is associated?
- Has the vendor published a patch or advisory?

### Step 3: Determine Exploitability
- Is the vulnerable service internet-facing?
- Are authentication boundaries bypassed?
- Is user interaction required?
- Are there public exploits available?

### Step 4: Assess Impact
- Confidentiality: Is sensitive data at risk?
- Integrity: Could data be modified?
- Availability: Could services be disrupted?

### Step 5: Prioritize

Prioritization should use a combination of:

- Severity
- Asset criticality
- Attack surface
- Ease of exploitation
- Threat intelligence and observed activity

## 3. Example Vulnerability Categories

- Missing authentication or authorization checks
- SQL injection
- Remote code execution
- Command injection
- Broken access control
- Weak crypto or misconfiguration
- Unpatched third-party libraries
- Privilege escalation flaws

## 4. Remediation Strategies

- Patch the vulnerable component
- Disable the vulnerable feature
- Restrict access through firewall or WAF rules
- Enforce secure defaults and configuration baselines
- Add runtime detection and monitoring
- Validate the fix with testing and verification

## 5. Reporting a Vulnerability

A vulnerability report should include:

- Title and summary
- Affected system or service
- Technical root cause
- Risk or impact
- Steps to reproduce
- Indicators of compromise if relevant
- Recommended remediation

## 6. Best Practice

Do not treat all vulnerabilities as equal. A low-severity issue on an isolated system may be less urgent than a moderate issue on a public-facing critical service.

---

Use this document as a guide when conducting triage or preparing a vulnerability finding in a lab exercise.
