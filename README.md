# Unity 2022 CLI 便携分享包

Windows x64 / Unity 2022.3 LTS / 社区 unity-cli 0.18.1 / 本地适配 r1。

[下载便携 ZIP](https://github.com/0everey/unity-cli-2022-portable/releases/latest) · [安装指南](INSTALL.zh-CN.md) · [常用命令](USAGE.zh-CN.md)

基于 MIT 许可的 [akiojin/unity-cli](https://github.com/akiojin/unity-cli)，提供已验证的 Unity 2022.3 适配、Windows CLI 和可选择工程路径的安装/卸载入口。

**先阅读 [中文安装指南](INSTALL.zh-CN.md)。** 解压到固定目录后，为你自己的 Unity 工程安装一次 Editor Bridge，即可通过命令行读取和操作该工程。

```powershell
# 把两处路径替换为自己的解压目录和 Unity 工程根目录。
Set-Location 'D:\Tools\UnityCLI2022-Portable-0.18.1-r1-20261015'
powershell -NoProfile -ExecutionPolicy Bypass -File .\Install.ps1 -Project 'D:\Projects\MyGame'
# 之后用 Unity Hub 打开 MyGame，等待导入和编译完成。
powershell -NoProfile -ExecutionPolicy Bypass -File .\Unity.ps1 -Project 'D:\Projects\MyGame' status
powershell -NoProfile -ExecutionPolicy Bypass -File .\Unity.ps1 -Project 'D:\Projects\MyGame' capabilities
```

包含固定 CLI 可执行文件、完整 Editor Bridge 源码与 Roslyn 依赖、安装/卸载入口、JSON 示例、MIT 与第三方许可。首轮 Unity 依赖解析需要网络和本机 Unity 授权。无需 Node.js、npm、Codex、API Key 或额外 Python 包。

它基于 [akiojin/unity-cli](https://github.com/akiojin/unity-cli/releases/tag/v0.18.1)，是社区工具的 Unity 2022 本地适配。当前打包范围为已验证 r1；下一轮编辑器扩展仍在制作，未纳入本包。

解压包可移到别处；Bridge 安装在对方工程内，不引用分享者电脑路径。工程内 `.unity-cli-portable` 留有安装回执及 manifest 备份；卸载入口保留其他后续依赖变更。

更多命令见 [USAGE.zh-CN.md](USAGE.zh-CN.md)，验证范围见 [VERIFIED.md](VERIFIED.md)。

## 从 GitHub 获取

推荐从 Releases 下载 ZIP，解压后阅读 `INSTALL.zh-CN.md`。也可克隆本仓库后直接运行相同安装脚本：

```powershell
git clone https://github.com/0everey/unity-cli-2022-portable.git
Set-Location .\unity-cli-2022-portable
powershell -NoProfile -ExecutionPolicy Bypass -File .\Verify.ps1
powershell -NoProfile -ExecutionPolicy Bypass -File .\Install.ps1 -Project 'D:\Projects\MyGame'
```

首个公开版本为 `v0.18.1-r1`。ZIP 提供 SHA256 校验文件，仓库文件由 `FILES.sha256.json` 记录。固定的 CLI 与 Roslyn 二进制随源码提供，Unity Editor、Python 和 Unity 包依赖由使用者按指南安装。

MIT 许可见 [LICENSE](LICENSE)；随附上游许可和第三方程序集许可见 [NOTICE.md](NOTICE.md)。
