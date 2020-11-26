# 毒鸡汤 Telegram bot

## bot 的配置

- 登陆 TG, 与 [@BotFather](https://t.me/BotFather) 发起对话创建一个 bot 得到 `Token`
- 将 Bot 添加到你的 Group 中
- 访问如下 URL (注意替换 URL 中的 Token) 得到你的 `GROUP_ID` (message.chat.id)：
```
https://api.telegram.org/bot<Token>/getUpdates
```
如 `token = example123`，则访问 `https://api.telegram.org/botexample123/getUpdates` 进行获取。

## 脚本的配置

- Fork 代码到你的 github 账号
- 启动 Github Actions
- 找到项目的 Settings => Secrets 添加 `BOT_TOKEN=<Token>`, `GROUP_ID=<GROUP_ID>`

ps. 多个 `GROUP_ID` 使用**英文逗号**分割，如 `-123,456`

## 修改定时任务的时间

- 文件位于 .github/bot.yml 修改 cron 即可，默认是 UTC时间，注意进行转换
