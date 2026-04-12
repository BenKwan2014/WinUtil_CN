# WinUtil_CN | WinUtil 中文汉化版 | Chris Titus Tech WinUtil 中文版

WinUtil_CN 是 **Chris Titus Tech WinUtil** 的**中文汉化版 / 中文注释版 / 中文说明版**。这个仓库面向中文用户，提供 **WinUtil 中文界面、WinUtil 中文说明、WinUtil Tweaks 中文解释、Win11ISO 中文说明**，方便理解每个优化项、系统修复项、更新策略项和镜像制作项的实际作用。

This repository is a **Chinese localization of Chris Titus Tech WinUtil**. It keeps the upstream WinUtil logic intact as much as possible, while translating user-facing text and adding Chinese explanations for Windows tweaks, repair options, update policies, and Win11ISO workflow.

当前同步版本：**WinUtil Release 26.04.02**  
当前中文维护日期：**2026-04-12**

<img width="2000" height="1583" alt="WinUtil_CN 中文界面截图 1" src="https://github.com/user-attachments/assets/fa871cb1-4d96-4f2e-9a9d-99730a720812" />
<img width="2018" height="1285" alt="WinUtil_CN 中文界面截图 2" src="https://github.com/user-attachments/assets/e30b0920-273c-4af9-b445-c674adf85c45" />
<img width="2018" height="1285" alt="WinUtil_CN 中文界面截图 3" src="https://github.com/user-attachments/assets/ffd4a92c-d0c2-4cb0-a29f-b18e3493020e" />
<img width="2018" height="1285" alt="WinUtil_CN 中文界面截图 4" src="https://github.com/user-attachments/assets/95d505ab-1113-4593-8dc3-191ec53ca0b0" />

## WinUtil_CN 是什么

- `WinUtil_CN` 是 `WinUtil` 的中文维护分支，不是官方版本。
- 上游项目是 `Chris Titus Tech / WinUtil`。
- 这个仓库主要做两件事：保留上游功能逻辑，补充中文 UI 和中文解释。
- 适合搜索这些关键词的用户：`WinUtil_CN`、`WinUtil 中文`、`WinUtil 汉化`、`Chris Titus Tech WinUtil 中文版`、`WinUtil Tweaks 中文说明`。

## 仓库定位

- 尽量不改动功能逻辑，不修改注册表路径、命令、参数、内部键名与逻辑分支。
- 主要修改用户可见文本，包括按钮、标签、说明、提示、部分弹窗、配置层文案。
- 优先在配置层维护翻译，减少后续跟上游同步时的合并冲突。

> 免责声明：
> - 本项目为个人维护的**非官方 WinUtil 中文汉化版**，与上游无隶属关系。
> - 我尽量只翻译与解释用户可见文本，但 WinUtil 涉及系统优化、注册表、服务、更新策略等操作，使用前请先备份。
> - 如你更信任原作者版本，请以上游官方仓库为准。

## 使用方法

### 1. 直接运行

管理员 PowerShell 执行：

```powershell
irm "https://raw.githubusercontent.com/constansino/WinUtil_CN/refs/heads/main/winutil.zh_CN.commented.20260412.ps1" | iex
```

### 2. 下载到本地后运行

```powershell
Unblock-File -Path "你的目录\winutil.zh_CN.commented.20260412.ps1"
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass -Force
.\winutil.zh_CN.commented.20260412.ps1
```

说明：
- `Unblock-File` 用于移除下载脚本的 Mark of the Web，避免 PowerShell 执行限制或闪退。
- 更推荐本地运行方式，因为更容易审计脚本内容。

## 汉化内容

### 1. 顶部导航和常用按钮

- `Install / Tweaks / Config / Updates / Win11ISO` 已补充中文标签和常用提示。

### 2. Tweaks 页面重点汉化

- Tweaks 项目标题中文化。
- Tweaks 项目说明中文化。
- 对很多项目补了更适合中文用户理解的说明，帮助判断“这个开关到底改了什么、有什么风险”。

### 3. 其他页面

- `Install / Config / Updates / Win11ISO` 已补充常用区域的中文说明。
- 软件名称如 `7-Zip`、`VS Code`、`PowerShell 7` 通常保留原产品名，避免对照困难。

## 上游同步策略

为了尽量降低与上游 `WinUtil` 合并冲突，本仓库遵循以下做法：

1. 不改功能逻辑，只改用户可见文本。
2. 优先维护配置层字段，例如 `Title / Description / Content / category`。
3. 上游更新后，先同步官方脚本，再迁移中文字段，最后补新版新增项的翻译。
4. 同时保留完整 patch，方便后续复用和审查。

## 文件说明

- `winutil.zh_CN.commented.20260412.ps1`：当前中文注释 + 中文界面维护版本
- `winutil.zh_CN.full.patch.20260412.diff`：基于上游 `26.04.02` 生成的完整 patch

## 上游项目

- 上游仓库：[ChrisTitusTech/winutil](https://github.com/ChrisTitusTech/winutil)
- 上游发布页：[WinUtil Releases](https://github.com/ChrisTitusTech/winutil/releases)
- 当前同步上游版本：[26.04.02](https://github.com/ChrisTitusTech/winutil/releases/tag/26.04.02)

## 贡献方式

- 提交 PR，补充新条目的中文翻译或更准确的中文说明。
- 提交 issue，指出某个 Tweaks/Feature/Win11ISO 项目的翻译不准确或解释不清楚。
- 如果上游更新了新版本，也欢迎提交同步 PR。

再次感谢上游开发者与社区贡献者。
