---
layout: post
title: 💻 Tips for using Macintosh
categories: misc
---

# Mac 新手使用与配置清单

这篇文章主要写给刚开始接触 Mac 的用户，也保留了我自己长期在用的一些进阶配置和开发环境工具。为了避免把“可选折腾”误认为“新手必做”，全文按下面三类来组织：

- `新手必做`：日常使用中最容易提升体验的设置，建议优先看。
- `按需优化`：不是每个人都需要，但在特定场景下很好用。
- `高风险操作`：会涉及系统安全策略或系统文件修改，只建议有明确需求时再做。
- `开发者进阶`：偏程序员工作流，不是普通用户的必装项。

如果你刚拿到一台 Mac，只看前半部分就够用了；后面的内容可以等用顺手以后再按需补上。

## 拿到 Mac 后建议先做的 5 件事

如果你不想一次性改太多设置，先做下面 5 件事，体验提升最明显：

1. 开启轻点来点按和三指拖移，触控板会顺手很多。
2. 调整截图快捷键，方便快速截取局部内容并直接贴到聊天工具里。
3. 在 Finder 中开启“显示所有文件扩展名”和“搜索当前文件夹”。
4. 先整理输入法顺序，避免中英文切换混乱。
5. 装一个常用工具，比如 `Maccy`、`IINA`、`MonitorControl`。

## 哪些内容可以跳过

下面这些内容都不是 Mac 新手必做项，如果你没有对应需求，可以直接跳过：

- `允许任何来源`：只在你明确知道自己要安装什么软件时才考虑。
- `关闭 SIP 删除 ABC 输入法`：这是系统级修改，不建议普通用户上来就做。
- `tmux`、`neovim`、`oh-my-zsh`：明显偏程序员工作流。
- `OrbStack`：主要给需要 Docker 或 Linux 虚拟机的开发者准备。
- `PlayCover`、`PixelPerfect`：属于特定娱乐或兼容性场景。

## 新手必做

### 触控板设置

Mac 的触控板体验很好，但默认设置不一定适合新手，稍微调整一下会顺手很多。

#### 轻点来点按

开启后不需要把触控板按下去，轻触一下就能点击，长时间使用会轻松很多。

设置 > 触控板 > 光标与点按 > 轻点来点按 ✔

![image-20240725114717172](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/1553239a1b7c83f767401e2145c1357d.png)

#### 多指手势

这组手势是我自己最常用的组合，适合经常在多个应用和桌面之间切换的人。

设置 > 触控板 > 更多手势

> 轻扫切换全屏幕显示的应用程序 修改为 四指左右轻扫
>
> 调度中心 修改为 四指向上轻扫
>
> App Exposé 修改为 四指向下轻扫

![image-20240725114702801](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/8d21e21d761fb5ba0f9c944a1c62ed87.png)

#### 三指拖移

这个设置对新手特别友好，拖窗口、拖文件、选中文本都会更省力。

设置 > 辅助功能 > 指针控制 > 触控板选项

> 使用触控板进行拖移 ✔
>
> 拖移样式 选择 三指拖移

![image-20240725114755753](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/bdf4b7f9094ebe2c679a23ee96416571.png)

### 截图快捷键

如果你经常要把截图发到微信、飞书或其他聊天工具，建议把“截取选区并复制到剪贴板”的快捷键改短一点。

设置 > 键盘 > 键盘快捷键 > 截屏

> 将所选区域的图片拷贝到剪切板修改为 ⇧⌘S

这样截图后就能直接粘贴，不用先保存成文件再发送。

![image-20240724165228439](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/44ab2444fc6387b5e78721fb33ddc76b.png)

### Finder

Finder 是你每天都会用到的文件管理器，下面几个设置都属于高频、低风险、非常值得改。

#### 通用

设置默认打开的文件夹，可以减少每次打开 Finder 还要重新跳路径的次数。

访达设置 > 通用 > 开启“访达”窗口时打开：选择自定义文件夹

我个人习惯设置成 `Downloads`。

#### 边栏

把常用目录固定到边栏，后面找文件会快很多。

访达设置 > 边栏 > 勾选自定义的路径

#### 高级

这两项都非常推荐开启：

- 访达设置 > 高级 > 执行搜索时 > 选择“搜索当前文件夹”
- 访达设置 > 高级 > 显示所有文件扩展名 ✔

前者可以避免搜索范围过大，后者则能帮你识别文件类型，减少误改后缀名的情况。

#### 路径栏

开启路径栏后，你会更容易看清当前文件到底在哪个目录里。

点击状态栏上访达的显示菜单

![image-20240725112524966](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/d6a93f29db34665c319d9cae7a845bed.png)

#### 工具栏

工具栏建议把自己高频操作的按钮固定上去，尤其是列表/分栏视图切换和排序相关功能。

![image-20240724165112466](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/9a085d897129a79b3c95d007b9b9ffb7.png)

### 输入法设置

对大多数中文用户来说，输入法体验会直接决定这台 Mac 用起来是否顺手。我的建议顺序是：

1. 先整理输入法顺序与默认项。
2. 如果你对系统输入法不满意，再考虑换成 `Rime`。
3. 只有长期被 `ABC` 自动切换困扰时，才考虑后面的系统级方案。

#### Rime

如果你已经对输入法有更高要求，比如词库、同步、候选风格和自定义方案，`Rime` 很值得折腾。

聪明的输入法懂我心意。

强烈推荐阅读我的另一篇文章：[中州韵输入法配置指北](https://alphasxd.pages.dev/misc/2024/02/18/rime){:target="_blank"}

![image-20240725125242124](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/7d28ee67b7001bd6625e7152dc0dfddc.png)

## 实用工具

这一节分成两类：一类是大多数用户都能感受到提升的通用工具，另一类是特定需求才需要的工具。

### 通用推荐

#### Maccy

`Maccy` 是剪贴板历史管理工具，适合经常复制链接、代码、文本的人。它只做一件事，就是把你最近复制过的内容保存下来，随时能找回。

![image-20240725175050089](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/36a07be24bf97bb70a686fffa4a5720b.png)

#### MonitorControl

如果你经常外接显示器，这个工具很实用。它可以让你像调节苹果原生显示器一样，直接用键盘调亮度和音量。

![image-20240725115641404](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/0604ec5ccd27f4591cd5b6cf78c74681.png)

#### IINA

`IINA` 是基于 [mpv](https://mpv.io/){:target="_blank"} 的开源播放器，适合本地视频播放，界面比传统播放器更符合 macOS 的使用习惯。

![sc-sky](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/bc57cb525c17c749a780de178453c02c.png)

### 特定需求推荐

#### Downie

这是一款简单好用的视频下载工具，只有在你确实有离线保存视频的需求时再装即可。使用时注意遵守平台规则和版权要求。

![image-20240725125528032](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/7ff772b4fba3455132b21966c3a2c90d.png)

## 按需优化与高风险操作

这一节内容全部不是新手必做项。你应该先把前面的基础体验用顺了，再决定要不要继续折腾。

### 允许任何来源

**风险提示：不推荐长期打开。**

这个选项只适合在你明确知道应用来源可信、而且普通方式无法打开时使用。对大多数用户来说，更安全的顺序应该是：

1. 先尝试右键应用图标，选择“打开”。
2. 如果系统拦截，再到 `设置 > 隐私与安全性` 里找“仍要打开”。
3. 只有前两种方式都不满足需求时，再考虑临时开启“任何来源”。

首先在终端中执行以下命令：

```bash
sudo spctl --master-disable
```

然后在系统设置中找到“任何来源”选项：

> 设置 > 隐私与安全性 > 安全性 选中 任何来源

用完后建议恢复更安全的默认策略，不要把它当成日常常驻设置。

![image-20240725114619572](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/1f9fc71730091a9e6f0ee3c155ddcf68.png)

### 未验证的软件

开发者未向 Apple 注册的 App，通常会看到一个警告对话框。看到这个弹窗不代表软件一定有问题，但至少说明你应该先确认来源是否可靠。

![image-20240724165016866](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/c0229efeb4bf95602ade17b403b05a6e.png)

### 移除 ABC 输入法

**风险提示：这是系统级修改，不是通用推荐。**

如果你只是偶尔不喜欢 `ABC`，先尝试调整输入法顺序、切换快捷键，或者直接改用 `Rime`。只有在你长期被 `ABC` 自动变成默认输入法困扰，并且确定自己能接受系统级修改的前提下，再考虑下面这套方案。

#### 第一步：关闭 SIP

> M 系列的 Mac 需要在恢复模式下执行以下命令，然后重启

```bash
csrutil disable
```

#### 第二步：修改输入法配置文件

接着在终端中执行以下命令：

```bash
sudo open ~/Library/Preferences/com.apple.HIToolbox.plist
```

在打开的文件中，选择 `AppleEnableInputSources`，找到 `KeyboardLayout Name` 为 `ABC` 的 item，整个删除掉，然后 `⌘ + S` 保存，点击文件的显示简介，勾选“已锁定”，最后重启电脑。

![](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/05/5994689b92e24924ad149b4bdc6a4374.png)

#### 第三步：建议恢复 SIP

如果你只是为了完成这一个修改，做完后建议重新进入恢复模式并执行下面的命令，把 SIP 打开：

```bash
csrutil enable
```

这样更符合默认安全策略，也更适合作为长期使用状态。

## 开发者进阶

这一节是给程序员和重度折腾党准备的。普通用户完全可以跳过，不会影响日常使用。

### Xcode Command Line Tools

很多开发工具第一次运行时都会要求安装命令行工具，比如 `git`、编译器和一些基础系统头文件。

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

`Homebrew` 可以理解成 macOS 上最常用的软件包管理器，程序员基本绕不开；普通用户如果只装图形界面 App，也未必一定需要它。

> **The Missing Package Manager for macOS (or Linux)**  
> macOS 上最常用的包管理工具之一。

#### 安装

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

#### 配置

装完以后记得把安装脚本提示的环境变量加进 shell 配置文件，否则终端里可能找不到 `brew`。

![image-20240725142003252](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/070edd1375fc68a94926320534162903.png)

[清华镜像源使用帮助](https://mirrors.tuna.tsinghua.edu.cn/help/homebrew/){:target="_blank"}

[中科大镜像源使用帮助](https://mirrors.ustc.edu.cn/help/brew.git.html){:target="_blank"}

#### 常用命令

- `brew doctor`：检查 Homebrew 安装是否有问题，并提供修复建议
- `brew search`：搜索可用的软件包
- `brew list`：列出已安装的软件包
- `brew install <package>`：安装指定软件包
- `brew uninstall <package>`：卸载指定软件包
- `brew update`：更新 Homebrew 及软件包列表
- `brew upgrade`：升级已安装的软件包

### iTerm2

如果你经常使用终端，`iTerm2` 比系统自带终端更强，也更适合后续做主题、状态栏和字体定制。

#### 安装

```bash
brew install iterm2
```

#### 主题配置

iTerm2 > Settings > Profile > Colors > Color Presets > Import

官方提供了主题 [Gallery](https://iterm2colorschemes.com/){:target="_blank"}，这里推荐 [Dracula](https://raw.githubusercontent.com/mbadolato/iTerm2-Color-Schemes/master/schemes/Dracula.itermcolors){:target="_blank"} 主题。

![image-20240725140600490](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/3004a6fba638054ded00c2aa5e8d39f2.png)

**Dracula Theme**

> One [theme](https://github.com/dracula/dracula-theme){:target="_blank"} for many platforms，比较省心。

![Dracula](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2026/04/b7d3faefafac2edbf5425ee254d9bd21.gif)

#### 字体配置

iTerm2 默认字体是 `Monaco`，但缺少一些图标字符渲染。这里推荐使用 nerd patched 版本的 [Monaco Nerd Font Mono](https://github.com/Alphasxd/monaco-nerd-fonts){:target="_blank"}。

![image-20240725141340634](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/64d2147292631870d915272f042d55be.png)

#### 主题设置

iTerm2 > Settings > Appearance > General > Theme > Minimal ✔

![image-20240725141705690](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/575fa0ec70a30fc5a9532b48a74c9c22.png)

#### 状态栏配置

如果你希望终端里直接看到 CPU、网络、路径等信息，可以把状态栏打开。

iTerm2 > Settings > Profile > Session > Status bar enabled ✔ > Configure Status Bar

![image-20240725141435572](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/a3c0160848c94e3f6bf93d290ff7a3fe.png)

### Bottom

`Bottom` 是一个终端里的系统监控工具，适合习惯命令行查看 CPU、内存、磁盘和进程信息的人。

#### 安装

```bash
brew install bottom
```

![image-20240725111756142](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/a75581918ef2049025f857fdb8957ea8.png)

### Tmux

如果你会经常 SSH 到远程机器上工作，`tmux` 很值得学。它最大的价值是让“终端窗口”和“会话本身”分离，断网以后任务也不容易丢。

> SSH 登录远程计算机，打开一个远程窗口执行命令。这时，网络突然断线，再次登录的时候，是找不回上一次执行的命令的。因为上一次 SSH 会话已经终止了，里面的进程也随之消失了。
>
> 为了解决这个问题，会话与窗口可以“解绑”：窗口关闭时，会话并不终止，而是继续运行，等到以后需要的时候，再让会话“绑定”其他窗口。
>
> **Tmux 就是会话与窗口的“解绑”工具。**

#### 安装

```bash
brew install tmux
```

#### 常用命令

- `tmux new -s <session-name>`：新建会话
- `tmux detach`：分离会话（快捷键：`Ctrl + b` 然后 `d`）
- `tmux ls`：查看会话
- `tmux attach -t <session-id>`：接入会话
- `tmux kill-session -t <session-id>`：终止指定会话
- `tmux rename-session -t <old-session-name> <new-session-name>`：重命名会话
- `tmux split-window -h`：水平分割窗口（快捷键：`Ctrl + b` 然后 `%`）
- `tmux split-window -v`：垂直分割窗口（快捷键：`Ctrl + b` 然后 `"`）
- `tmux kill-pane -t <pane-id>`：关闭指定窗格（快捷键：`Ctrl + b` 然后 `x`）
- `tmux kill-window -t <window-id>`：关闭指定窗口（快捷键：`Ctrl + b` 然后 `&`）

### oh-my-zsh

`oh-my-zsh` 主要用来美化和增强终端 shell 体验。如果你只是偶尔打开终端，它不是必需品；如果你每天都在终端里工作，它会很省事。

#### 安装

- `curl`

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

- `wget`

```bash
sh -c "$(wget -O- https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

#### 主题

我自己配置为 `ys` 主题。

![image-20240725142740782](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/a360b6b441524ef2d3ae04322355db0a.png)

#### 插件

在 `~/.oh-my-zsh/custom/plugins` 下，`git clone` 自定义插件即可。

推荐安装以下插件：

- [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions){:target="_blank"}
- [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting){:target="_blank"}

前者负责命令补全提示，后者负责命令高亮，新手也能明显感受到终端输入更安心。

![image-20240725142809946](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/d05a7fff96a1791ac5e3e0d676c376b2.png)

### NeoVim

`NeoVim` 是一个高度可扩展的 Vim 系编辑器。它很强，但学习曲线也更陡，适合已经明确想把终端编辑器当主力工具的人。

#### 安装

```bash
brew install neovim
```

#### 配置方案

有很多开箱即用的配置方案，比如 `AstroVim`、`LunarVim`，选个顺眼的就行。

![截屏2024-07-25 10.57.26](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/44d583b5804de28afec5c6ca1eef4b9f.png)

#### 类似 IDE 的界面效果

![image-20240725110559890](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/5caaf08961a5f2068c057b0cd2d8ed5c.png)

### fastfetch

`fastfetch` 主要是展示系统信息，实用性不是最高，但很适合终端党做环境确认和展示。

#### 安装

```bash
brew install fastfetch
```

![image-20240725115535178](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/8e2cfffc55174484bc320ad805382437.png)

### OrbStack

如果你需要跑 Docker 容器或 Linux 虚拟机，`OrbStack` 是现在体验很好的选择之一。

> **Say goodbye to slow, clunky containers and VMs**  
> 如果你觉得 Docker Desktop 偏重，OrbStack 会轻快很多。

> **OrbStack is the fast, light, and easy way to run Docker containers and Linux. Develop at lightspeed with our Docker Desktop alternative.**

我自己的使用体验很好，Docker 和 VM 都能覆盖，尤其适合 Apple Silicon Mac 上的开发者。

![image-20240725143344788](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/b68a020e762a6cd08193c81384bfe21d.png)

Docker 环境：

![image-20240725143218399](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/e59968ca4a60ab6a161ddea886e1000f.png)

VM 使用效果（VSCode 也可以无痛连接）：

![image-20240725143303687](https://pub-1f7966b8d1aa419d8595fea40c064c5c.r2.dev/2025/01/3b52a96cd097966f17c170ba1652f66c.png)

## 其他（摸鱼利器）

这一节纯粹是按兴趣推荐，不属于效率工具。

### PixelPerfect

适合想把 iPhone 和 iPad App 在 Mac 上显示得更清晰的人。

> Increase the text size of iPhone and iPad apps on Mac. Say goodbye to small and blurry text, and enjoy pixel-perfect graphics, all rendered at 100% native resolution.

### PlayCover

适合 Apple Silicon Mac 上有运行 iOS App 或游戏需求的人。

> Run iOS apps and games natively on your Apple Silicon Mac.

## 参考

- [Mac开光指南](https://shockerli.net/post/mac-initialize/){:target="_blank"}
- [Tmux 使用教程](https://www.ruanyifeng.com/blog/2019/10/tmux.html){:target="_blank"}
