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
选择左侧任意 AI（甜蜜女友，也可以点击 ![fenleiorguangchangorqitatianchong.png](docs%2Ffenleiorguangchangorqitatianchong.png) 添加更多AI），选择「智体」。
![iShot_2025-03-03_20.35.29.png](docs%2FiShot_2025-03-03_20.35.29.png)
点击「绑定新设备」，输入小智硬件提示的6位数字验证码，点击「确认」。
![iShot_2025-03-03_20.36.26.png](docs%2FiShot_2025-03-03_20.36.26.png)
三、【开始使用】  
唤醒小智，即可开始聊天对话。

### 声音复刻
打开 TalkX，选择已绑定设备的 AI，进入「智体」，点击页面上方的「我的声音」，复刻声音。  
![iShot_2025-03-03_20.43.02.png](docs%2FiShot_2025-03-03_20.43.02.png)

复刻成功之后，在「智体设置」页面，声音角色选择刚才复刻的声音，保存即可。
![iShot_2025-03-03_20.43.46.png](docs%2FiShot_2025-03-03_20.43.46.png)

### 切换模型
点击AI，进入聊天界面，然后在输入框的左下角切换模型。
```
建议选择国内模型，延迟低，模型列表会不定期更新。
```
![iShot_2025-03-03_20.45.16.png](docs%2FiShot_2025-03-03_20.45.16.png)

### 模型调参
点击AI，更多选项中选择「编辑」，可以设置模型的角色定义及其他配置。
![iShot_2025-03-03_20.49.59.png](docs%2FiShot_2025-03-03_20.49.59.png)
![iShot_2025-03-03_20.50.11.png](docs%2FiShot_2025-03-03_20.50.11.png)