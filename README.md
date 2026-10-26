# AviumUI equuleus 自动编译

> 🤖 使用 GitHub Actions 自动编译 AviumUI

## 📱 适用设备

| 项目 | 信息 |
|------|------|
| 设备 | 小米,红米,一加 |
| ROM | AviumUI |

## 🚀 使用方法

### Fork 后手动触发

1. Fork 本仓库
2. 在 Actions 页面点击 "Build AviumUI"
3. 点击 "Run workflow" 开始编译
4. 等待编译完成，下载产物

## 📦 编译产物

编译完成后，在 Actions 的 Artifacts 中可以下载：
- `AviumUI-[设备代号]-YYYYMMDD.zip` — 刷机包
- `recovery.img` — Recovery 镜像
- `boot.img` — 内核镜像
- `build-info.txt` — 构建信息

## 📋 刷入步骤

1. 解锁 Bootloader
2. 刷入 第三方 Recovery（TWRP,AERA...）
3. 在 Rec 中三清（必要时需要五清）
4. 刷入编译好的 ROM 包
5. 可选：刷入 Magisk 获取 Root

## 🔧 环境要求（Self-hosted Runner）

| 项目 | 最低要求 | 推荐配置 |
|------|---------|---------|
| 系统 | Ubuntu 22.04 LTS | Ubuntu 22.04 LTS |
| 内存 | 16 GB | 32 GB+ |
| 磁盘 | 300 GB SSD | 400 GB+ SSD |
| CPU | 4 核 | 8 核+ |
| 网络 | 稳定连接 | 高速网络（源码同步） |

## ⚠️ 注意事项

- 首次源码同步需要 **几小时**，请确保网络稳定
- 编译过程需要 **4-8 小时**（取决于 CPU 性能）
- 确保 `/tmp` 有足够空间（编译过程中需要）
- GitHub Actions 标准 Runner **空间不足**，必须使用 Self-hosted Runner

## 📝 常见问题

### Q: 编译失败怎么办？
查看 Actions 日志，常见原因：
- 磁盘空间不足
- 内存不够（添加 swap）
- 网络问题导致源码不完整

### Q: 如何清理编译缓存？
在 Actions 页面选择 "clean_build" 选项重新运行

## 🙏 致谢

- [AviumUI](https://github.com/AviumUI) — ROM 开发团队
- [LineageOS](https://lineageos.org) — 设备树和内核源码

---

*本项目仅供学习交流使用，刷机有风险，操作需谨慎。*
