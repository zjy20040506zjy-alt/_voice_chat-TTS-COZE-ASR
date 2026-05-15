# ESP32-S3 AI Voice Interaction

ESP32-S3 + Coze + Doubao ASR/TTS，端到端中文语音交互：  
语音采集 → 云端识别 → 智能对话 → 实时语音合成播放。

## Features
- ESP32-S3 I2S 麦克风/喇叭
- 流式 ASR、流式 TTS、WebSocket
- Coze 智能体状态机解析
- FreeRTOS、PSRAM 优化、低延迟

## Hardware
- ESP32-S3 (with PSRAM)
- Mic: ICS-43434
- Speaker: MAX98357

### Wiring
- Mic：BCLK=42, LRC=2, DOUT=1
- Speaker：BCLK=39, LRC=40, DIN=38

## Configuration
```cpp
WiFi.begin("YOUR_WIFI", "PASSWORD");
CozeAgent agent("YOUR_COZE_BOT_ID", &tts);
setExtraHeaders("Authorization: Bearer YOUR_TOKEN");
