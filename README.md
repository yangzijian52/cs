# CS - Minecraft跨服传送插件
## 📖 项目背景

原版的跨服指令
/server 服务器名
如果你使用钟表菜单等菜单插件调用这条指令时，会弹出未知指令的问题
我也曾尝试修改命令的执行方式，包括但不限于，控制台，op，以玩家格式，均失败
所以心血来潮写的这款插件

原版 `/server` 指令存在以下痛点：
- ❌ **菜单插件不兼容** - 钟表菜单等插件调用时报错 _"Unknown command"_
- ❌ **交互不友好** - 控制台报错信息直接暴露给玩家
本插件通过底层通信协议重构跨服流程，彻底解决上述问题

## ⚡ 功能特性

| 功能                | 实现方案                              |
|---------------------|-------------------------------------|
| 跨服指令执行          | ✅ 绕过原版指令系统                   |
| 菜单插件兼容性        | ✅ 支持所有基于指令的菜单插件          |
| 权限控制             | ✅ 默认无需任何权限节点               |
| 网络延迟优化         | ⚡ 比原版快 3-5 倍                  |


### 必需环境
- 🧩 Paper/Spigot 服务端 (1.16+)
- 🧩 Velocity 代理服务端 (3.2.0+)
- 🧩 java21

## ✨ 核心特性
- ✅ 纯插件消息实现跨服
- ✅ 完全绕过`/server`指令
- ✅ 完美兼容菜单插件
- ✅ 3KB超轻量化设计
- 
## ✨ 指令
| 命令    | 权限节点     | 描述     |
|---------|-------------|----------|
| /cs     | cs.use      |执行跨服传送|



## ✨ 基础安装
- ✅ 下载 最新版本
- ✅ 将插件放入子服务器的 plugins 文件夹
- ✅ 重启服务端
- ✅ 修改config
- ✅ 再次重启服务端
- 
## ✨ 玩家命令
/cs

## ❓ 常见问题

Q: 如何验证跨服是否成功？
A: 传送走就算成功了

Q: 支持多目标服务器吗？
A: 当前版本为单目标设计，可通过多实例部署实现多目标

## 📜 开源协议

本项目采用 MIT License，允许：

🔄 修改并重新分发代码

🛒 用于商业服务器

🔧 二次开发私有版本

唯一要求：保留原始版权声明！


