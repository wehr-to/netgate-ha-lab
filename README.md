## 🛡️ netgate-ha-firewall-lab
Enterprise-Grade Networking in a Self-Contained, Isolated Lab
A fully offline, high-availability (HA) firewall and enterprise-style network stack using Netgate 6100 hardware, pfSense, Suricata IDS, VLAN segmentation, and automated infrastructure with Ansible — all isolated from production environments.

## 🔧 Lab Features
- Active/Passive pfSense HA cluster with seamless failover (CARP-based)
- Suricata IDS with Slack webhook alerting
- pfBlockerNG for DNS-based ad/tracker blocking
- IoT VLAN with strict segmentation (e.g., Arlo Cameras)
- Local SIEM deployment (Wazuh or Graylog) for log ingestion and correlation
- Ansible automation for pfSense, Ubuntu, and Docker services
- Offline-first: Fully operational without ISP/modem
- Ubuntu-hosted infrastructure with Docker bridging

## 🧰 Services & Tooling
| Tool/Service        | Purpose                                            |
| ------------------- | -------------------------------------------------- |
| **pfSense**         | Enterprise-grade firewall, HA failover via CARP    |
| **Suricata**        | Intrusion detection and alerting                   |
| **pfBlockerNG**     | DNS-level ad/tracker blocking                      |
| **Docker**          | Hosting internal bridge services and test apps     |
| **Ansible**         | Infrastructure as Code (IaC) for config management |
| **Ubuntu Server**   | Host OS for all networking and containers          |
| **Slack Webhooks**  | Alerting system for IDS and HA status              |
| **Wazuh / Graylog** | Log aggregation, SIEM correlation                  |

## 🔐 Security and Segmentation
- IoT VLAN restricted with egress/ingress ACLs (east-west & north-south)
- Air-gapped from the internet by design
- DNS resolver restricted to trusted internal traffic
- IDS alerts triggered on unauthorized lateral movement or traffic anomalies

## 🎯 Learning Objectives
- Deploy and understand enterprise firewall HA design
- Gain hands-on experience with VLAN segmentation and routing
- Develop Ansible playbooks for real network automation tasks
- Strengthen my skills in Linux systems and Docker networking
- Emulate secure, modern enterprise network posture in a risk-free lab

## 🚀 Planned Enhancements
- NAS Integration for VM backups and shared lab storage
- VPN Gateway to simulate remote access and SASE environments
- NetFlow/sFlow Collector for traffic analytics
- Zero Trust ACLs across VLANs and enforcement zones
- Multi-WAN Failover Testing
- Replace Slack with self-hosted alerting (e.g., Mattermost, ntfy)
- Build CI/CD GitOps-style automation for firewall config and Ansible push
- Tune Suricata rules to match specific lab threats

## 🧠 Ideal For
- Aspiring Network Security Engineers
- Those prepping for CySA+, CASP, or enterprise firewall certs
- Home labbers who want production-grade design
- Security-focused DevOps / Infra Engineers











