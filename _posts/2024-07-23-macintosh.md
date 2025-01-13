---
layout: post
title: 💻 Tips for using Macintosh
categories: misc
---

# Mac 使用技巧

## 触控板设置

设置  >  触控板  >  光标与点按 > 轻点来点按 ✔

![image-20240725114717172](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/1553239a1b7c83f767401e2145c1357d.png)

设置 > 触控板 > 更多手势

> 轻扫切换全屏幕显示的应用程序 修改为 四指左右轻扫
>
> 调度中心 修改为 四指向上轻扫
>
> App Exposé 修改为 四指向下轻扫

![image-20240725114702801](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/8d21e21d761fb5ba0f9c944a1c62ed87.png)

设置 > 辅助功能 > 指针控制 > 触控板选项

> 使用触控板进行拖移 ✔
>
> 拖移样式 选择 三指拖移

![image-20240725114755753](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/bdf4b7f9094ebe2c679a23ee96416571.png)

## 基础设置

### 截屏快捷键

设置 > 键盘 > 键盘快捷键 > 截屏

> 将所选区域的图片拷贝到剪切板修改为 ⇧⌘S

![image-20240724165228439](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/44ab2444fc6387b5e78721fb33ddc76b.png)

### 允许任何来源

> 设置 > 隐私与安全性 > 安全性 选中 任何来源

![image-20240725114619572](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/1f9fc71730091a9e6f0ee3c155ddcf68.png)

### 未验证的软件

> 开发者未向 Apple 注册的 App，将看到一个警告对话框。

![image-20240724165016866](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/c0229efeb4bf95602ade17b403b05a6e.png)

## Finder

### 通用

访达设置 > 通用 > 开启“访达”窗口时打开：> 选择自定义文件夹（我习惯设置成 Downloads）

### 边栏

访达设置 > 边栏 > 勾选自定义的路径

### 高级

访达设置 > 高级 > 执行搜索时 > 选择“搜索当前文件夹”

访达设置 > 高级 > 显示所有文件扩展名 ✔

### 路径栏

点击状态栏上访达的显示菜单

![image-20240725112524966](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/d6a93f29db34665c319d9cae7a845bed.png)

### 工具栏

![image-20240724165112466](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/9a085d897129a79b3c95d007b9b9ffb7.png)

## 开发环境

### Xcode Command Line Tools

你有三种选择在 Mac 上安装 Xcode 命令行工具：

- 安装完整的 Xcode 包
- 当被一个命令触发时安装 Xcode 命令行工具
- 安装 Xcode 命令行工具作为 Homebrew 安装的一部分

![image-20240725114958019](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/4386bcdbc7f95ecd160d4e2d73356307.png)

#### 安装

```bash
xcode-select --install
```

![image-20240725133822386](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/fc9fec7e62b1ade0aad3b7e9b3df7f5a.png)

### Homebrew

> **The Missing Package Manager for macOS (or Linux)**

#### 安装

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

#### 配置

![image-20240725142003252](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/070edd1375fc68a94926320534162903.png)

[清华镜像源使用帮助](https://mirrors.tuna.tsinghua.edu.cn/help/homebrew/){:target="_blank"}

[中科大镜像源使用帮助](https://mirrors.ustc.edu.cn/help/brew.git.html){:target="_blank"}

#### 常用命令

  - `brew doctor` # 检查 Homebrew 安装是否有问题，并提供修复建议
  - `brew search` # 搜索可用的 Homebrew 软件包
  - `brew list` # 列出已安装的 Homebrew 软件包
  - `brew install <package>` # 安装指定的软件包
  - `brew uninstall <package>` # 卸载指定的软件包
  - `brew update` # 更新 Homebrew 及其软件包列表
  - `brew upgrade` # 升级已安装的 Homebrew 软件包

### iTerm2

#### 安装

```bash
brew install iterm2
```

#### 主题配置

iTerm2 > Settings > Profile > Colors > Color Presets > Import

> 官方提供了主题 [Gallery](https://iterm2colorschemes.com/){:target="_blank"}，这里推荐 [Dracula](https://raw.githubusercontent.com/mbadolato/iTerm2-Color-Schemes/master/schemes/Dracula.itermcolors){:target="_blank"}主题

![image-20240725140600490](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/3004a6fba638054ded00c2aa5e8d39f2.png)

**Dracula Theme**

> 🧛🏻‍♂️ One [theme](https://github.com/dracula/dracula-theme){:target="_blank"}. All platforms. 

![Dracula](https://draculatheme.com/images/dracula.gif)

#### 字体配置

iTerm2 默认字体即为 Monaco，但是缺少一些图形的渲染，这里推荐使用 nerd patcher 版本的 [Monaco Nerd Font Mono](https://github.com/Alphasxd/monaco-nerd-fonts){:target="_blank"}

![image-20240725141340634](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/64d2147292631870d915272f042d55be.png)

#### 主题设置

iTerm2 > Settings > Appearance > General > Theme > Minimal ✔

![image-20240725141705690](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/575fa0ec70a30fc5a9532b48a74c9c22.png)

#### 状态栏配置

iTerm2 > Settings > Profile > Session > Status bar enabled ✔ > Configure Status Bar

![image-20240725141435572](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/a3c0160848c94e3f6bf93d290ff7a3fe.png)

### Bottom

> A customizable cross-platform graphical process/system monitor for the terminal. Supports Linux, macOS, and Windows.

#### 安装

```bash
brew install bottom
```

![image-20240725111756142](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/a75581918ef2049025f857fdb8957ea8.png)

### Tmux

> SSH 登录远程计算机，打开一个远程窗口执行命令。这时，网络突然断线，再次登录的时候，是找不回上一次执行的命令的。因为上一次 SSH 会话已经终止了，里面的进程也随之消失了。
>
> 为了解决这个问题，会话与窗口可以"解绑"：窗口关闭时，会话并不终止，而是继续运行，等到以后需要的时候，再让会话"绑定"其他窗口。
>
> **Tmux 就是会话与窗口的"解绑"工具，将它们彻底分离。**

#### 安装

```bash
brew install tmux
```

#### 常用命令

- `tmux new -s <session-name>` # 新建会话
- `tmux detach` # 分离会话（快捷键：`Ctrl + b` 然后 `d`）
- `tmux ls` # 查看会话
- `tmux attach -t <session-id>` # 接入会话
- `tmux kill-session -t <session-id>` # 终止指定会话
- `tmux rename-session -t <old-session-name> <new-session-name>` # 重命名会话
- `tmux split-window -h` # 水平分割窗口（快捷键：`Ctrl + b` 然后 `%`）
- `tmux split-window -v` # 垂直分割窗口（快捷键：`Ctrl + b` 然后 `"`）
- `tmux kill-pane -t <pane-id>` # 关闭指定窗格（快捷键：`Ctrl + b` 然后 `x`）
- `tmux kill-window -t <window-id>` # 关闭指定窗口（快捷键：`Ctrl + b` 然后 `&`）

### oh-my-zsh

#### 安装

  - curl

  ```bash
  sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
  ```

  - wget

  ```bash
  sh -c "$(wget -O- https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`
  ```

#### 主题

配置为 ys 主题

![image-20240725142740782](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/a360b6b441524ef2d3ae04322355db0a.png)

#### 插件

> 在 ~/.oh-my-zsh/custom/plugins下，git clone 自定义的插件即可

推荐安装以下插件：

  - [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions){:target="_blank"}
  - [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting){:target="_blank"}

![image-20240725142809946](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/d05a7fff96a1791ac5e3e0d676c376b2.png)

### NeoVim

> hyperextensible Vim-based text editor

#### 安装

  ```bash
  brew install neovim
  ```

#### 配置方案

有很多开箱即用的配置方案，譬如 AstroVim、LunarVim，选个顺眼的就行

![截屏2024-07-25 10.57.26](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/44d583b5804de28afec5c6ca1eef4b9f.png)

#### 类似IDE的界面效果

![image-20240725110559890](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/5caaf08961a5f2068c057b0cd2d8ed5c.png)

### fastfetch

#### 安装

```bash
brew install fastfetch
```

![image-20240725115535178](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/8e2cfffc55174484bc320ad805382437.png)

### OrbStack

**Say goodbye to slow, clunky containers and VMs**

> **OrbStack is the fast, light, and easy way to run Docker containers and Linux. Develop at lightspeed with our Docker Desktop alternative.**

墙裂推荐，Mac 终于可以彻底抛弃 Docker Desktop 了，Docker 和 VM 两手抓，主打一个全都要 🤣

![image-20240725143344788](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/b68a020e762a6cd08193c81384bfe21d.png)

Docker 环境

![image-20240725143218399](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/e59968ca4a60ab6a161ddea886e1000f.png)

VM 使用效果（VSCode 也可以无痛连接）

![image-20240725143303687](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/3b52a96cd097966f17c170ba1652f66c.png)

## 实用工具

### Maccy

Clipboard manager for macOS which does one job - keep your copy history at hand. Period.

Lightweight. Open source. No fluff.

![image-20240725175050089](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/36a07be24bf97bb70a686fffa4a5720b.png)

### MonitorControl

🖥 Control your display's brightness & volume on your Mac as if it was a native Apple Display. Use Apple Keyboard keys or custom shortcuts. Shows the native macOS OSDs.

![image-20240725115641404](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/0604ec5ccd27f4591cd5b6cf78c74681.png)

### Downie

一款简单好用的视频下载工具

![image-20240725125528032](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/7ff772b4fba3455132b21966c3a2c90d.png)

### IINA

基于[mpv](https://mpv.io/){:target="_blank"}的自由及开源媒体播放器

![sc-sky](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/bc57cb525c17c749a780de178453c02c.png)

### RIME

聪明的输入法懂我心意

  > 强烈推荐阅读我的另一篇文章[中州韵输入法配置指北](https://alphasxd.pages.dev/misc/2024/02/18/rime){:target="_blank"}

![image-20240725125242124](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/7d28ee67b7001bd6625e7152dc0dfddc.png)

## 其他(摸鱼利器)

### PixelPerfect

>**Increase the text size of iPhone and iPad apps on Mac. Say goodbye to small and blurry text, and enjoy pixel-perfect graphics, all rendered at 100% native resolution. Compatible with macOS Sonoma, macOS Ventura, macOS Monterey, and macOS Big Sur.**

### PlayCover

> **Run iOS apps and games natively on your Apple Silicon Mac.**

## 参考

- [Mac开光指南](https://shockerli.net/post/mac-initialize/){:target="_blank"}
- [Tmux 使用教程](https://www.ruanyifeng.com/blog/2019/10/tmux.html){:target="_blank"}