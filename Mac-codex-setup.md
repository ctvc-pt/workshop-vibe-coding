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

