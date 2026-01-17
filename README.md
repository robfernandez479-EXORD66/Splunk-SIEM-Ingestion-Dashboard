# Splunk SIEM Ingestion Dashboard
**Author:** Robert Fernandez  
**Purpose:** SOC Analyst portfolio project demonstrating ingestion, parsing, tuned detections, dashboards, and incident playbooks.

## What’s included
- **Realistic sample logs** (syslog, Windows security, cloud API, web proxy)
- **Ingestion examples** (UF inputs, HEC example)
- **Four tuned detections** with SPL and rationale
- **SOC Overview dashboard** (JSON panels)
- **Two incident playbooks** for triage and escalation
- **Scripts** to generate synthetic logs for demos

## Quick demo (local)
1. Install Splunk Enterprise or use Splunk Cloud trial (note Splunk version used: 9.x recommended).  
2. Enable HTTP Event Collector (HEC) or install a Universal Forwarder (UF).  
3. From repo root, run:
   - `python3 scripts/generate_synthetic_logs.py --out data_samples/` to create demo logs.
   - Use Splunk Add Data → Upload (for quick demo) or configure UF/HEC using `configs/inputs.conf.example`.
4. Import saved searches from `spl/detections` and import dashboard JSON from `dashboards/soc_overview.json`.
5. Review `playbooks/` for triage steps.

## Detections included
- Brute-force authentication (threshold + adaptive suppression)
- Suspicious process spawn from web proxy hosts
- DNS-based data exfiltration (high entropy + long query rate)
- Cloud IAM misuse (console login from new geo + privilege escalation)

## How to reproduce
- Exact Splunk version, sample ingestion commands, and dashboard import steps are in `/docs/architecture.md`.

## Skills demonstrated
- SPL, parsing (props/transforms), detection tuning, MITRE ATT&CK mapping, playbook writing, synthetic log generation.

## Contact
LinkedIn: Robert Fernandez
