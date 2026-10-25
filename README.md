# 🐧 MiniOS

一个由 AI（Claude 3.5 Sonnet）深度辅助开发、基于 Debian Live 构建的轻量级 Linux 桌面操作系统。

## ✨ 核心特性

*   **轻量桌面**：采用 `Xfce` 桌面环境，资源占用极低，老旧电脑与虚拟机皆可流畅运行。
*   **开箱即用**：预装 Firefox 浏览器、NetworkManager 网络管理、中文字体及输入法支持。
*   **虚拟机增强**：专为 VirtualBox / VMware / QEMU 优化，自动编译开源 vboxvideo 驱动，支持分辨率自适应与共享剪贴板。
*   **数据持久化（Persistence）**：基于 `Overlayfs` 技术，可将系统及个人数据保存至独立磁盘，实现重启不丢失！

## 🚀 下载与使用

请直接前往右侧的 **[Releases](../../releases)** 页面，下载最新版本的 `.iso` 文件。

1. **虚拟机运行**：直接新建 Debian 64位 虚拟机，将 ISO 挂载至光驱启动即可。
2. **实体机运行**：使用 Rufus 或 Ventoy 等工具，将 ISO 烧录至 U 盘，从 U 盘引导启动。

## ⚠️ 使用注意事项（必看）

1. **持久化存储怎么用？**
   * 为了保护数据安全，系统内置的脚本会**自动屏蔽当前正在运行 MiniOS 的磁盘**。
   * 如果你在虚拟机测试，请额外挂载一块**空白虚拟硬盘**（建议 8GB 以上）。如果是物理机，请确保 U 盘有未分配空间。
   * 进入系统后，双击桌面 **“设置持久化存储”**，按提示一键格式化并配置即可。
2. **升级风险**
   * 基于 `overlayfs` 的特性，如果你下载了新版本，**请先备份数据并清空持久化盘**，否则旧底层文件可能引起系统黑屏崩溃。
3. **无线网卡固件**
   * 由于 Debian 默认不包含非自由固件，若较新的笔记本搜不到 WiFi，可能需要等待后续版本或自行注入固件。

## 🙏 致谢
*   基础框架：[Debian Live](https://www.debian.org/)
*   AI 辅助代码生成：[Claude](https://claude.ai/)
*   算力支持：[GitHub Actions](https://github.com/features/actions)

---
*If you like this project, please give it a ⭐!*
