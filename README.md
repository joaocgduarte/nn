# nn 🗒️

A minimalist Bash script to manage your **fleeting**, **literature**, and **permanent** notes—Zettelkasten style. Includes searching, Markdown previews, git sync, and more.

[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20me%20a%20coffee-☕-blue)](https://buymeacoffee.com/joaocgduarte)

---

## 🚀 Features

- Quickly create Fleeting, Literature, or Permanent notes
- Preview and search notes using `fzf` and `glow` (or your preferred tools)
- Edit notes directly from terminal
- Simple Git-based syncing
- Lightweight and dependency-minimal
- Configurable with your preferred editor/viewer

---

## 🛠️ Installation

### 1. Clone the Repository

```bash
git clone https://github.com/joaocgduarte/nn.git
cd nn
```

### 2. Make It Executable
```bash
chmod +x nn
```

### 3. Add It to Your PATH
```bash
# Move to /usr/local/bin
sudo mv nn /usr/local/bin/nn

# OR use an alias
alias nn="/full/path/to/nn"
```

## ⚙️  Configuration (Optional)
The script creates a .nnconfig file in your home, which will be used for
choosing your CLI tools like glow for markdown viewing and nvim for editing
```bash
# Default configuration for nn
NOTE_DIR="$HOME/home/notes"
EDITOR="nvim"
VIEW_NOTE_PROGRAM="glow"
FZF_PREVIEW="glow -p -w 109 -s dark {}"
```
You can edit these preferences at any time.

## 📦 Dependencies
- fzf
- glow (or your own viewer like bat, less, etc.)
- ripgrep (rg)
- git

Install with Homebrew on macOS/Linux:
```bash
brew install fzf glow ripgrep
```

Or use your system package manager.
```bash
sudo apt-get install fzf glow ripgrep
```

## 🧪 Usage

```bash
nn               # Create a fleeting note
nn -f            # Create fleeting note
nn -l            # Create literature note
nn -p            # Create permanent note
nn -o            # Open the notes directory
nn -e -p         # Edit a permanent note
nn -gn -g term   # Preview a note containing a term
nn -d -n "idea"  # Delete a note by name
nn -s            # Sync notes (git add/commit/push)
```

## ☕ Support
If you find this useful, you can [buy me a coffee](https://buymeacoffee.com/joaocgduarte)

## 📄 License
MIT — Feel free to use, modify, and share.
