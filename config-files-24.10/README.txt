================================================
K2 OpenWrt 24.10.4 配置文件说明（全功能版 + Attended Sysupgrade）
================================================

文件列表：
- .config                            # 编译配置文件
- mt7620a_phicomm_k2-v22.4.dts        # K2 v22.4 DTS文件（已修改为16M闪存）
- mt7620.mk                           # Makefile（IMAGE_SIZE已修改为16064k）

配置说明：
1. DTS 修改：partition@50000 的 reg 已从 0x7b0000 改为 0x1fb0000
2. Makefile 修改：phicomm_k2-v22.4 的 IMAGE_SIZE 从 7872k 改为 16064k
3. .config 包含以下功能：
   - LuCI 完整 Web 界面
   - 简体中文语言包
   - WireGuard（内核模块 + LuCI 界面）
   - ZeroTier（客户端 + LuCI 界面）
   - auc + Attended Sysupgrade（自动升级）
   - uhttpd Web 服务器

使用方法：
1. 将这些文件复制到 OpenWrt 24.10.4 源码对应目录
2. 完整固件请从 Actions 下载
================================================
