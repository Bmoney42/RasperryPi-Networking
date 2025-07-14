# Stand-Ready Network 

A plug-and-play Raspberry Pi cybersecurity toolkit built to secure home and small business networks. Includes DNS filtering, VPN.

## 🔧 What's Inside
- Pi-hole (DNS/ad-blocking)
- WireGuard (secure VPN access)
More Coming Soon!

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
Make Directory 
```bash
Mkdir  -p ~/stand-ready/docker
cd ~/stand-ready/docker
```
Make Our Requirements For Docker ** Edit the YAML file To Set Your Password **# FTLCONF_webserver_api_password: 'YourSecurePassword'**
```bash
Nano docker-compose.yml 
Control+O 
enter 
Control+X
```
Start The Dock
```bash
docker-compose up -d
```
Login Using Your Ip/Port And Password And You Should See The Dashboard! 

Lets Start WireGuard - Check Config File If Its Filled Out
```bash
docker exec -it wireguard cat /config/peer1/peer1.conf
```

Generate QR Code And Scan To Set Up Phone For WireGuard 
```bash
docker exec -it wireguard /app/show-peer 1
```

Once containers are running:

Visit: http://<YOUR_PI_IP>:8080/admin

Login with the password you set

🔐 Set Up WireGuard VPN
6. Confirm VPN Config
```bash
docker exec -it wireguard cat /config/peer1/peer1.conf
```
7. Generate QR Code (for your phone)
```bash
docker exec -it wireguard /app/show-peer 1
```
Open the WireGuard app, scan the QR code, and toggle the tunnel on.


**Turn on the VPN**

--Visit http://10.13.13.1/admin to confirm access

--Visit https://icanhazip.com → should show your home IP

--Visit https://example.com → confirms internet works
