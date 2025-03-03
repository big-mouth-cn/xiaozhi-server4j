# 小智 ESP32 后端服务（xiaozhi-server4j）

本项目为开源智能硬件项目 [xiaozhi-esp32](https://github.com/78/xiaozhi-esp32) 提供的后端服务。使用 小智MQTT+UDP 协议与 [TalkX](https://web.talkx.cn) 通信。因此小智硬件通过此项目连接的后台是 TalkX，而非小智官方后台。

## 特性
- 声音复刻

## 快速开始
一、【前提准备】  
你需要准备一个小智AI聊天机器人设备，点击 [xiaozhi-esp32](https://github.com/78/xiaozhi-esp32) 查看详情。  
然后将该项目的固件刷入到设备。:point_right: [Flash烧录固件（无IDF开发环境）](https://ccnphfhqs21z.feishu.cn/wiki/Zpz4wXBtdimBrLk25WdcXzxcnNS)

二、【绑定设备】  
打开 [TalkX](https://web.talkx.cn)，并登录。  
选择任意左侧的 AI（智能体），选择「智体」，点击「绑定」，输入小智硬件的 6位数字验证码 点击「确定」。

三、【开始使用】  
唤醒小智，即可开始聊天对话。

### 声音复刻
打开 TalkX，选择已绑定设备的 AI，进入「智体」，点击页面上方的「我的声音」，复刻声音。  
复刻成功之后，在「智体设置」页面，声音角色选择刚才复刻的声音即可。