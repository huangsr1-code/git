# Git for Windows 安装目录快照

本仓库是 **Git for Windows 2.56.0** 本地安装目录（`D:\桌面\Git`）的文本配置快照，
用于记录该安装的身份、来源与配置选项。

- Git 版本：`git version 2.56.0.windows.2`
- 安装形态：Git for Windows 标准安装（MinTTY / OpenSSH / 启用了 Git Credential Manager）
- 上游项目：<https://github.com/git-for-windows/git>
- 许可证：见 [LICENSE.txt](LICENSE.txt)（GPL-2.0）

## 仓库包含什么

只包含体积小、可审查的文本与配置：

| 路径 | 说明 |
| --- | --- |
| `LICENSE.txt` | Git for Windows 许可证（GPL-2.0） |
| `ReleaseNotes.html` | 该版本的上游发行说明 |
| `etc/package-versions.txt` | 安装的全部 MSYS2/MinGW 软件包及精确版本 |
| `etc/install-options.txt` | 安装器选项（编辑器、SSH、CRLF、凭据管理器等） |
| `etc/gitconfig`、`etc/gitattributes` | 系统级 Git 配置 |
| `etc/profile`、`etc/bash.bashrc`、`etc/*.d/` | MSYS2/Bash 环境初始化 |
| `etc/nsswitch.conf`、`etc/inputrc`、`etc/vimrc`、`etc/nanorc`、`etc/tigrc`、`etc/DIR_COLORS` | 各类运行时配置 |

## 仓库不包含什么

以下内容属于二进制或本机专有数据，已被 [.gitignore](.gitignore) 排除：

- `bin/`、`cmd/`、`usr/`、`ucrt64/`、`dev/`、`tmp/`：可执行文件与共享库（约 360 MB）
- `unins000.exe`、`unins000.dat`、`unins000.msg`：卸载器及其状态数据
- `git-bash.exe`、`git-cmd.exe`：启动器
- `etc/pki/`、`etc/ssl/`、`etc/ca-certificates/`、`etc/ssh/ssh_host_*`、`etc/hosts` 等：
  证书库与主机相关配置

如需完整的 Git for Windows 发行版，请从上游
[git-for-windows/git releases](https://github.com/git-for-windows/git/releases) 获取官方安装包。
