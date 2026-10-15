# 来源、许可和打包范围

- 上游：https://github.com/akiojin/unity-cli ，v0.18.1，MIT，许可见 LICENSE-unity-cli.txt。
- Bridge 上游 revision：7f45d7aec2a866abda88ba3768bf4057c5f23053。
- CLI 为原固定 Windows x64 二进制，SHA256：efcd697b940f78b6457829453888d9c608f19d2fcd331d0005b1ff47a7839357。
- 本地适配 r1：Input System 1.7.0 基线、全限定组件名、材质参数/失败原子性、Transform Undo、虚拟键盘、能力报告/序列化只读工具、排除测试夹具的工具发现、辅助程序集仅 Editor。
- 本分享包新增通用目标安装/卸载与启动入口，Bridge 的业务源码固定为已安装/验证的 r1 记录；正在开发的 r2 扩展未纳入。
- Roslyn 和相关 Microsoft 程序集许可随包位于 package/com.akiojin.unity-cli-bridge/Editor/ThirdParty/Roslyn。
- 没有随附分享者工程、游戏素材、账号、API Key、会话日志或个人安装备份。

本包不是 Unity 官方 CLI 产品，也不包含 Unity Editor、Unity 授权、Python 或 Unity Package Manager 完整离线缓存。
