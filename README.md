# Hermes Desktop for Windows

Hermes 桌面版的 Windows 分发（本仓库为构建产物分发页；基于上游 Hermes Agent 项目的本地增强构建）。

## 下载安装

1. 打开本仓库的 [Releases](../../releases/latest)，下载 `Hermes-Desktop-Setup-20260928-r2.exe`（约 121 MB）。
2. 双击运行安装（按当前用户安装，无需管理员权限）。
3. 首次运行如出现「Windows 已保护你的电脑」（SmartScreen）提示：点 **更多信息 → 仍要运行**。安装包为未签名构建，这是正常提示。
4. 安装完成后，从开始菜单或桌面打开 **Hermes**，按界面提示连接后端服务（地址由服务提供方给你）。

## 系统要求

- Windows 10 / 11（x64）

## 更新

下载新版安装包，直接安装覆盖即可；配置不受影响。

## 卸载

打开「设置 → 应用 → Hermes → 卸载」，或使用开始菜单中的卸载入口。

## 校验

Release 里附带 `SHA256SUMS.txt`。下载后可在 PowerShell 里校验：

```powershell
Get-FileHash .\Hermes-Desktop-Setup-20260928-r2.exe -Algorithm SHA256
```

## 说明

- 本仓库是 Hermes 桌面版的 Windows 分发构建（基于 [上游 Hermes Agent 项目](https://github.com/NousResearch/hermes-agent)，MIT License，含本地增强）。
- 需要在本机运行时（不使用远端后端）时，安装包首次启动会从配套源码仓 `ss12113/hermes-agent-win` 安装运行时，无需手工配置。
- 本仓库与安装包不含任何密钥或个人信息；连接配置由使用者在本机完成。
- 这是未签名的内部分发构建，不提供自动更新通道；新版本会以新的 Release 发布。

---

## English

Download `Hermes-Desktop-Setup-20260928-r2.exe` from [Releases](../../releases/latest) and run it.
Windows 10 / 11 (x64). Unsigned build — if SmartScreen shows up, choose "More info → Run anyway".
On first launch the app installs its local runtime from the companion source repo `ss12113/hermes-agent-win`; connecting to a remote backend needs no local runtime.
