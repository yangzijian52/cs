# cs
重新定义跨服指令
原版的跨服指令
/server 服务器名
如果你使用钟表菜单等菜单插件调用这条指令时，会弹出未知指令的问题
我也曾尝试修改命令的执行方式，包括但不限于，控制台，op，以玩家格式，均失败
所以心血来潮写的这款插件，这款插件
实现原理
BungeeCord 插件消息机制
使用 BungeeCord 插件消息通道发送跨服请求。
消息格式为 Connect + 目标服务器名称，这是 BungeeCord/Velocity 的标准跨服协议。
无需依赖 server 指令
直接通过底层通信实现跨服，彻底绕过指令系统，避免权限或语法问题。
Velocity 配置要求

在 velocity.toml 中确保目标服务器已声明：
[servers]
factions = "factions.example.com:25565"  # 你的服务器地址

使用方法：
将插件放到插件文件夹即可
运行后生成config文件，修改其中的服务器名称即可
