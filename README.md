# Dotfiles

Конфігураційні файли для zsh, tmux, nvim, alacritty, ghostty, bat, starship та zed.

## Встановлення

### 1. Встановити Oh My Zsh
```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

### 2. Клонувати плагіни tmux
```bash
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
```

### 3. Клонувати репозиторій у домашню директорію
```bash
cd ~
git clone <url-репозиторію> dotfiles
```

### 4. Застосувати конфігурації через stow
```bash
cd ~/dotfiles
stow .
```

### 5. Встановити плагіни tmux
Запустити tmux і натиснути `prefix + I` (зазвичай `Ctrl+b` потім `Shift+i`)
