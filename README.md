# dotfiles

Personal dotfiles managed with [chezmoi](https://www.chezmoi.io/).

## 🚀 Quick Start (Installation)

On a new machine, you can initialize and apply these dotfiles with a single command:

```bash
sh -c "$(curl -fsLS get.chezmoi.io)" -- init --apply orrisroot
```

If `chezmoi` is already installed:

```bash
chezmoi init --apply orrisroot
```

---

## 📂 Included Configurations

- **Bash (`~/.bashrc.d/`)**: Modular bash scripts
  - `deno`: Deno runtime environment settings
  - `gpg`: GPG / SSH agent configuration
  - `javaenv`: Java SDK / environment variables
  - `opencode`: OpenCode development tools configuration
  - `rust`: Cargo / Rust toolchain paths
  - `zzz-dedupe-path`: PATH deduplication utility
- **Alacritty (`~/.config/alacritty/`)**: Terminal emulator configuration (`alacritty.toml`)
- **Git (`~/.gitconfig`)**: User information, commit signing (GPG), LFS, and credential helpers
- **Readline (`~/.inputrc`)**: Terminal input / editing keybindings

---

## 🛠 Useful chezmoi Commands

| Command | Description |
| :--- | :--- |
| `chezmoi edit <file>` | Edit the source file for the specified target (e.g. `chezmoi edit ~/.config/alacritty/alacritty.toml`) |
| `chezmoi diff` | Show diff between target state and current state in home directory |
| `chezmoi apply` | Apply changes to the home directory |
| `chezmoi cd` | Open a shell in the chezmoi source directory (`~/.local/share/chezmoi`) |
| `chezmoi update` | Pull latest changes from git repository and apply them |
| `chezmoi status` | Check status of managed files |
