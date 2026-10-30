---
id: sound-as-vibration
site: prod
cat: A5
title: 声音的物理性
title_en: What Sound Is
summary: 声音是介质中的压强波动，理解它才谈得上处理房间与监听。
summary_en: Sound is a pressure wave in a medium; separating source, room and ear is the first step in monitoring.
level: standard
tags: [声学, 声波, 压强, 介质, 监听基础]
tags_en: [acoustics, sound wave, pressure, medium, monitoring basics]
alias: [声音, 声波, 物理声学, sound, acoustics, vibration]
links:
  - "[[glossary:room-mode]]"
  - "[[glossary:monitoring]]"
  - "[[instrument:piano]]"
instances:
  - giantmidi-000171 | 管风琴前奏曲的钢琴改编，持续音与低音声部适合分辨音头、余响与房间反射（C1）
  - essen-000191 | 单声部民歌《高山调》，素材简单，适合先听清声源本身的振动（C1）
  - pdmx-000237 | 钢琴与低音的多轨爵士，用来对比单声源与合奏在房间里呈现的差别（C1）
sources:
  - Everest, F. Alton，Master Handbook of Acoustics（McGraw-Hill）— 声学基础与房间章节核对，未引用
  - Howard, David M. & Angus, Jamie，Acoustics and Psychoacoustics（Focal Press）— 听觉与频率章节核对，未引用
updated: 2026-10-28
---

::: zh
## 问题
我们常说「声音好听」，却很少分清是哪一环在发声。房间、话筒、音箱和耳朵都在改写同一个振动；不先拆开，调整只能靠猜。

## 物理或房间
声音是弹性介质中的压强扰动。声源推动空气，空气不随波跑到耳边，只在原位压缩与稀疏。20 °C 空气中声速约 343 米每秒；频率决定振动次数，振幅决定压强变化。没有介质就没有声音。

## 做法与判断
先做单变量测试：用拍手、扫频或独奏，依次改变声源位置、听音位置和音量，每次只动一项。判断标准不是更响，而是同一件事是否更清楚：低频收得住、中频不被掩蔽、高频不刺耳。记下可复现的位置与频率。

## 听什么
在房间里拍一次手，听直达声与反射声的间隔；再持续发一个元音，感受胸腔与头骨的传导。独奏一段旋律，注意音头、余响和噪声各占多少。换到耳机重复，差异就是房间与双耳加进来的部分。

## 常见误解
声音不是空气从声源流到耳朵，而是压强波动。分贝不是音量旋钮刻度，0 dB 也不等于无声。采样点不会被听成台阶，真正要担心的是混叠、削波与监听环境。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C2","C4","G4","C5"],"label":"从低到高听同一件乐器的振动","label_en":"One instrument, low to high","hint":"注意低音的音头与余响更长，高音更快衰减；这不是音量变化，而是频率与乐器共鸣的差别。","hint_en":"Notice the longer attack and ring of the low notes; the high notes decay faster. This is frequency and resonance, not level."}
```
:::

::: en
## The problem
A good sound is rarely one thing. Room, microphone, speaker and ear all rewrite the same vibration; separate them or adjustments become guesswork.

## Physics or room
Sound is a pressure disturbance in an elastic medium. A source pushes air; the air oscillates in place rather than travelling to your ear. At 20 °C sound moves at about 343 m/s. Frequency sets cycles per second, amplitude the size of the pressure change. No medium, no sound.

## Practice and judgement
Run one-variable tests. With a clap, sweep or solo, change source position, listening position and level one at a time. Judge clarity, not loudness: does the low end hold, is the midrange masked, is the top harsh? Note what can be repeated.

## What to listen for
Clap once and hear the gap between direct sound and reflections. Sustain a vowel and feel conduction through chest and skull. Play a solo line and separate attack, tail and noise. Repeat on headphones.

## Common misunderstandings
Sound is a pressure wave, not air flowing to your ear. Decibels are ratios, and 0 dB is not silence. Sample steps are not heard as stairs; aliasing, clipping and the room are the real risks.

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C2","C4","G4","C5"],"label":"One instrument, low to high","label_en":"One instrument, low to high","hint":"Notice the longer attack and ring of the low notes; the high notes decay faster. This is frequency and resonance, not level.","hint_en":"Notice the longer attack and ring of the low notes; the high notes decay faster. This is frequency and resonance, not level."}
```
:::
