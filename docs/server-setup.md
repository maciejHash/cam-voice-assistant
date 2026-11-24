# Server setup

Tested on: Ubuntu Server 24.04 LTS, <CPU>, <RAM>.

## 1. Packages

```bash
sudo apt install -y git gh ffmpeg docker.io docker-compose-v2
sudo usermod -aG docker $USER
curl -LsSf https://astral.sh/uv/install.sh | sh
```

## 2. Network

- DHCP reservation: server 192.168.50.4, camera 192.168.50.23.
- No ports are forwarded on the router.

## 3. Project

```bash
gh auth login
gh repo clone <login>/cam-voice-assistant
cd cam-voice-assistant && uv sync
```
