CS - 跨服传送插件 🚀
彻底解决菜单插件调用跨服指令的顽疾
License Version

🔍 痛点背景
原版 Minecraft 跨服指令 /server [服务器名] 存在以下问题：

❌ 菜单插件兼容性差：钟表菜单等插件调用时提示「未知指令」

❌ 交互不友好：玩家直接使用指令体验生硬

🚀 解决方案
CS 插件通过底层协议重构跨服流程
✅ 零指令污染 - 完全绕过 server 指令系统
✅ 即装即用 - 无需任何权限配置和前置插件
✅ 完美兼容 - 支持所有菜单插件调用

⚙️ 技术实现
mermaid
复制
graph LR
A[玩家执行 /cs] --> B(插件捕获请求)
B --> C{验证配置文件}
C --> D[通过BungeeCord协议发送连接请求]
D --> E[[Velocity代理服务器]]
E --> F[目标服务器]
核心技术栈：

📡 BungeeCord 插件消息机制
使用标准 Connect 协议直接建立跨服连接

🛡️ 绕过指令系统
通过 ByteArrayOutputStream 实现底层数据包通信

🔧 轻量化设计
仅需 3KB 内存占用，零运行时依赖

📥 安装指南
环境要求
Minecraft 服务端版本 ≥ 1.16

使用 Velocity/BungeeCord 代理架构

配置流程
将插件放入 plugins 文件夹

启动服务器生成配置文件 plugins/CS/config.yml

编辑配置文件：

yaml
复制
# 必须与 velocity.toml 中的服务器名称一致
target-server: "lobby"
在 Velocity 代理端验证服务器配置：

toml
复制
[servers]
lobby = "127.0.0.1:25565"  # 实际服务器地址
使用方式
玩家直接执行 /cs

菜单插件配置示例（DeluxeMenus）：

yaml
复制
command: 'cs'
📜 协议声明
本项目采用 MIT License

基于 BungeeCord 通信协议开发，符合 Minecraft EULA 规范
