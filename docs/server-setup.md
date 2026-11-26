# Server setup

Tested on: Debian 13 (trixie), Intel Core i5-7300HQ, 8GB RAM.

## 1. Packages

```bash
sudo apt install -y git ffmpeg python3 curl ca-certificates
```

- Docker Engine + Compose plugin from Docker's apt repository:
  https://docs.docker.com/engine/install/debian/ , then `sudo usermod -aG docker $USER`
- GitHub CLI from its official apt repository:
  https://github.com/cli/cli/blob/trunk/docs/install_linux.md
- uv: `curl -LsSf https://astral.sh/uv/install.sh | sh`

## 2. Network

- DHCP reservation: server 192.168.50.4, camera 192.168.50.23.
- No ports are forwarded on the router.

## 3. Project

```bash
gh auth login
gh repo clone <login>/cam-voice-assistant
cd cam-voice-assistant && uv sync
```
