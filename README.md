# Homelab Infra & Secure Ops / Ryzen 7 Node

This repository documents the infrastructure, containerization, and security hardening of my Ryzen 7-powered homelab node. It serves as the primary compute and observability engine in a segmented, zero-trust lab environment. Every component is designed with least privilege, visibility, and automation in mind.

---

## Architecture Overview

| Component         | Role                                               |
|------------------|----------------------------------------------------|
| **Ryzen 7 PC**    | Main workstation & container host (Ubuntu Desktop)|
| **Raspberry Pi 5**| Auxiliary DNS / Ad-block / standby firewall       |
| **Netgate 6100**  | Primary router and firewall (pfSense)             |
| **Ubiquiti USW Lite 16 PoE** | L2 switching & VLAN segmentation      |
| **NAS** *(future)*| Backup storage for SIEM logs & Ansible snapshots  |

>  **Goal:** Build a hardened, zero-trust lab environment with full observability, least privilege access, and minimal public exposure.

---

## Services & Tooling

| Layer               | Tools / Services                                    |
|--------------------|-----------------------------------------------------|
| **Containerization** | Docker + container tagging for segmentation        |
| **Reverse Proxy**  | NGINX with TLS, caching, and upstream control       |
| **Monitoring & SIEM** | Wazuh (SIEM), Grafana (performance), Suricata (IDS) |
| **Automation**     | Ansible for backups, updates, and Slack alerts      |
| **DNS & Security** | AdGuard Home, DNS-based phishing sinkhole           |
| **Access Control** | Authelia (proxy auth), SSH key-only access          |
| **Segmentation**   | VLANs via pfSense and managed switch                |

---

## Security Highlights

- **No public services** exposed without proxy-level auth
- **No root or admin** logins by default (least privilege enforced)
- **VLANs** isolate IoT, infra, DNS, and management traffic
- **SSH** hardened with keys, fail2ban, firewall rules
- **Audit-ready** config templates and recovery scripts
- **Future NAS integration** for log retention and off-host backups

## Check out:
- ansible/playbooks/ for auto-patching and backup jobs
- docker/ for hardened services and proxy architecture
- hardening/ for baseline config templates
- monitoring/ for Wazuh and Grafana container configs

## Future Enhancements
- Deploy NAS for SIEM logs & monthly Ansible snapshots
- Integrate Authelia into NGINX reverse proxy flow
- Add Portainer for container visibility (internally only)
- Centralize log aggregation with Rsyslog or Loki
- Enable full GitOps-style redeployments from this repo












