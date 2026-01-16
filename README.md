# Dotfiles

Конфігураційні файли для zsh, tmux, nvim, alacritty, ghostty, bat, starship та zed.

## Залежності

Встановити через Homebrew:
```bash
brew install eza fd fzf ripgrep bat zoxide starship stow neovim tmux
```

## Встановлення

### 1. Встановити Oh My Zsh
```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

### 2. Встановити плагіни zsh
```bash
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
git clone https://github.com/zsh-users/zsh-syntax-highlighting ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

### 3. Клонувати плагіни tmux
```bash
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
```

### 4. Клонувати репозиторій у домашню директорію
```bash
cd ~
git clone <url-репозиторію> dotfiles
```

### 5. Застосувати конфігурації через stow
```bash
cd ~/dotfiles
stow .
```

### 6. Встановити плагіни tmux
Запустити tmux і натиснути `prefix + I` (зазвичай `Ctrl+b` потім `Shift+i`)

## Основні інструменти та аліаси

### Zsh
- `ls` → `eza --icons --group-directories-first`
- `ll` → `eza -l --git` (детальний список)
- `la` → `eza -la --git` (з прихованими файлами)
- `lt` → `eza --tree --level=2` (дерево файлів)
- `cat` → `bat` (підсвітка синтаксису)
- `cd` → `z` (zoxide - швидка навігація)

### FZF (Ctrl+R, Ctrl+T)
- `Ctrl+T` - пошук файлів з попереднім переглядом через bat
- `Ctrl+R` - пошук в історії команд
- `Ctrl+/` - перемикання попереднього перегляду

### Tmux
- `Ctrl+b` - prefix
- `prefix + |` - вертикальний split
- `prefix + -` - горизонтальний split
- `Ctrl+h/j/k/l` - навігація між панелями (vim-tmux-navigator)
- `prefix + I` - встановити плагіни

### Neovim (LazyVim)
- `<leader>` = `Space`
- `<leader>ff` - пошук файлів
- `<leader>sg` - пошук по тексту (grep)
- `<leader>e` - файловий менеджер
- `gcc` - закоментувати рядок
- `Ctrl+h/j/k/l` - навігація між вікнами tmux/nvim

**LSP та екстра:**
- LazyVim з автоматичним LSP
- Catppuccin Mocha тема
- Treesitter для підсвітки синтаксису
- vim-tmux-navigator для інтеграції з tmux
