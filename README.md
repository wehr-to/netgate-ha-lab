🛡️ Netgate 6100 HA Firewall Lab — Enterprise-Style Networking in a Self-Contained Lab
Emulates a high-availability enterprise firewall and network stack using Netgate 6100 hardware, pfSense, VLANs, IDS, and automated infrastructure — built entirely offline and isolated from production networks.

🔧 Lab Features
✅ Active/Passive pfSense HA firewall with CARP failover
✅ Real-time Suricata IDS with Slack alerting
✅ Network-wide ad blocking via pfBlockerNG
✅ Segmented IoT VLAN for Arlo Cameras
✅ Local SIEM with log correlation
✅ Automated updates via Ansible for:
pfSense
Ubuntu
Docker services

✅ Self-contained environment (no ISP/modem needed)
✅ Hosted on Ubuntu Linux with Docker bridge services

📦 Services and Tools Used
Service	Purpose
pfSense (Netgate 6100 + VM)	Core firewall + failover
Suricata	Intrusion detection and network monitoring
pfBlockerNG	DNS-based ad/tracker blocking
Docker	Hosting bridge services and internal apps
Ansible	Infrastructure automation and config management
Ubuntu Server	Host OS for lab environment
Slack Webhooks	Alerting for IDS and system status
SIEM (e.g., Wazuh/Graylog)	Log collection and correlation

🔐 Security and Segmentation
IoT VLAN with strict east-west and north-south traffic rules
No external internet access by design (lab isolation)
IDS alerts for any anomalous behavior
DNS resolver configured for local trust

🚀 Goals and Learning Objectives
Practice enterprise firewall design without production risk
Understand failover, redundancy, and state synchronization
Build hands-on VLAN and routing experience
Develop Ansible playbooks for network ops automation
Strengthen Linux and containerization knowledge

📚 Future Enhancements
🗂️ Integrate NAS for internal backups, network file sharing, and VM/container storage
📊 Add NetFlow or sFlow collector for traffic analytics
🔐 Build out VPN gateway and secure remote access
🧱 Expand Zero Trust enforcement between VLANs
🪪 Replace Slack with self-hosted notification system (e.g., Mattermost, Ntfy)
🎯 Tune Suricata rulesets for lab-specific threat detection
📦 Add a GitOps-style CI/CD pipeline to auto-push changes to pfSense and Ansible
🧪 Simulate multi-WAN for failover and load balancing testing


