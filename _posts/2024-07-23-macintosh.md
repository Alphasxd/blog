---
layout: post
title: 💻 Tips for using Macintosh
categories: misc
---

# Mac 使用技巧

## 触控板设置

设置  >  触控板  >  光标与点按 > 轻点来点按 ✔

![image-20240725114717172](https://jihulab.com/Alphasxd/pic/raw/main/2024/11/202411051852602.png)

设置 > 触控板 > 更多手势

> 轻扫切换全屏幕显示的应用程序 修改为 四指左右轻扫
>
> 调度中心 修改为 四指向上轻扫
>
> App Exposé 修改为 四指向下轻扫

![image-20240725114702801](https://jihulab.com/Alphasxd/pic/raw/main/2024/11/202411051852603.png)

设置 > 辅助功能 > 指针控制 > 触控板选项

> 使用触控板进行拖移 ✔
>
> 拖移样式 选择 三指拖移

![image-20240725114755753](https://jihulab.com/Alphasxd/pic/raw/main/2024/11/202411051852604.png)

## 基础设置

### 截屏快捷键

设置 > 键盘 > 键盘快捷键 > 截屏

> 将所选区域的图片拷贝到剪切板修改为 ⇧⌘S

![image-20240724165228439](https://jihulab.com/Alphasxd/pic/raw/main/2024/11/202411051852605.png)

### 允许任何来源

> 设置 > 隐私与安全性 > 安全性 选中 任何来源

![image-20240725114619572](https://jihulab.com/Alphasxd/pic/raw/main/2024/11/202411051852606.png)

### 未验证的软件

> 开发者未向 Apple 注册的 App，将看到一个警告对话框。

![image-20240724165016866](https://jihulab.com/Alphasxd/pic/raw/main/2024/11/202411051852607.png)

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

![image-20240725112524966](https://jihulab.com/Alphasxd/pic/raw/main/2024/11/202411051852608.png)

### 工具栏

![image-20240724165112466](https://jihulab.com/Alphasxd/pic/raw/main/2024/11/202411051852609.png)

## 开发环境

### Xcode Command Line Tools

你有三种选择在 Mac 上安装 Xcode 命令行工具：

- 安装完整的 Xcode 包
- 当被一个命令触发时安装 Xcode 命令行工具
- 安装 Xcode 命令行工具作为 Homebrew 安装的一部分

![image-20240725114958019](https://jihulab.com/Alphasxd/pic/raw/main/2024/11/202411051852610.png)

#### 安装

```bash
xcode-select --install
```

![image-20240725133822386](https://jihulab.com/Alphasxd/pic/raw/main/2024/11/202411051852611.png)

### Homebrew

> **The Missing Package Manager for macOS (or Linux)**

#### 安装

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

#### 配置

![image-20240725142003252](https://jihulab.com/Alphasxd/pic/raw/main/2024/11/202411051852612.png)

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

![image-20240725140600490](https://jihulab.com/Alphasxd/pic/raw/main/2024/11/202411051852613.png)

**Dracula Theme**

> 🧛🏻‍♂️ One [theme](https://github.com/dracula/dracula-theme){:target="_blank"}. All platforms. 

![Dracula](https://draculatheme.com/images/dracula.gif)

#### 字体配置

iTerm2 默认字体即为 Monaco，但是缺少一些图形的渲染，这里推荐使用 nerd patcher 版本的 [Monaco Nerd Font Mono](https://github.com/Alphasxd/monaco-nerd-fonts){:target="_blank"}

![image-20240725141340634](https://jihulab.com/Alphasxd/pic/raw/main/2024/11/202411051852614.png)

#### 主题设置

iTerm2 > Settings > Appearance > General > Theme > Minimal ✔

![image-20240725141705690](https://jihulab.com/Alphasxd/pic/raw/main/2024/11/202411051852615.png)

#### 状态栏配置

iTerm2 > Settings > Profile > Session > Status bar enabled ✔ > Configure Status Bar

![image-20240725141435572](https://jihulab.com/Alphasxd/pic/raw/main/2024/11/202411051852616.png)

### Bottom

> A customizable cross-platform graphical process/system monitor for the terminal. Supports Linux, macOS, and Windows.

#### 安装

```bash
brew install bottom
```

![image-20240725111756142](https://jihulab.com/Alphasxd/pic/raw/main/2024/11/202411051852617.png)

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

![image-20240725142740782](https://jihulab.com/Alphasxd/pic/raw/main/2024/11/202411051852618.png)

#### 插件

> 在 ~/.oh-my-zsh/custom/plugins下，git clone 自定义的插件即可

推荐安装以下插件：

  - [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions){:target="_blank"}
  - [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting){:target="_blank"}

![image-20240725142809946](https://jihulab.com/Alphasxd/pic/raw/main/2024/11/202411051852619.png)

### NeoVim

> hyperextensible Vim-based text editor

#### 安装

  ```bash
  brew install neovim
  ```

#### 配置方案

有很多开箱即用的配置方案，譬如 AstroVim、LunarVim，选个顺眼的就行

![截屏2024-07-25 10.57.26](https://jihulab.com/Alphasxd/pic/raw/main/2024/11/202411051852620.png)

#### 类似IDE的界面效果

![image-20240725110559890](https://jihulab.com/Alphasxd/pic/raw/main/2024/11/202411051852621.png)

### fastfetch

#### 安装

```bash
brew install fastfetch
```

![image-20240725115535178](https://jihulab.com/Alphasxd/pic/raw/main/2024/11/202411051852622.png)

### OrbStack

**Say goodbye to slow, clunky containers and VMs**

> **OrbStack is the fast, light, and easy way to run Docker containers and Linux. Develop at lightspeed with our Docker Desktop alternative.**

墙裂推荐，Mac 终于可以彻底抛弃 Docker Desktop 了，Docker 和 VM 两手抓，主打一个全都要 🤣

![image-20240725143344788](https://jihulab.com/Alphasxd/pic/raw/main/2024/11/202411051852623.png)

Docker 环境

![image-20240725143218399](https://jihulab.com/Alphasxd/pic/raw/main/2024/11/202411051852624.png)

VM 使用效果（VSCode 也可以无痛连接）

![image-20240725143303687](https://jihulab.com/Alphasxd/pic/raw/main/2024/11/202411051852625.png)

## 实用工具

### Maccy

Clipboard manager for macOS which does one job - keep your copy history at hand. Period.

Lightweight. Open source. No fluff.

![image-20240725175050089](https://jihulab.com/Alphasxd/pic/raw/main/2024/11/202411051852626.png)

### MonitorControl

🖥 Control your display's brightness & volume on your Mac as if it was a native Apple Display. Use Apple Keyboard keys or custom shortcuts. Shows the native macOS OSDs.

![image-20240725115641404](https://jihulab.com/Alphasxd/pic/raw/main/2024/11/202411051852627.png)

### Downie

一款简单好用的视频下载工具

![image-20240725125528032](https://jihulab.com/Alphasxd/pic/raw/main/2024/11/202411051852628.png)

### IINA

基于[mpv](https://mpv.io/){:target="_blank"}的自由及开源媒体播放器

![sc-sky](https://jihulab.com/Alphasxd/pic/raw/main/2024/11/202411051852629.png)

### RIME

聪明的输入法懂我心意

  > 强烈推荐阅读我的另一篇文章[中州韵输入法配置指北](https://alphasxd.pages.dev/misc/2024/02/18/rime){:target="_blank"}

![image-20240725125242124](https://jihulab.com/Alphasxd/pic/raw/main/2024/11/202411051852630.png)

## 其他(摸鱼利器)

### PixelPerfect

>**Increase the text size of iPhone and iPad apps on Mac. Say goodbye to small and blurry text, and enjoy pixel-perfect graphics, all rendered at 100% native resolution. Compatible with macOS Sonoma, macOS Ventura, macOS Monterey, and macOS Big Sur.**

### PlayCover

> **Run iOS apps and games natively on your Apple Silicon Mac.**

## 参考

- [Mac开光指南](https://shockerli.net/post/mac-initialize/){:target="_blank"}
- [Tmux 使用教程](https://www.ruanyifeng.com/blog/2019/10/tmux.html){:target="_blank"}