<h1 align="center">ChatGPT-weBot</h1>



[TOC]

使用基于 ChatGPT官方API 和 官方微信 hook 接口 的 ChatGPT-weBot 机器人。中文文档 | [English](./Readme.md)

###### 作者

[Snapdragon Lee (github.com)](https://github.com/SnapdragonLee)
[yehaodong (github.com)](https://github.com/EvAnhaodong)


## 支持和特点

- [x] 支持对话
- [x] 支持上下文感知问答
- [x] **使用官方微信软件执行，信息来源方面永不封禁**
- [x] 设置关键字在私聊中唤醒微信机器人
- [x] 设置关键字在群中唤醒微信机器人
- [x] 在线获取帮助文档
- [x] 设置关键字以重置之前的对话
- [x] 重新生成答案


## 默认配置 （请在启动前仔细阅读，所有配置文件在.config中）

```
{
  // 本地host运行地址（仅本地）
  "server_host": "127.0.0.1:5555",

  // 是否开启ChatGPT自动回复
  "autoReply": true,
  // 在群聊中设置唤醒机器人关键词
  "groupChatKey": "-c",
  // 在群聊中响应回复
  "grpReplyMode": false,
  // 在群聊回答前添加源问题格式
  "grpCitationMode": true,
  // 在私聊中设置唤醒机器人关键词
  "privateChatKey": "-c",
  // 在私聊中响应回复
  "prvReplyMode": true,
  // 在群聊回答前添加源问题格式
  "prvCitationMode": false,

  // 查看可用命令帮助
  "helpKey": "-h",
  // 设置重置上下文关键词
  "resetChatKey": "-rs",
  // ChatGPT API key : https://platform.openai.com/account/api-keys
  "api": ""
}
```


## 启动步骤

1. 安装 `requirements.txt` 中列出的所有包，使用如下命令：

   ```
   pip install -r ./requirements.txt
   ```

   

2. 从 Github Releases 下载需要的包。

3. 在您的计算机上安装 `WeChat-3.6.0.18.exe`，**如果您正在使用的微信版本高于3.6.0.18，可以降级覆盖安装。** 之后请登陆您的微信。**

   
4. 运行服务器监控微信消息。这里有两种方法可以实现，请 ***二选一***：

   - 运行 `funtool_3.6.0.18-1.0.0013.exe` ，后点击 `Start` 。

     ![image-20230221044609319](assets/image-20230221044609319.png)

5. 在 `.config/` 目录下填写 JSON 文件。

   - 在 `config.json` 中，您需要根据自己的偏好配置自定义选项。

6. 运行以下命令启动服务：

   ```
   python main.py
   ```

   **一切准备就绪，欢迎使用 ChatGPT-weBot！** 


## 常见问题解答

1. 如何获取所有的回复？您可以用您的语言说 “请继续”。
2. 遇到问题了吗？随时来创建一个 issue 进行发布。


###### 参考

- [AutumnWhj/ChatGPT-wechat-bot: ChatGPT for wechat](https://github.com/AutumnWhj/ChatGPT-wechat-bot)
- [cixingguangming55555/wechat-bot: 带二次开发接口的PC微信聊天机器人](https://github.com/cixingguangming55555/wechat-bot)

