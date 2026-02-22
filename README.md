⸻

📦 tmux Configuration

Tokyo Night inspired tmux setup optimized for:
	•	macOS
	•	WezTerm
	•	Nerd Font
	•	SSH-heavy workflow
	•	Nix / multi-machine environment

⸻

✨ Features
	•	Ctrl+a as prefix
	•	Mouse support enabled
	•	256-color terminal support
	•	Top status bar
	•	Strong active pane highlight
	•	Dim inactive panes
	•	Modern window labels
	•	Vim-style pane navigation
	•	Session persistence via TPM plugins

⸻

🎨 Visual Design

Designed for Tokyo Night × WezTerm.
	•	Status bar at top
	•	Active pane with high-contrast border
	•	Inactive panes slightly dimmed
	•	Clean block-style window labels
	•	User + host display (SSH-friendly)

⸻

📁 File Structure

~/.config/tmux/tmux.conf
~/.tmux.conf   # minimal bridge file
~/.tmux/plugins/tpm

Bridge file (~/.tmux.conf):

source-file "$HOME/.config/tmux/tmux.conf"


⸻

🔧 Installation

1️⃣ Install TPM

git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
chmod +x ~/.tmux/plugins/tpm/tpm

2️⃣ Restart tmux

tmux kill-server
tmux

3️⃣ Install plugins

Inside tmux:

Ctrl+a I


⸻

⌨️ Keybindings

Prefix

Ctrl+a


⸻

Splits

Action	Key
Vertical split	`Ctrl+a
Horizontal split	Ctrl+a -
Compatible default	Ctrl+a % / Ctrl+a "


⸻

Pane Navigation (no prefix)

Ctrl+h
Ctrl+j
Ctrl+k
Ctrl+l


⸻

Reload Config

Ctrl+a r


⸻

Save / Restore Session

Action	Key
Save session	Ctrl+a Ctrl+s
Restore	Ctrl+a Ctrl+r


⸻

🧠 Workflow Philosophy

One machine = one session.

Example:

tank
m16
gpd

Each session layout:

Window	Purpose
1	nvim
2	build
3	logs
4	system

Never close tmux.
Detach instead.

Ctrl+a d


⸻

🖥 Recommended Terminal

Tested with:
	•	WezTerm
	•	Nerd Font enabled
	•	Tokyo Night theme

Suggested WezTerm settings:

window_background_opacity = 0.92
macos_window_background_blur = 20
window_padding = {
  left = 12,
  right = 12,
  top = 8,
  bottom = 8,
}


⸻

📌 Notes
	•	Plugins are runtime dependencies, not version-controlled.
	•	plugins/ directory should not be committed.
	•	Designed for multi-machine consistency.
	•	Compatible with Home Manager / Nix.

⸻

🚀 Future Improvements
	•	Optional git branch in status bar
	•	Battery indicator (macOS)
	•	CPU load indicator
	•	SSH host color auto-detection
	•	Floating pane support

⸻

If you use Nix, consider generating the config declaratively.

⸻
