<div align="center">

<a href="https://github.com/ajiua/Inkita-Leaf">
    <img src="./.github/assets/inkita-logo.png" alt="Inkita Leaf 图标" title="Inkita Leaf" width="96"/>
</a>

# Inkita Leaf

一款轻量、流畅的 Kavita Android 阅读器。

[![CI](https://img.shields.io/github/actions/workflow/status/ajiua/Inkita-Leaf/lint.yml?branch=master&label=CI&labelColor=27303D)](https://github.com/ajiua/Inkita-Leaf/actions/workflows/lint.yml)
[![Release](https://img.shields.io/github/v/release/ajiua/Inkita-Leaf?include_prereleases&label=Release&labelColor=2c2c47&color=1c1c39)](https://github.com/ajiua/Inkita-Leaf/releases)
![Platform](https://img.shields.io/badge/平台-Android-blue)
![Language](https://img.shields.io/badge/界面-简体中文-389564)

> 本项目基于 [dom-53/Inkita](https://github.com/dom-53/Inkita) 开发，在保留原项目核心能力的基础上增加简体中文支持、独立图标及适配本仓库的发布与自动更新流程。

</div>

---

## 项目简介

Inkita Leaf 是一款面向自托管 [Kavita](https://www.kavitareader.com/) 服务器的轻量 Android 阅读器，提供快速浏览、离线下载和可靠的阅读进度同步。应用会缓存元数据、页面和缩略图，让你在没有网络时也能继续阅读，并在恢复连接后准确同步上次阅读位置。

项目使用 Kotlin 与 Jetpack Compose 构建，专注于简洁的阅读体验、快速导航和与 Kavita API 的紧密集成。

## 主要功能

- 浏览 Kavita 媒体库、系列、收藏、阅读列表、标签和类型。
- 支持搜索、排序和多条件筛选。
- 查看封面、作者、出版信息、卷、章节和相关作品。
- 支持 EPUB、PDF、图像及归档类内容的阅读流程。
- 自动同步阅读进度，并支持标记已读或未读。
- 下载系列、卷、章节或页面，支持离线阅读。
- 缓存元数据、详情、页面和缩略图。
- 提供离线模式、下载队列和缓存管理。
- 支持浅色、深色及多种阅读器主题。
- 支持简体中文、英语和捷克语界面。
- 通过 GitHub Releases 检查、下载和安装新版本。

## 下载与安装

APK 会发布在本仓库的 [Releases](https://github.com/ajiua/Inkita-Leaf/releases) 页面。

- 带有 `-alpha` 或 `-beta` 的版本属于预览版。
- 不带预发布后缀的版本属于正式版。
- Android 安装第三方 APK 时，可能需要允许浏览器或文件管理器“安装未知应用”。

应用使用以下地址检查更新：

```text
https://ajiua.github.io/Inkita-Leaf/updates.json
```

APK 文件由 GitHub Releases 托管，不需要额外的下载服务器。

## 连接 Kavita

Inkita Leaf 不包含任何预设服务器。首次使用时：

1. 打开“设置 → Kavita”。
2. 输入 Kavita 服务器地址。
3. 填写 API 密钥和图像 API 密钥。
4. 保存配置并重新启动应用。

应用默认使用 HTTPS。局域网环境也可以手动关闭“使用 HTTPS”并通过 HTTP 连接，但 HTTP 不加密，请只在可信网络中使用。

## 本地构建

开发环境要求：

- Android Studio
- JDK 17 或更高版本
- Android SDK 36

调试构建：

```bash
./gradlew assembleDebug
```

正式发布由 [GitHub Actions](https://github.com/ajiua/Inkita-Leaf/actions/workflows/release.yml) 完成。推送以 `v` 开头的标签即可触发，例如：

```bash
git tag v0.3.2-beta
git push origin v0.3.2-beta
```

## 日志与问题反馈

可以在“设置 → 高级 → 日志”中保存或分享经过脱敏处理的日志。保存的日志位于设备的 `Documents/Inkita/logs` 目录。

提交问题前，建议开启“详细日志”、复现问题，然后将导出的 ZIP 文件附在 Issue 中。请勿公开包含服务器地址、账号或密钥的原始数据。

## 项目来源

Inkita Leaf 来源于 [Inkita](https://github.com/dom-53/Inkita)，原项目由 `dom-53` 创建，是一款非官方 Kavita Android 客户端。

本分支保留对原作者及原项目的明确署名。感谢原作者与所有贡献者完成了应用架构、阅读器、下载、缓存和 Kavita API 集成等核心工作。

如果你希望了解原项目、提交上游问题或参与原版开发，请访问：

```text
https://github.com/dom-53/Inkita
```

## 参与贡献

欢迎提交 Issue 和 Pull Request，包括：

- 中文翻译修正
- 功能改进和错误修复
- 阅读体验优化
- Kavita API 兼容性改进
- 文档完善

提交代码前建议运行：

```bash
./gradlew spotlessCheck detekt
```

## 许可证与声明

本项目遵循仓库中的 [LICENSE](./LICENSE)。衍生修改继续保留原项目的版权与许可证信息。

Inkita Leaf 是社区维护的非官方项目，与 Kavita 官方无隶属或合作关系。使用前请自行评估预览版本可能存在的兼容性和稳定性问题。
