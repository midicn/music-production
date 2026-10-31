---
id: job-live-stream
site: prod
cat: D
order: 523
title: 直播音频
title_en: Live Stream Audio
summary: 直播的人声、床与触发音，先保可懂，再谈气氛。
summary_en: Voice, beds and triggers for a live stream, with intelligibility before atmosphere.
level: standard
tags: [流程, 直播, 音频, 响度]
tags_en: [workflow, live stream, audio, loudness]
alias: [直播音频, 直播声音, 直播配乐, live stream audio]
links:
  - "[[glossary:loudness-normalization]]"
  - "[[glossary:headroom]]"
  - "[[instrument:polysynth]]"
instances:
  - oga-000089 | 一分多钟的循环曲，结构稳定，可参考直播长时段的循环床
  - oga-000088 | 二十四秒的循环，长度短，适合对照「床」与「过场」的差别
  - groove-000011 | 三分半的放克鼓型，可听长段落里怎样靠细微变化维持听感
  - oga-000283 | 四秒半的选单音，起音清楚，可作通知与切换提示
sources:
  - OBS Studio 官方文档 — Audio Mixer、Audio Filters 与 Audio Monitoring 三节。
  - Twitch Music Guidelines — 直播、回放与剪辑片段的音乐使用边界。
  - EBU R 128 — 响度与真峰值的测量口径。
tool_kind: guide
tool_vendor: —
tool_form: 流程
tool_platforms: [通用]
tool_price: 不适用
tool_jobs: [流程]
tool_verified: 2026-10-31
updated: 2026-10-31
---

::: zh
## 先解决回路与延迟，再谈音乐

直播音频最常见的坏法不是音质差，是回授、延迟和双重监听。先画信号链：话筒进接口，游戏声与桌面声各走一路，音乐播放器单独一路，全部汇到 OBS 一类直播软件。监听只留一条路径，别让主播同时听声卡直监和软件监听，否则会出现梳状滤波。缓冲区先保稳定，再加插件；机器吃不消时，掉帧比音质更伤直播。

## 三套声音各管一件事

| 层 | 作用 | 处理 | 常见错误 |
|---|---|---|---|
| 人声 | 可懂度 | 高通 80–100 Hz，轻压缩，少量齿音控制 | 混响太多，字头糊 |
| 床 | 气氛与填空 | 比人声低 12–18 dB，侧链或手拉 | 一直满编，盖住说话 |
| 触发 | 通知、转场 | 短，峰值低于人声 | 连发，抢话 |

床是背景，不是主角。人声一进来，床要退；句间回来时不要抽气，侧链的释放留长一点。触发音只在对的地方响，别让打赏提示每隔十秒切一次气氛。

## 按场景搭一条信号链

给每一路起名字，推子前后保持一致。人声加高通、轻压缩和去齿音；音乐加限制器，防突然的峰值；游戏声单独控制，别和话筒一起进同一条压缩。做三个场景：聊天、游戏、休息，每个场景存一套音量，切换前先把音乐拉低再开麦。用手机外放试一次，听字头还在不在。音乐只用有授权的版本，否则回放和剪辑片段会被静音。把场景和信号链图留档，换机器时照图重搭。

## 上线前的检查

- 耳机里没有自己的延迟回声
- 说话时音乐退，句间回来不抽气
- 手机外放能听清每个字
- 通知音不盖过人声
- 游戏声与话筒不互相触发回授
- 直播与录制的电平一致
- 每路有名字，推子前后一致
- 断流重连后场景恢复默认

## 观众端的失败模式

人声太轻、音乐太满；混响像在浴室；手机外放只剩低频的轰；通知音连发；音乐版权导致回放静音；采样率不匹配，声音变调；双路监听造成梳状滤波；直播很响、录像很轻；过度压缩，笑声和喊声全被压平；用系统立体声混音把桌面所有提示音都播出去。

```audiolab
{"type":"instrument","gm":"Pad 2 (warm)","synth":"bowed","phrase":["C3","G3","C4","E4"],"label":"人声下面的四音铺底","label_en":"A four-note bed under a voice","hint":"先听铺底，再想人声进来时它该退多少","hint_en":"Hear the bed first, then decide how far it should drop when the voice enters"}
```
:::

::: en
## Fix the loop and latency first

The usual failure in live-stream audio is not poor tone but feedback, delay and double monitoring. Draw the signal chain: microphone into the interface, game and desktop audio on separate paths, music player on its own path, all summed in OBS or similar streaming software. Keep one monitoring route; if the host hears both direct monitoring and software monitoring, comb filtering follows. Favour a stable buffer before adding plug-ins. When the machine struggles, dropped frames hurt the stream more than tone does.

## Three layers, three jobs

| Layer | Job | Treatment | Common mistake |
|---|---|---|---|
| Voice | Intelligibility | High-pass at 80–100 Hz, light compression, some sibilance control | Too much reverb, blurred consonants |
| Bed | Atmosphere and fill | 12–18 dB under the voice, sidechain or manual rides | Always full, covering speech |
| Trigger | Alerts and transitions | Short, peak below the voice | Firing in bursts, talking over the host |

The bed is background, not a co-lead. It drops when the voice enters and returns without pumping; give the sidechain a longer release. Triggers belong at real moments, not every ten seconds when a donation arrives.

## Building the chain by scene

Name every path and keep pre-fader and post-fader consistent. Give the voice a high-pass, light compression and de-essing; put a limiter on the music against sudden peaks; control game audio separately instead of running it through the vocal compressor. Build three scenes, talk, game and break, save a level set for each, and pull the music down before opening the microphone. Check once on a phone speaker and see whether the consonants survive. Use only music you are licensed to use, or the replay and clips will be muted. Keep the scenes and a signal-chain diagram on file so a new machine can be rebuilt from it.

## Pre-flight checks

- No delayed echo of your own voice in the headphones
- Music drops under speech and returns without pumping
- Every word is clear on a phone speaker
- Alert sounds do not cover the voice
- Game audio and microphone do not set each other off
- Stream and recording levels match
- Every path is named and pre/post-fader settings agree
- Scenes return to default after a reconnect

## How it fails at the viewer's end

The voice is too quiet and the music too full. Reverb sounds like a bathroom. On a phone speaker only low-end rumble remains. Alerts fire in bursts. A music claim mutes the replay. A sample-rate mismatch bends the pitch. Double monitoring creates comb filtering. The stream is loud and the recording is quiet. Over-compression flattens laughter and shouts. System stereo mix sends every desktop notification to air.
:::
