# Codex Setup Guide

## Mac Terminal

```powershell
brew update
```
- Doesn't work?
  
```powershell
xcode-select --install
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
```
> Note: On Intel Macs, the path is usually /usr/local/bin/brew. The installer will show the correct line, just copy and paste it into the Terminal.
> Try again brew update

```powershell
brew upgrade
```

>Note: Can take a while

```powershell
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
source ~/.zshrc
```

- Doesn't work?

```powershell
touch ~/.zshrc
echo 'export NVM_DIR="$HOME/.nvm"' >> ~/.zshrc
echo '[ -s "$NVM_DIR/nvm.sh" ] && . "$NVM_DIR/nvm.sh"' >> ~/.zshrc
source ~/.zshrc
```

***How to get SSH Key?***

-Terminal 

```powershell
ssh-keygen -t ed25519 -C "your-email@example.com"
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
pbcopy <~/.ssh/id_ed25519.pub
```

***Install Codex on Mac***

```bash
nvm install --lts
nvm use --lts
npm install -g @openai/codex
```

> Note: Choose the folder you want to work in with `cd folder_name` before launching Codex.

## Launch Codex

```bash
codex
```

[Codex API](https://pastebin.com/srcYagdG)
