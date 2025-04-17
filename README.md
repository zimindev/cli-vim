# 📝 Vim — The Ubiquitous Text Editor

`vim` (Vi IMproved) is a powerful, fast, and highly configurable terminal-based text editor. It's ideal for everything from quick edits to full-scale coding — and it’s available on virtually every Unix system.

---

## ✅ Features

- Modal editing (normal, insert, visual, command modes)
- Syntax highlighting for hundreds of languages
- Macros, registers, and recording
- Powerful search and replace
- Extensible with plugins and `.vimrc` config
- Works inside a terminal, even over SSH

---

## 🔧 Installation

### On Debian/Ubuntu:
```bash
sudo apt update && sudo apt install vim
```

### On Arch Linux:
```bash
sudo pacman -S vim
```

### On macOS (via Homebrew):
```bash
brew install vim
```

---

## 🚀 Launching Vim

```bash
vim filename.txt
```

If the file doesn't exist, Vim will create it when you save.

---

## 🧠 Vim Modes

| Mode         | Description                         | Enter With     |
|--------------|-------------------------------------|----------------|
| Normal       | Default mode for navigation         | `<Esc>`        |
| Insert       | Typing text like a regular editor   | `i`, `a`, `o`  |
| Visual       | Select text for copying/deleting    | `v`, `V`, `Ctrl+v` |
| Command      | Execute commands like `:w`, `:q`    | `:`            |

---

## ⌨️ Essential Keybindings

### ⬅️ Navigation

| Key        | Action                                |
|------------|----------------------------------------|
| `h` `j` `k` `l` | Move left/down/up/right          |
| `w` / `b`   | Jump to next/previous word            |
| `gg` / `G`  | Go to start / end of file             |
| `0` / `^` / `$` | Line start / first char / end    |

### 📝 Insert Mode

| Key      | Description                             |
|----------|-----------------------------------------|
| `i`      | Insert before cursor                    |
| `a`      | Append after cursor                     |
| `o`      | Open a new line below                   |
| `I` / `A`| Insert/Append at start/end of line      |
| `<Esc>`  | Return to normal mode                   |

### 🔨 Editing

| Key         | Action                                |
|-------------|----------------------------------------|
| `x`         | Delete character under cursor          |
| `dd`        | Delete line                            |
| `yy`        | Yank (copy) line                       |
| `p`         | Paste after cursor                     |
| `u`         | Undo                                   |
| `Ctrl+r`    | Redo                                   |
| `.`         | Repeat last change                     |

### 🔍 Search & Replace

| Command                       | Description                         |
|------------------------------|-------------------------------------|
| `/word`                      | Search forward for "word"           |
| `?word`                      | Search backward for "word"          |
| `n` / `N`                    | Next / previous search result       |
| `:%s/old/new/g`              | Replace all in file                 |
| `:s/old/new/g`               | Replace in current line             |

---

## 📁 File Commands

| Command     | Description                             |
|-------------|-----------------------------------------|
| `:w`        | Save                                     |
| `:q`        | Quit                                     |
| `:wq`       | Save and quit                            |
| `:q!`       | Force quit without saving                |
| `:e filename` | Open another file                      |
| `:r filename` | Read file into current buffer          |

---

## 🛠️ Configuring Vim

Create or edit your config file:

```bash
vim ~/.vimrc
```

### Example `.vimrc`:

```vim
set number              " Show line numbers
syntax on               " Enable syntax highlighting
set tabstop=4           " 4-space tabs
set expandtab           " Convert tabs to spaces
set shiftwidth=4        " Indentation width
set autoindent
set clipboard=unnamedplus " Use system clipboard
```

---

## 🔌 Plugins (with Vim-Plug)

Install Vim-Plug:

```bash
curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
     https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```

Add this to `~/.vimrc`:

```vim
call plug#begin('~/.vim/plugged')
Plug 'preservim/nerdtree'
Plug 'junegunn/fzf', { 'do': { -> fzf#install() } }
call plug#end()
```

Then install plugins in Vim with:

```vim
:PlugInstall
```

---

## 🎯 Pro Tips

- Use `:set paste` before pasting to avoid auto-indent issues
- Use `:reg` to view registers
- Record macros with `q[a-z]`, stop with `q`, play with `@a`
- Jump to previous location with `` `"`

---

## 📚 More Info

- Official site: [https://www.vim.org](https://www.vim.org)  
- GitHub mirror: [https://github.com/vim/vim](https://github.com/vim/vim)  
- Learn Vim interactively: [https://www.openvim.com](https://www.openvim.com)  
- Tutorial: Launch `vimtutor` in terminal

---

## 🧩 Alternatives

- `neovim` — Modern fork with Lua scripting and better plugin support  
- `nano` — Simpler CLI text editor  
- `emacs` — More complex but very extensible
```
