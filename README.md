# Cybersecurity Defense Frameworks & Detection Rules

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

**Open-source cybersecurity defense resources** developed by [Shakil Md. Rezwanul Bari](https://www.linkedin.com/in/rezwanulbari) — a cybersecurity architect with 17+ years of experience protecting critical infrastructure across financial services, cloud technology, and international development sectors.

## Overview

This repository contains replicable, framework-agnostic cybersecurity defense resources including:

- **Sigma Detection Rules** — Vendor-neutral detection rules mapped to MITRE ATT&CK for use in any SIEM platform
- **YARA Rules** — Pattern-matching rules for malware detection, webshell identification, and exploit analysis
- **Playbook Templates** — Standardized incident response, threat hunting, and compliance automation playbook templates aligned with MITRE ATT&CK and D3FEND frameworks

These resources are designed to be **transferable and adoptable** by any security operations team, regardless of industry vertical or tooling.

## Repository Structure

```
├── sigma-rules/
│   ├── web-attacks/          # Web application attack detection
│   ├── credential-access/    # Credential theft and abuse detection
│   ├── lateral-movement/     # Lateral movement detection
│   ├── exfiltration/         # Data exfiltration detection
│   └── persistence/          # Persistence mechanism detection
├── yara-rules/
│   ├── malware/              # Malware family detection
│   ├── webshells/            # Web shell detection
│   └── exploits/             # Exploit payload detection
├── playbook-templates/
│   ├── incident-response/    # IR playbook templates
│   ├── threat-hunting/       # Threat hunting playbook templates
│   └── compliance/           # Compliance automation templates
└── docs/
    ├── MITRE-MAPPING.md      # ATT&CK technique mapping reference
    └── DEPLOYMENT-GUIDE.md   # Deployment and integration guide
```

## Framework Alignment

All detection rules and playbooks are mapped to industry-standard frameworks:

| Framework | Coverage |
|-----------|----------|
| **MITRE ATT&CK** | Technique IDs mapped to every detection rule |
| **MITRE D3FEND** | Defensive technique alignment for playbooks |
| **NIST CSF 2.0** | Control mapping for compliance templates |
| **PCI-DSS v4.0.1** | Financial sector compliance mapping |
| **ISO 27001:2022** | Information security management alignment |

## Getting Started

### Sigma Rules
Sigma rules can be converted to your SIEM's native query language using [sigmac](https://github.com/SigmaHQ/sigma) or [pySigma](https://github.com/SigmaHQ/pySigma).

```bash
# Convert to Splunk SPL
sigmac -t splunk sigma-rules/credential-access/brute_force_auth_failures.yml

# Convert to Microsoft Sentinel KQL
sigmac -t ala sigma-rules/credential-access/brute_force_auth_failures.yml
```

### YARA Rules
YARA rules can be deployed with any YARA-compatible tool:

```bash
yara -r yara-rules/malware/ransomware_indicators.yar /path/to/scan
```

### Playbook Templates
Playbook templates are provided in YAML/Markdown format and can be imported into SOAR platforms (Cortex XSOAR, Splunk SOAR, IBM Resilient) or used as standard operating procedures.

## Background

These resources were developed through 17+ years of hands-on cybersecurity operations across:
- **Financial Services** — Bank Asia PLC, NCC Bank PLC, BA Express
- **Cloud Technology** — Cloud Himalaya
- **International Development** — IDRA (World Bank project)
- **Education** — Daffodil Institute of IT

Key results achieved using these methodologies:
- 60% reduction in incident response time
- 45% reduction in MTTD/MTTR
- 40% reduction in false positives
- 80% improvement in security posture (PCI-DSS v4.0.1)

## Contributing

Contributions are welcome! Please submit a pull request with:
1. A clear description of the detection logic or playbook
2. MITRE ATT&CK technique mapping
3. Test cases or validation methodology

## License

This project is licensed under the MIT License — see [LICENSE](LICENSE) for details.

## Author

**Shakil Md. Rezwanul Bari**
- LinkedIn: [linkedin.com/in/rezwanulbari](https://www.linkedin.com/in/rezwanulbari)
- Email: rezwanbari@gmail.com
- Certifications: CISM, CISA, CySA+, Security+, AWS SA, Azure SC-100, AZ-500, CEH, Splunk ES Admin, ISO 27001 LA (18 total)
