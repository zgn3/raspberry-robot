# raspberry-robot
基于树莓派的桌面情感交互机器人项目。

本项目面向毕业设计，目标是搭建一个具备语音交互、情感识别、大语言模型回复生成和语音播报能力的桌面机器人系统。机器人端部署在树莓派上，负责语音采集、音频播放和外设控制；后端负责语音识别、情感识别、对话生成和语音合成。
---

## 项目目标
实现一个桌面小机器人，具备以下基本能力：

- 采集用户语音
- 将语音上传到后端
- 后端生成回复
- 树莓派播放回复语音
- 后续扩展情感识别、LED 灯效、表情显示和多轮对话

---

## 当前开发阶段

当前优先完成最小闭环：

**树莓派录音 -> 后端回复 -> 树莓派播放**

在最小闭环跑通后，逐步加入：

- 语音识别 ASR
- 情感识别
- 大语言模型回复生成
- 语音合成 TTS
- LED / OLED / 舵机反馈
- 多轮上下文记忆

---

## 项目结构

```text
raspberry-robot/
├── backend/
│   ├── app.py
│   ├── asr_service.py
│   ├── chat_service.py
│   ├── config.py
│   ├── dialog_service.py
│   ├── emotion_service.py
│   ├── memory_manager.py
│   ├── prompt_builder.py
│   ├── tts_service.py
│   ├── requirements.txt
│   ├── static/
│   └── uploads/
├── raspberry_pi_client/
│   ├── api_client.py
│   ├── audio_player.py
│   ├── audio_recorder.py
│   ├── display_controller.py
│   ├── led_controller.py
│   └── main.py
└── docs/
    ├── hardware_design.md
    ├── software_architecture.md
    └── test_plan.md**
