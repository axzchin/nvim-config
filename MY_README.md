# My Neovim Configuration (based on Kickstart.nvim)

This is my personal Neovim configuration, built on top of **[Kickstart.nvim](https://github.com/nvim-lua/kickstart.nvim)** – a starting point for Neovim that is not a distribution, but a well‑commented `init.lua` you can fully understand and modify.

I’ve added:
- **Obsidian.nvim** for note‑taking with my Obsidian vault.
- **Bullets.vim** for auto‑bullet lists in Markdown.
- Personal keymaps, UI tweaks, and a portable vault path using environment variables.

---

## 🚀 Installation

### Prerequisites
- Neovim ≥ 0.10.0
- `ripgrep` – for Telescope and Obsidian search
- `xclip` or `wl‑clipboard` – for pasting images (if using Obsidian)

### Clone this repository
```bash
git clone git@github.com:axzchin/nvim-config.git ~/.config/nvim
```

### Set your Obsidian vault path (optional)
If you use Obsidian, set the environment variable:
```bash
export OBSIDIAN_VAULT="/path/to/your/vault"
```
Add that to your `~/.bashrc` or `~/.zshrc`. If not set, the config falls back to `~/Documents/Obsidian/Vault`.

### Start Neovim
```bash
nvim
```
Plugins will be automatically installed via `vim.pack`.

---

## 🔁 Repository Structure

This repository is not a fork of Kickstart; instead, it tracks the upstream Kickstart repository as a remote (`upstream`) so that I can merge future improvements while maintaining my own changes.

- **`origin`** → `git@github.com:axzchin/nvim-config.git` (my personal remote)
- **`upstream`** → `https://github.com/nvim-lua/kickstart.nvim.git` (original Kickstart)

---

## 📥 Keeping Up‑to‑Date with Kickstart

To pull in the latest changes from the original Kickstart repository:

```bash
git fetch upstream
git checkout master
git merge upstream/master
```

If there are merge conflicts, resolve them, then:
```bash
git add .
git commit -m "Merge upstream changes"
```

Then push your updated config to your own remote:
```bash
git push origin master
```

---

## 📤 Pushing Your Own Changes

After making modifications to your config:

```bash
git add .
git commit -m "Describe your changes"
git push origin master
```

---

## 🛠️ Customisation Tips

- **Vault path**: Modify the `VAULT_PATH` variable in `init.lua` or set `OBSIDIAN_VAULT`.
- **Keymaps**: Additional keymaps are documented inside the file.
- **Plugins**: Add new plugins using `vim.pack.add { "url" }`.

---

## 🙏 Acknowledgements

This config is built on the excellent work of:
- [Kickstart.nvim](https://github.com/nvim-lua/kickstart.nvim) by TJ DeVries and contributors.
- [Obsidian.nvim](https://github.com/obsidian-nvim/obsidian.nvim)
- [Bullets.vim](https://github.com/bullets-vim/bullets.vim)

---

## 📝 License

Same as Kickstart – use at your own risk, feel free to copy and modify.
```

---

Save this as `README.md` in the root of your repository, then add, commit, and push it.

```bash
git add README.md
git commit -m "Add README with upstream instructions"
git push origin master
```

