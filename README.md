# Checkin_wb

该项目为https://github.com/y1ndan/genshin-impact-helper 的修改版，代码的绝大部分逻辑为原项目逻辑，本项目作者只对极少部分代码进行了微调。

感谢@y1ndan 及 https://github.com/y1ndan/genshin-impact-helper 相关代码贡献者。

如有侵权请告知，作者将看到后第一时间删除该项目。

## 🌀简介

Checkin_wb 可以自动化为你检查忘川风华录在微博超话的签到活动，并自动进行签到、领取激活码。

## 📐部署

1. Fork 仓库
2. 获取 Cookie
3. 添加 Cookie 至 Secrets
4. 启用 Actions


WB_COOKIE: 新浪微博的COOKIE.前往  https://m.weibo.cn 获取.

KA_COOKIE: 新浪新手卡的COOKIE.前往 https://ka.sina.com.cn 获取.

登录微博账号
- 按`F12`，打开`开发者工具`，找到`Network`并点击
- 按`F5`刷新页面，按下图复制`Cookie`
- 添加 Cookie 至 Secrets

- 回到项目页面，依次点击`Settings`-->`Secrets`-->`New secret`


- 建立名为`WB_COOKIE`和`KA_COOKIE`的 secret，值为`步骤2`中复制的`Cookie`内容，最后点击`Add secret`


# 🔔订阅

若开启订阅推送，无论成功与否，都会收到推送通知

### Push All In One

支持Server酱、酷推、Bark App、Telegram Bot、钉钉机器人、企业微信机器人、企业微信应用、iGot聚合推送、pushplus和自定义推送 单个或多个推送，配置对应参数就会开启对应的推送方式，参数列表详见下文`参数`部分。

#### Server酱

以Server酱为例：

**a.获取 SCKEY**

- 使用 GitHub 登录 [sc.ftqq.com](http://sc.ftqq.com/?c=github&a=login) 创建账号
- 点击「[发送消息](http://sc.ftqq.com/?c=code)」，获取`SCKEY`
- 点击「[微信推送](http://sc.ftqq.com/?c=wechat&a=bind)」，完成微信绑定

**b.添加 SCKEY 到 Secrets**

- 建立名为`SCKEY`的 secret，并添加获取的 SCKEY 值，即可开启Server酱推送

## 🧬参数

在`Settings`-->`Secrets`里添加的参数，`Name`必须为下列的参数名称之一，`Value`则填写对应获取的值

|   参数名称         |   是否必填   |   默认值           |   说明                                                          |
|---                |---          |---                 |---                                                              |
|   WB_COOKIE       | ✅         |                    |   新浪微博的Cookie                                                 |
|   KA_COOKIE       | ✅         |                    |   新浪新手卡中心的Cookie                                                 |
|   SCKEY           | ❌         |                    |   Server酱的SCKEY                                                |
|   COOL_PUSH_SKEY  | ❌         |                    |   Cool Push的SKEY                                                |
|   COOL_PUSH_MODE  | ❌         | send               |   Cool Push的推送方式.可选私聊(send)、群组(group)或者微信(wx).      |
|   BARK_KEY        | ❌         |                    |   Bark的IP或设备码                                                |
|   BARK_SOUND      | ❌         | healthnotification |   Bark的推送铃声.在APP内查看铃声列表                                |
|   TG_BOT_TOKEN    | ❌         |                    |   Telegram Bot的token.向bot father申请bot时生成                    |
|   TG_USER_ID      | ❌         |                    |   Telegram推送对象的用户ID                                         |
|   DD_BOT_TOKEN    | ❌         |                    |   钉钉机器人WebHook地址中access_token后的字段                       |
|   DD_BOT_SECRET   | ❌         |                    |   钉钉加签密钥.在机器人安全设置页面,加签一栏下面显示的以SEC开头的字符串 |
|   WW_BOT_KEY      | ❌         |                    |   企业微信机器人WebHook地址中key后的字段                             |
|   WW_ID           | ❌         |                    |   企业微信的企业ID(corpid).在'管理后台'->'我的企业'->'企业信息'里查看  |
|   WW_APP_SECRET   | ❌         |                    |   企业微信应用的secret.在'管理后台'->'应用与小程序'->'应用'->'自建',点进某应用里查看|
|   WW_APP_USERID   | ❌         | @all               |   企业微信应用推送对象的用户ID.在'管理后台'->'通讯录',点进某用户的详情页里查看   |
|   WW_APP_AGENTID  | ❌         |                    |   企业微信应用的agentid.在'管理后台'->'应用与小程序'->'应用',点进某应用里查看   |
|   IGOT_KEY        | ❌         |                    |   iGot的KEY                                                         |
|   PUSH_PLUS_TOKEN | ❌         |                    |   pushplus一对一推送或一对多推送的token                               |
|   PUSH_PLUS_USER  | ❌         | 一对一推送          |   pushplus一对多推送的群组编码                                        |
|   PUSH_CONFIG     | ❌         |                    |   JSON格式的自定义推送配置.详见 订阅-自定义推送 部分说明                |




❗️协议

使用 Checkin_wb 即表明，您知情并同意：

- 此代码通过模拟浏览器使用 Cookies 登录网页，点击页面完成签到来实现签到。功能通过官方公开的 API 实现，并非游戏外挂
- 该项目禁止用于商业用途。
- 用户之 Cookie 被储存于 Github 服务器，只供本项目使用。若 Github 服务器被攻破，则您的 Cookie 有遭到泄露的风险。除此之外，开发者无权获取您的 Cookie；即使是用户，一旦创建完成`Secrets`，也无法再次从中查看 Cookie
- Checkin_wb 不会对您的任何损失负责，包括但不限于奖励回收、账号异常、第三次世界大战等
