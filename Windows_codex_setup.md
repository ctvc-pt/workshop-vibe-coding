# WSL + Codex Setup Guide

## Windows PowerShell (Admin)

```powershell
wsl --install
wsl --set-default-version 2
wsl --install -d Ubuntu
```

- Restart the computer after the commands finish running.
- When the system reboots, Ubuntu should open automatically and prompt for a Linux username and password.

> Note: When you type your password nothing appears on the screen, but it is being recorded. Press Enter when you finish typing.

**If Ubuntu does not open automatically**

1. Launch Windows PowerShell as Administrator.
2. Run `wsl --install -d Ubuntu`.

## Inside Ubuntu

```bash
sudo apt update
sudo apt upgrade -y
```

> Note: `sudo apt update` will ask for your password. If you see `sudo: command not found` or sudo access is disabled, go to Windows Settings → System → For Developers → Windows Subsystem for Linux → Sudo and enable “Enable sudo”.

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
source ~/.bashrc
nvm install --lts
nvm use --lts
```

```bash
npm install -g @openai/codex
```

> Note: Choose the folder you want to work in with `cd folder_name` before launching Codex.

## Launch Codex

```bash
codex
```
