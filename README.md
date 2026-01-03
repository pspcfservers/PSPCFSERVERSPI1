PSPCF SERVERS PI1

A professional Raspberry Pi server ecosystem built on Debian Trixie Lite, designed for security, branding, reproducibility, and community collaboration. This project is part of the PSPCF SERVERS COMMUNITY, showcasing how modest hardware can be transformed into a polished, scalable, and branded server hub.

Overview
PSPCF SERVERS PI1 integrates a curated stack of services — Nextcloud, Cockpit, Samba, and Tailscale — configured with strict security, professional branding, and reproducible documentation. Every component is modular, copy‑paste ready, and aligned with the PSPCF SERVERS identity.

Features

• Branded MOTD Dashboard: Custom ASCII banner with PSPCF SERVERS identity, showing CPU, RAM, disk usage, uptime, and active services.
• Secure Networking: UFW firewall exposing only essential ports (22, 445, 443, 9090, 465), Tailscale for encrypted remote access, SSL enforced for all web services.
• Service Stack: Nextcloud for cloud storage and collaboration, Cockpit for web dashboard and monitoring, Samba for branded file shares (Storage, Work, Entertainment).
• Alerts and Monitoring: SSH/Tailscale login and logout tracking, disk usage and service health checks, optional email or Telegram notifications.
• System Hygiene: Removed default shares and unnecessary services, clean professional environment with modular configs.


Installation

1. Flash Debian Trixie Lite onto Raspberry Pi.
2. Update system:
sudo apt update && sudo apt upgrade -y
3. Install core services:• Nextcloud (manual setup for reproducibility)
• Cockpit (sudo apt install cockpit)
• Samba (sudo apt install samba)
• Tailscale (curl -fsSL https://tailscale.com/install.sh | sh)

4. Configure firewall:
sudo ufw allow 22,445,443,9090,465/tcp
sudo ufw enable


Configuration

• MOTD Banner: Custom ASCII art plus system stats under PSPCF SERVERS branding.
• Samba Shares: Only branded folders exposed (Storage, Work, Entertainment).
• Firewall Rules: Minimal ports, strict logging, adaptive rules for evolving needs.
• Alerts: PAM hooks or cron scripts for login/logout events.


Roadmap

• Dynamic MOTD with live CPU, RAM, and disk stats.
• Automated backups with Borg or rsync.
• Branded landing page hub for all services.
• Netdata or Grafana dashboards for real‑time monitoring.
• Community documentation and tutorials.


Community Vision
PSPCF SERVERS PI1 is more than a server — it is a blueprint for professional Raspberry Pi deployments. By combining branding, security, and reproducibility, it empowers others to replicate and extend the project while reinforcing the PSPCF SERVERS identity. The long‑term vision is to grow the PSPCF SERVERS COMMUNITY into an inclusive ecosystem where technical solutions are easy to replicate, share, and improve.

License
MIT License — free to use, modify, and share with attribution.

