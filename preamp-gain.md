---
id: preamp-gain
site: prod
cat: A4
title: 话放与增益
title_en: Preamps and Gain
summary: 话放把话筒的微弱电压抬到可用电平，增益分配决定底噪与余量
summary_en: The preamp lifts a microphone's tiny voltage to line level. Gain staging sets noise floor and headroom.
level: standard
tags: [录音, 话放, 增益]
tags_en: [recording, preamp, gain]
alias: [话放, 前置放大器, 增益级, 增益分配, preamp, gain staging]
links:
  - "[[glossary:preamp]]"
  - "[[glossary:gain]]"
  - "[[glossary:headroom]]"
  - "[[glossary:noise-floor]]"
instances:
  - mutopia-001541 | 尼龙弦吉他输出低，增益不足时底噪最先暴露
  - atepp-001319 | 钢琴弱奏段多，适合用最强与最弱段设定峰值
  - groove-000010 | 鼓组瞬态强，可听增益过高时低频先糊
sources:
  - Ballou, Handbook for Sound Engineers, 5th ed., console gain and noise chapters
  - AES recommended practice for professional audio, level and interconnection terminology
updated: 2026-10-28
---

::: zh
## 问题

话筒出来的信号只有几毫伏，直接进转换器几乎等于没有声音。话放要把它抬到线路电平。抬多少、在哪里抬，决定了底噪、余量和音色，而不只是音量。

## 信号链

话筒 → 话放 → 转换器 → 工作站。话放通常提供 40 至 60 dB 增益，有的还有衰减垫与阻抗选择。模拟段要留余量，数字段峰值落在 -12 至 -6 dBFS。先保证模拟段不削波，再让转换器拿到足够电平。

## 摆位与参数

大声源先按衰减垫，再开 48V，最后慢慢加增益。用演奏中最强的一段设峰值，不要用弱奏设，也不要用推子补。需要更厚的低频时，先试距离与指向，不要先换话放。

```audiolab
{"type":"instrument","gm":"Acoustic Guitar (nylon)","synth":"plucked","phrase":["E3","A3","C4","E4"],"label":"低输出乐器的增益余量","label_en":"Headroom on a low-output instrument","hint":"先听合成近似，再听 GM 采样，留意音头是否被压住","hint_en":"Compare synth and GM sample, listening for a compressed attack"}
```

## 听什么

把增益从低往高推，听底噪与房间声是否同时变大；接近削波时，低频通常先糊。对比同一段话在两种增益下的瞬态，听字头是否还在。

## 常见误解

- **增益和音量是一回事** → 增益在模拟段，推子在数字段，两者影响的噪声不同。
- **数字表到 0 才够响** → 0 dBFS 是上限，不是目标。
- **话放染色一定好听** → 染色是选择，不是保证。
:::

::: en
## The problem

A microphone delivers only a few millivolts; plugged straight into a converter, it gives almost nothing. The preamp raises that signal to line level. How much gain you add, and where, sets the noise floor, the headroom and the tone, not just the loudness.

## Signal chain

Microphone → preamp → converter → workstation. A preamp usually offers 40 to 60 dB, sometimes with a pad and an impedance switch. Leave headroom in the analogue stage, and aim for peaks between -12 and -6 dBFS in the digital stage. Keep the analogue stage clean before asking the converter for more level.

## Placement and settings

For a loud source, engage the pad first, then 48 V, then raise gain slowly. Set the peak from the loudest passage, not the quietest, and do not fix it with a fader. If you want more low-end weight, try distance and polar pattern before changing the preamp.

```audiolab
{"type": "instrument", "gm": "Acoustic Guitar (nylon)", "synth": "plucked", "phrase": ["E3", "A3", "C4", "E4"], "label": "Headroom on a low-output instrument", "label_en": "Headroom on a low-output instrument", "hint": "先听合成近似，再听 GM 采样，留意音头是否被压住", "hint_en": "Compare synth and GM sample, listening for a compressed attack"}
```

## What to listen for

Raise gain from low to high and listen for hiss and room sound rising together. As clipping approaches, the low end usually blurs first. Compare the attack of the same phrase at two gain settings and hear whether it survives.

## Common misconceptions

- **Gain and volume are the same** → gain lives in the analogue stage, the fader in the digital stage, and they affect noise differently.
- **The meter must reach 0** → 0 dBFS is a ceiling, not a target.
- **Preamp colour always sounds better** → colour is a choice, not a guarantee.
:::
