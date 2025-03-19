# 小智 AI 聊天机器人 （XiaoZhi AI Chatbot）

[![SVG Banners](https://svg-banners.vercel.app/api?type=origin&text1=%E5%B0%8F%E6%99%BA%20AI%20%E8%81%8A%E5%A4%A9%E6%9C%BA%E5%99%A8%E4%BA%BA&text2=💖%20for%20TalkX&width=800&height=300)](https://github.com/Akshay090/svg-banners)

本项目在开源智能硬件项目 [xiaozhi-esp32](https://github.com/78/xiaozhi-esp32) 基础上调整，并且使用 MQTT+UDP 协议与 [TalkX](https://web.talkx.cn) 通信。因此小智硬件通过此项目连接的后台是 TalkX，而非小智官方后台。

---

【开源版】

如果你想本地部署TalkX，可以点击查看 📢 [TalkX 服务端开源版本](https://github.com/big-mouth-cn/talkx)，两分钟搭建属于自己的小智服务端。

【开源版本部署视频教程】

[Bilibili（一）两分钟在本地部署一个TalkX](https://www.bilibili.com/video/BV1C3QdYeErz/)

[Bilibili（二）小智后台开源项目之TalkX部署](https://www.bilibili.com/video/BV17WQdYxE41/)


--- 

> 有任何问题或建议加QQ群：953272742

【小智智能机器人介绍视频】

👉 [ESP32+SenseVoice+Qwen72B打造你的AI聊天伴侣！【bilibili】](https://www.bilibili.com/video/BV11msTenEH3/)

👉 [给小智装上 DeepSeek 的聪明大脑【bilibili】](https://www.bilibili.com/video/BV1GQP6eNEFG/)

👉 [手工打造你的 AI 女友，新手入门教程【bilibili】](https://www.bilibili.com/video/BV1XnmFYLEJN/)

## 特性
- :white_check_mark: 🎉🔥 支持使用自己的声音进行复刻
- :white_check_mark: 🎉🔥 支持使用自己的大模型服务
- :white_check_mark: 🎉🔥 支持通过自动生成并更新记忆
- :white_check_mark: 基于 MQTT+UDP 协议的语音聊天
- :white_check_mark: 支持多语言语音识别和语音生成
- :white_check_mark: 支持多个AI、多个模型、多种声音切换
- :white_check_mark: 支持通过大模型实现IoT能力（需要选择支持function_call的大模型）

### 开发中 :construction:
- 微调更适合聊天的AI智体

## 快速开始


#### 一、【前提准备】

> 📢 **注意，如果烧录TalkX固件之前已经烧录过其他固件，烧录完成后务必重启一下。否则可能连接的仍是之前的服务器。**

**无IDF开发环境：**

首先，你需要准备一个小智AI聊天机器人设备：[《🤖小智 AI 聊天机器人百科全书》](https://ccnphfhqs21z.feishu.cn/wiki/F5krwD16viZoF0kKkvDcrZNYnhb)  
然后，下载对应的固件，提供两个下载地址： 1、[xiaozhi-server4j github release page](https://github.com/big-mouth-cn/xiaozhi-esp32-for-talkx/releases) | 2、[百度网盘](https://pan.baidu.com/s/1wX78aa3Q1bP90Rea5zxJsQ?pwd=taap)。  
最后，按照教程烧录固件：👉 [Flash烧录固件（无IDF开发环境）](https://ccnphfhqs21z.feishu.cn/wiki/Zpz4wXBtdimBrLk25WdcXzxcnNS)

---

**源码编译环境：**

将下面指定的配置项的值修改为 `https://api.talkx.cn/xiaozhi/ota/`

方式1、使用 `scripts/release.py` 编译：  
请修改源码中的 `/main/Kconfig.projbuild` 中的 `OTA_VERSION_URL`

方式2、使用 `idf.py build` 编译：  
请使用 `idf.py menuconfig` > `Xiaozhi Assistant` > `OTA Version URL` > 修改后按`S`键并退出；或者修改源码中的 `/sdkconfig` 中的 `CONFIG_OTA_VERSION_URL`。

#### 二、【绑定设备】
设备准备好并连接网络之后，进入激活模式。这时打开 [TalkX](https://web.talkx.cn)，并登录。  
选择左侧任意 AI 的菜单选项，点击「智体」。
> 点击 ![fenleiorguangchangorqitatianchong.png](docs%2Fscreenshot%2Ffenleiorguangchangorqitatianchong.png) 可以添加更多AI。对于聊天场景，建议选择适合对话场景的AI，如生活类、教育类等。也可以添加后编辑AI，以便适配聊天场景。

![iShot_2025-03-03_20.35.29.png](docs%2Fscreenshot%2FiShot_2025-03-03_20.35.29.png)
点击「绑定新设备」，输入小智硬件提示的6位数字验证码，点击「确认」。
![iShot_2025-03-03_20.36.26.png](docs%2Fscreenshot%2FiShot_2025-03-03_20.36.26.png)
#### 三、【开始使用】
唤醒小智，即可开始聊天对话。

## 声音复刻
打开 TalkX，选择已绑定设备的 AI，进入「智体」，点击页面上方的「我的声音」，复刻声音。  
![iShot_2025-03-03_20.43.02.png](docs%2Fscreenshot%2FiShot_2025-03-03_20.43.02.png)

复刻成功之后，在「智体设置」页面，声音角色选择刚才复刻的声音，保存即可。
> 音频时长：10～20秒，不建议超过60秒。在朗读时请保持连贯，至少包含一段超过5秒的连续语音。

![iShot_2025-03-03_20.43.46.png](docs%2Fscreenshot%2FiShot_2025-03-03_20.43.46.png)

## 开启记忆
打开 TalkX，选择已绑定设备的 AI，进入「智体」，点击页面上方的「记忆」，开启或关闭记忆。
![iShot_2025-03-11_17.48.31.png](docs%2Fscreenshot%2FiShot_2025-03-11_17.48.31.png)

## 切换模型
打开 TalkX，选择已绑定设备的 AI，进入「智体」，点击页面上方的「智体设置」，切换模型。或设置自己的模型服务。
```
:boom: 建议选择国内模型，延迟低。模型列表不定期更新或提供测试。
```
![iShot_2025-03-05_19.29.24.png](docs%2Fscreenshot%2FiShot_2025-03-05_19.29.24.png)

## 模型调参
点击AI，更多选项中选择「编辑」，可以设置模型的角色定义及其他配置。
![iShot_2025-03-03_20.49.59.png](docs%2Fscreenshot%2FiShot_2025-03-03_20.49.59.png)
![iShot_2025-03-03_20.50.11.png](docs%2Fscreenshot%2FiShot_2025-03-03_20.50.11.png)

# 鸣谢 :love_you_gesture:
- 小虾智能机器人设备开源项目：[xiaozhi-esp32](https://github.com/78/xiaozhi-esp32)
- 使用 [Silero-VAD](https://github.com/snakers4/silero-vad) 来检测用户的说话活动
- 使用 [Concentus](https://github.com/lostromb/concentus) 实现 Opus 音频编码/解码
- 使用 [SenseVoice](https://github.com/FunAudioLLM/SenseVoice) 实现语音识别
- 使用 [CosyVoice](https://github.com/FunAudioLLM/CosyVoice)、阿里云、火山引擎提供的语音生成能力
- 使用 通义千问、豆包、DeepSeek 等大模型实现LLM能力