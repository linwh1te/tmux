# tmux-config

Tokyo Night × WezTerm 专用 **tmux 配置**  
适合 macOS、WezTerm、Nerd Font、SSH 多主机 + 高效终端工作流

---

## 📌 特色

- `Ctrl+a` 作为 tmux 前缀
- 顶部状态栏（清晰分段）
- 强对比当前 Pane 高亮
- Dim 弱化非活动 Pane
- Vim 风格 Pane 导航
- 多 Host / 多 Session 友好
- 自动 Session 保存 & 恢复
- 优雅的窗口标签样式

---

## 📁 结构说明

~/.config/tmux/tmux.conf
~/.tmux.conf                ← bridge
~/.tmux/plugins/tpm         ← 插件管理

> `~/.tmux.conf` 只用于 bridge 加载主配置。

Bridge 文件示例：

```tmux
source-file "$HOME/.config/tmux/tmux.conf"


⸻

🛠 安装说明

1) 克隆仓库

git clone https://github.com/linwh1te/tmux.git ~/.config/tmux


⸻

2) 安装 TPM 插件管理器

rm -rf ~/.tmux/plugins/tpm
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
chmod +x ~/.tmux/plugins/tpm/tpm


⸻

3) 重启 tmux

tmux kill-server
tmux


⸻

4) 安装插件

在 tmux 里按：

Ctrl+a I


⸻

🚀 使用指南

✔ 分屏

左右分屏：

Ctrl+a |

上下分屏：

Ctrl+a -

兼容默认：

Ctrl+a %
Ctrl+a "


⸻

✔ Pane 切换（无需前缀）

Ctrl+h  ←
Ctrl+j  ↓
Ctrl+k  ↑
Ctrl+l  →


⸻

✔ 重载配置

Ctrl+a r


⸻

✔ 保存 & 恢复 Session

Ctrl+a Ctrl+s   ← 保存
Ctrl+a Ctrl+r   ← 恢复


⸻

🧠 推荐工作流

每台主机一个 Session：

Host	Session	常规窗口
tank	tank	nvim / build / logs / sys
gpd	gpd	…
m16	m16	…


⸻

📦 WezTerm 配置（建议）

在 wezterm.lua 加：

return {
  window_background_opacity = 0.92,
  macos_window_background_blur = 20,
  window_padding = {
    left = 12, right = 12,
    top = 8, bottom = 8,
  },
  window_frame = {
    corner_radius = 12,
  },
}