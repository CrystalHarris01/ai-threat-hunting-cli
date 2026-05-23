# AI Threat Hunting CLI

AI Threat Hunting CLI is a beginner-friendly cybersecurity portfolio project focused on using terminal-based AI assistance to support threat hunting, alert triage, log review, and detection documentation.

This project is designed as a practical lab that combines Parrot OS, ShellGPT/OpenAI API usage, Wazuh, Sysmon, Windows endpoint telemetry, sample logs, Sigma rules, and structured hunt reports.

## Project Purpose

The purpose of this repository is to demonstrate a repeatable threat hunting workflow:

1. Collect or generate security telemetry.
2. Review logs and suspicious activity.
3. Use AI assistance to summarize and explain findings.
4. Map behavior to MITRE ATT&CK.
5. Write detection logic.
6. Document findings in a professional hunt report.

This is not meant to replace analyst judgment. The AI assistant is used as a support tool for explanation, summarization, and documentation while the analyst validates evidence manually.

## Lab Architecture

Planned lab components:

| Component | Purpose |
|---|---|
| Parrot OS | Analyst workstation and terminal environment |
| ShellGPT | Terminal-based AI assistant |
| OpenAI API | AI model access for analysis prompts |
| Windows VM | Endpoint telemetry source |
| Sysmon | Windows process and event visibility |
| Wazuh | SIEM/XDR platform for alerting and dashboards |
| Sample logs | Safe test data for repeatable investigations |
| Sigma rules | Portable detection logic |

## Planned Folder Structure

```text
ai-threat-hunting-cli/
├── README.md
├── sample_logs/
├── hunt_reports/
├── sigma_rules/
├── screenshots/
└── scripts/
```

## Initial Threat Hunting Scenarios

### Scenario 1: Nmap Reconnaissance

Simulate or analyze network scanning activity and document signs of reconnaissance.

Potential indicators:

- Multiple ports probed in a short time window
- SYN scan behavior
- Unusual source host activity
- Service enumeration attempts

MITRE ATT&CK mapping:

- T1046 - Network Service Discovery

### Scenario 2: Suspicious PowerShell

Analyze PowerShell activity for signs of abuse.

Potential indicators:

- Encoded PowerShell commands
- Suspicious parent-child process relationships
- Download cradle behavior
- Hidden or bypass execution flags

MITRE ATT&CK mapping:

- T1059.001 - PowerShell

### Scenario 3: Authentication Brute Force

Review failed login activity and identify possible brute-force behavior.

Potential indicators:

- Repeated failed logins
- Multiple attempts against one account
- Multiple accounts targeted from one host
- Login attempts outside normal activity windows

MITRE ATT&CK mapping:

- T1110 - Brute Force

## Example Terminal Usage

```bash
sgpt "Explain what a SIEM is in one paragraph."
```

```bash
cat sample_logs/example.log | sgpt "Identify suspicious behavior and map it to MITRE ATT&CK."
```

## Hunt Report Template

Each investigation should include:

- Executive summary
- Scope
- Data sources
- Timeline
- Findings
- Indicators of compromise
- MITRE ATT&CK mapping
- Detection logic
- Remediation recommendations
- Lessons learned

## Safe Use Statement

This project is for defensive security education, detection engineering, and portfolio development only. Any attack simulations should be performed only in a lab environment owned or explicitly authorized by the user.

Do not run scans, brute-force tools, exploit code, or suspicious scripts against systems without permission.

## Portfolio Goal

This project is intended to show practical ability in:

- Threat hunting
- SOC investigation workflow
- SIEM/log analysis
- Detection documentation
- MITRE ATT&CK mapping
- AI-assisted cybersecurity workflows
- GitHub-based technical documentation

## Status

Project initialized. Future updates will add sample logs, Sigma rules, scripts, screenshots, and completed hunt reports.
