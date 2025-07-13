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
sudo apt update && sudo apt upgrade -y
```
Set Up Static IP - 
 ```bash
Set Inside Router
```
Reboot Your Machine And SSH Back In 
```bash
sudo reboot
```
Install Doctor:
```bash
curl -sSL https://get.docker.com | sh
```
Set User To Docker Group 
```bash
sudo usermod -aG docker $USER
```
Reboot & SSH Back In 
```bash
sudo reboot
```
Install Doctor Compose 
```bash
sudo apt install docker-compose -y
```







