## Wazuh-based SOC monitoring, detection and response lab for Windows endpoint on VMware

A hands-on Security Operations Center (SOC) lab implementing centralized monitoring, detection, vulnerability assessment, and investigation workflows using a Wazuh-based platform deployed on VMware and monitoring a Windows 11 endpoint.

---

## Project Overview

This project demonstrates the design and operation of a functional SOC monitoring and detection environment capable of:

- Centralized endpoint visibility
- Real-time alerting and detection
- Vulnerability assessment and exposure tracking
- File integrity and configuration monitoring
- Analyst triage and investigation workflows

The lab is designed to replicate an entry-level SOC analyst operating environment.

---

## Architecture

**SOC Platform**

- Wazuh all-in-one server deployed from official OVA
- Web-based dashboard for monitoring and investigation
- Integrated manager, indexing, and API services

**Endpoint**

- Windows 11 Enterprise workstation
- Wazuh agent installed and registered to the manager

**High-level flow**

1. Endpoint telemetry ingestion
2. Event normalization and correlation
3. Alert generation
4. Analyst triage and investigation
5. Response and remediation decision

---

## Implemented SOC Capabilities

### Real-time Threat Detection

The Windows endpoint is monitored for:

- Process activity
- Security and system events
- Suspicious behavior patterns
- Policy and configuration violations

Alerts are generated and correlated by the Wazuh rules engine.

---

### Vulnerability Detection

The vulnerability detection module continuously evaluates:

- Installed software inventory
- Operating system exposure
- Known CVEs

This enables identification of:

- Missing patches
- Vulnerable applications
- High-risk software components

---

### File Integrity Monitoring (FIM)

The platform monitors:

- Critical system directories
- Configuration files
- Security-relevant artifacts

Unauthorized file or configuration changes generate security alerts.

---

### Configuration & Compliance Monitoring

Security baseline and configuration checks are used to support:

- System hardening validation
- Misconfiguration detection
- Security posture monitoring

---

## Example Investigation Use Case

**Finding**

- CVE ID: CVE-2025-55188  
- Affected software: 7-Zip 25.00 (x64)  
- Endpoint OS: Windows 11  
- Detection source: Wazuh vulnerability detection module  
- Platform severity: Low

**Analyst assessment**

- Vulnerability related to how 7-Zip handles extraction of specially crafted archives
- Potential for files to be written to unintended locations
- Relevant to workstation hardening and local attack surface reduction

**Recommended response**

- Upgrade or remove affected 7-Zip version
- Validate user privilege assignments
- Re-scan endpoint after remediation

---

## SOC Operational Workflow

1. Endpoint telemetry ingestion
2. Real-time alert generation
3. Severity-based triage
4. Alert contextualization using endpoint metadata
5. Investigation using:
   - event timelines
   - vulnerability data
   - file integrity alerts
6. Response and containment decision-making

---

## Validation Checklist

- Wazuh server reachable on network
- Dashboard accessible and operational
- Windows agent authenticated and active
- Alerts successfully generated and processed
- Endpoint telemetry visible in dashboard
- Vulnerability and configuration modules enabled

---

## Repository Structure

```text
wazuh-soc-lab-windows-endpoint/
│
├── README.md
├── architecture/
│   └── soc-architecture.png
├── deployment/
│   ├── wazuh-server-ova-deployment.md
│   ├── network-setup.md
│   └── validation.md
├── agent-onboarding/
│   └── windows-agent-install.md
├── detection-and-monitoring/
│   ├── threat-detection.md
│   ├── vulnerability-detection.md
│   └── fim-and-compliance.md
├── investigations/
│   └── vulnerability-case-7zip-cve.md
├── screenshots/
│   └── (dashboard and alert screenshots)
└── report/
    └── Design_and_Implementation_of_Wazuh_SOC.pdf
