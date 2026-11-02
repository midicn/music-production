---
id: noise-and-hum
site: prod
cat: A4
title: 噪声与哼声
title_en: Noise and Hum
summary: 先区分宽带嘶声、工频及谐波，再逐段排查环境、电路与连接。
summary_en: Distinguish broadband hiss from mains-frequency components, then isolate environmental, circuit and connection causes.
level: standard
tags: [录音, 噪声, 接地]
tags_en: [recording, noise, grounding]
alias: [底噪, 哼声, 交流声, 嘶声, hum, hiss, noise]
links:
  - "[[glossary:noise-floor]]"
  - "[[glossary:signal-to-noise]]"
  - "[[instrument:organ]]"
instances:
  - cyberhymnal-001740 | 管风琴持续和弦可作背景素材；排查哼声需另录实际设备的静音与有声片段 | Sustained organ chords offer background material; diagnose hum with separate recordings of actual silent and active equipment
  - mutopia-000848 | 弱奏吉他可用于设计信号与底噪的混合练习，噪声需另行加入并记录电平 | Soft guitar can support signal/noise mixing practice; add noise separately and log its level
  - openscore-000667 | 声乐与伴奏可作降噪练习的音乐底稿，不能据 MIDI 判断房间噪声或电流声 | Voice and accompaniment provide a musical base for denoising practice, not evidence of room or electrical noise in the MIDI
sources:
  - Ballou, Handbook for Sound Engineers, grounding and shielding chapters
  - AES Convention paper on hum, ground loops and balanced interconnection
updated: 2026-11-02
---

::: zh
## 问题

嘶声、窄带嗡声、无线干扰和房间杂声可有不同来源。先看它是否随输入增益、线缆或设备连接变化，再判断应处理环境、布线、供电还是音频文件，不能只凭音色确定原因。

## 信号链

模拟电子噪声、话筒自噪声与环境声会随增益链一起进入录音。50或60 Hz及其谐波可能与供电或地环路有关，也可能来自电磁感应和机械振动。用频谱确认频率，逐段改变连接定位来源，不要把所有嗡声都诊断为地环路。

## 摆位与参数

先降低监听音量，再按设备手册依次检查信号线、输入模式与增益。用已知良好的平衡线或隔离器验证音频路径，线缆布局远离强干扰源。不得通过断开电源保护地线来消嗡；涉及供电故障时应由合适人员处理。需要后期去嗡时先测频率，并保存未处理录音。

```audiolab
{"type":"instrument","gm":"Contrabass","synth":"bowed","phrase":["G1","G1"],"label":"G1 音高参照","label_en":"A G1 pitch reference","hint":"G1约49 Hz，可帮助定位50 Hz附近；这段是低音乐器音，不是实际市电哼声，60 Hz及谐波需另测。","hint_en":"G1 is about 49 Hz, near 50 Hz. This is a bass-instrument tone, not recorded mains hum; measure 60 Hz and harmonics separately."}
```

## 听什么

记录安静输入与实际演奏两种状态，保持监听在安全范围，比较噪声是否随输入增益或某个连接改变。切换设备或插拔时先静音，避免瞬时冲击。最后检查修复是否损伤了有用低频，而非只看嗡声是否变小。

## 常见误解

- 噪声大不一定需要更换话筒
- 降噪和去嗡不能修复所有供电或布线故障
- 频谱峰值只是定位线索，不是单一成因的证明
- 保留测试条件和原始文件，便于重复排查
:::

::: en
## The problem

Hiss, narrow-band hum, radio interference and room noise have different possible sources. Check changes with gain, cables and connections before choosing environmental, wiring, power or file processing; sound alone does not identify the cause.

## Signal chain

Electronic noise, microphone self-noise and environment enter through the gain chain. Mains-frequency hum and harmonics may involve power or ground loops, but also magnetic induction or mechanical vibration. Identify frequencies and change connections stage by stage rather than diagnosing every hum as a ground loop.

## Placement and settings

Lower monitoring before checking cables, input mode and gain according to manuals. Test the audio path with known-good balanced connections or suitable isolation, away from strong interference. Do not defeat protective mains earth to remove hum; power faults need qualified attention. Measure frequencies before later de-hum and preserve the original.

```audiolab
{"type":"instrument","gm":"Contrabass","synth":"bowed","phrase":["G1","G1"],"label":"A G1 pitch reference","label_en":"A G1 pitch reference","hint":"G1 is about 49 Hz, near 50 Hz. This is a bass-instrument tone, not recorded mains hum; measure 60 Hz and harmonics separately.","hint_en":"G1 is about 49 Hz, near 50 Hz. This is a bass-instrument tone, not recorded mains hum; measure 60 Hz and harmonics separately."}
```

## What to listen for

Record quiet input and performance at safe monitoring levels, noting noise changes with gain or a connection. Mute before switching or connecting equipment to avoid transients. Finally check whether a repair removed wanted bass rather than judging only hum reduction.

## Common misconceptions

- Noise does not automatically call for a new microphone
- Denoising/de-hum cannot repair every wiring or power fault
- Spectral peaks are clues, not proof of one cause
- Preserve test conditions and originals for repeatable diagnosis
:::
