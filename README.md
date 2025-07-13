# Stand-Ready Network 

A plug-and-play Raspberry Pi cybersecurity toolkit built to secure home and small business networks. Includes DNS filtering, VPN, monitoring, logging, and local dashboard control.

## 🔧 What's Inside
- Pi-hole (DNS/ad-blocking)
- WireGuard (secure VPN access)
- Prometheus + Grafana (monitoring)
- Nginx (custom local dashboard)
- node_exporter (system metrics)
- Rclone (cloud sync logs)

## 📦 Requirements
- Raspberry Pi 4 (4GB+)
- 32GB+ SD card
- Ethernet connection (recommended)
- Docker + Docker Compose

## 🚀 Quick Start
```bash
git clone https://github.com/Bmoney42/stand-ready-pi.git
cd stand-ready-pi/docker
cp .env.example .env
sudo docker-compose up -d
