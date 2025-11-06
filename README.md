## Netlib 保活脚本
这是一个用于自动登录 Netlib 网站以保持账户活跃的脚本，配合 GitHub Actions 实现自动定时执行。

注册地址：https://www.netlib.re
### 功能特点
- 🔐 自动登录 Netlib 账户(单账户或多账户)
- 👥 支持多账户批量处理
- ⏰ 每60天自动执行一次
- 📱 执行结果可通过 Telegram 通知

### 使用方法
1. fork 此项目
2. 在Actions菜单允许 `I understand my workflows, go ahead and enable them` 按钮

4. 在 GitHub 仓库的 Settings → Secrets and variables → Actions 中添加以下环境变量
```
ACCOUNTS	Netlib账户(必填)，格式(单账号)：用户名:密码    格式(多账号)：用户名1:密码1,用户名2:密码2

不需要telegram通知可不配置
BOT_TOKEN	Telegram机器人Token	  123456:ABC-DEF1234ghIkl-zyx57W2v1u1212Dtr
CHAT_ID	   Telegram 聊天ID	      123456789
```

3. GitHub Actions 初始手动执行检查是否有配置错误，脚本会自动每60天执行一次,可手动执行

### 注意事项
1. 确保 Netlib 账户密码正确
2. 首次运行 GitHub Actions 需要授权
3. 脚本执行时间为 UTC 0:00（香港时间 8:00）
4. 如果不需要 Telegram 通知，可不配置相关环境变量


### 许可证
GPL 3.0
