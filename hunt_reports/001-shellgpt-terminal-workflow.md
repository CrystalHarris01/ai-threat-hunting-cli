# Hunt Report 001: ShellGPT Terminal Workflow Setup

## Executive Summary

This report documents the initial setup of an AI-assisted threat hunting workflow using Parrot OS, ShellGPT, the OpenAI API, and a GitHub-based project structure.

The goal of this phase was to validate that terminal-based AI assistance can support cybersecurity documentation, folder-structure explanation, and future log-analysis workflows.

## Scope

This hunt report covers:

- Parrot OS terminal environment
- ShellGPT command-line AI integration
- GitHub project structure
- Initial documentation workflow

## Data Sources

- Parrot OS terminal output
- GitHub repository structure
- ShellGPT-generated explanation
- Screenshot evidence

## Activity Performed

The project folder structure was reviewed using the `tree` command and piped into ShellGPT for explanation in a cybersecurity portfolio context.

## Findings

ShellGPT successfully explained the repository structure and mapped each folder to its cybersecurity purpose.

The repository supports a structured threat hunting workflow through the following folders:

- `hunt_reports/` for investigation write-ups
- `sample_logs/` for log evidence and test data
- `screenshots/` for visual documentation
- `scripts/` for automation
- `sigma_rules/` for portable detection logic

## Security Relevance

This setup demonstrates an analyst-support workflow where AI can help summarize project structure, explain logs, draft findings, and support documentation.

AI output should not be treated as final evidence without analyst validation.

## MITRE ATT&CK Mapping

No adversary behavior was simulated in this setup phase.

Future reports will map observed activity to MITRE ATT&CK techniques.

## Evidence

Screenshot:

```text
screenshots/ai-threat-hunting-cli-structure-shellgpt.png
