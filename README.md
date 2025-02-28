# R66S OpenWrt 固件

[![GitHub Actions](https://img.shields.io/github/actions/workflow/status/king/r66s-action/build-r66s-openwrt.yml?label=构建状态)](https://github.com/king/r66s-action/actions/workflows/build-r66s-openwrt.yml)
[![固件下载](https://img.shields.io/github/release/king/r66s-action?color=blue&label=固件下载)](https://github.com/king/r66s-action/releases)
[![仓库访问](https://img.shields.io/github/stars/king/r66s-action?color=orange&label=仓库访问)](https://github.com/king/r66s-action)

本项目基于 GitHub Actions 自动构建 R66S 路由器的 OpenWrt 固件。支持 Lean 的 LEDE 源码和 ImmortalWrt 源码，提供稳定可靠的固件编译服务。

## 固件特性

- **双版本支持**：同时支持 Lean 的 LEDE 源码和 ImmortalWrt 源码
- **自动编译**：每天定时自动编译，确保固件及时更新
- **丰富插件**：预置多种常用插件，满足不同用户需求
- **精简稳定**：优化系统配置，提供流畅稳定的使用体验
- **默认配置**：默认 IP 地址：`192.168.100.1`，默认密码：`password`

## 支持插件

### 网络相关
- **科学上网**
  - SSR Plus：全能的科学上网工具
  - PassWall/PassWall2：强大的出国工具
  - OpenClash：基于 Clash 核心的科学上网工具
  - Mihomo：另一个基于 Clash 的代理工具

### 系统工具
- **系统管理**
  - TTYD 终端：网页终端
  - 晶晨宝盒：针对晶晨 SoC 设备的管理工具
  - NetData：实时性能监控
  - 定时重启：系统定时重启服务
  - 文件传输：文件管理工具

### 网络工具
- **网络优化**
  - ZeroTier：虚拟局域网工具
  - MosDNS：DNS 转发器
  - SmartDNS：本地 DNS 服务器

### 存储应用
- **文件管理**
  - Alist：强大的网盘管理工具

## 主题支持

- **Argon**：清新现代的主题
- **Design**：简约设计风格主题
- **Edge**：锐利边缘风格主题
- **OpenTomcat**：开源猫主题

## 使用方法

### 下载固件

1. 前往 [Releases](https://github.com/king/r66s-action/releases) 页面下载最新固件
2. 选择对应的版本：
   - `armv8-lede-xxx.img.gz`：基于 Lean 源码的固件
   - `armv8-immortalwrt-xxx.img.gz`：基于 ImmortalWrt 源码的固件

### 安装固件

1. 解压下载的固件
2. 使用 balenaEtcher 或 dd 命令将固件写入 TF 卡或 U 盘
3. 将写入好固件的存储设备插入 R66S 路由器
4. 启动路由器，等待系统启动完成
5. 使用浏览器访问 `192.168.100.1` 进入管理界面

### 自定义编译

如果需要自定义编译：

1. Fork 本仓库
2. 修改 `configs/armv8.config` 文件，添加或删除所需插件
3. 修改 `diy-lede.sh` 或 `diy-immortalwrt.sh` 进行个性化定制
4. 在 Actions 页面手动触发构建工作流

## 定制说明

- 默认管理 IP：`192.168.100.1`
- 默认用户名：`root`
- 默认密码：`password`
- TTYD 终端已配置免密登录

## 鸣谢

- [Lean's LEDE](https://github.com/coolsnowwolf/lede)
- [ImmortalWrt](https://github.com/immortalwrt/immortalwrt)
- [OpenWrt](https://github.com/openwrt/openwrt)
- [GitHub Actions](https://github.com/features/actions)
- [flippy-openwrt-actions](https://github.com/haiibo/flippy-openwrt-actions)
- 以及所有插件的开发者

## 许可

本项目遵循 [MIT 许可协议](LICENSE)。