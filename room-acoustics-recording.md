---
id: room-acoustics-recording
site: prod
cat: A4
title: 房间声学对录音的影响
title_en: How the Room Shapes a Recording
summary: 房间的低频驻波与反射会写进录音，摆位与处理比换话筒更有效
summary_en: Standing waves and reflections are printed into the recording. Placement and treatment matter more than a new mic.
level: standard
tags: [录音, 声学, 房间]
tags_en: [recording, acoustics, room]
alias: [房间声学, 录音房间, 驻波, 早期反射, 混响时间, room acoustics, standing wave]
links:
  - "[[glossary:room-mode]]"
  - "[[glossary:room-treatment]]"
  - "[[glossary:reverb]]"
  - "[[instrument:organ]]"
instances:
  - mutopia-001411 | 稀疏织体加踏板，房间的尾巴与驻波最容易暴露
  - cyberhymnal-000828 | 管风琴在教堂空间里，混响时间直接写在声音上
  - m21-000602 | 合唱与房间声比例清楚，适合比较不同摆位
sources:
  - Everest, Master Handbook of Acoustics, room modes and reverberation chapters
  - Ballou, Handbook for Sound Engineers, 5th ed., studio acoustics chapters
updated: 2026-10-28
---

::: zh
## 问题

房间会把它自己的声音写进录音。低频驻波让某些音特别响，早期反射让声像变模糊，尾巴长则让快句糊成一片。换话筒之前，先听房间。

## 信号链

话筒先收到直达声，随后是墙面、地面与天花板的早期反射，最后是混响尾巴。房间模式由尺寸决定，低频在固定频率上堆积。RT60 越长，尾巴越难收，也更难用摆位躲开。

## 摆位与参数

话筒离墙至少 1 米，避开房间中线与角落。第一反射点做吸音，角落放低频陷阱。小房间用近场拾音加短混响，大房间可以把话筒退远，利用自然空间。

```audiolab
{"type":"instrument","gm":"Church Organ","synth":"blown","phrase":["C3","G3","C4","G4"],"label":"房间也是乐器的一部分","label_en":"The room is part of the instrument","hint":"先听合成近似，再听 GM 采样，注意尾音的长度","hint_en":"Compare synth and GM sample, listening to the length of the tail"}
```

## 听什么

拍手听是否有颤动回声，说话听低频是否嗡嗡。录一段持续音，回放时听尾巴是否均匀，有没有某个音特别突出。

## 常见误解

- **小房间不用处理** → 小房间的低频问题更集中。
- **吸音棉贴满就好** → 过度吸音会让声音发闷，低频仍需专门处理。
- **地毯能解决低频** → 地毯只吸收高频。
:::

::: en
## The problem

The room writes its own sound into the recording. Standing waves make some notes louder, early reflections blur the image, and a long tail smears fast passages. Listen to the room before changing the microphone.

## Signal chain

The microphone hears direct sound first, then early reflections from walls, floor and ceiling, then the reverberant tail. Room modes follow the dimensions, and low frequencies pile up at fixed notes. A longer RT60 is harder to control and harder to escape by placement alone.

## Placement and settings

Keep the microphone at least 1 metre from a wall and away from the room centre line and corners. Treat the first reflection points and put bass traps in the corners. In a small room, work close with a short reverb; in a large room, move the microphone back and use the natural space.

```audiolab
{"type": "instrument", "gm": "Church Organ", "synth": "blown", "phrase": ["C3", "G3", "C4", "G4"], "label": "The room is part of the instrument", "label_en": "The room is part of the instrument", "hint": "先听合成近似，再听 GM 采样，注意尾音的长度", "hint_en": "Compare synth and GM sample, listening to the length of the tail"}
```

## What to listen for

Clap and listen for a flutter echo, then speak and listen for low-frequency boom. Record a sustained note and check whether the tail is even or one pitch jumps out.

## Common misconceptions

- **Small rooms need no treatment** → their low-frequency problems are more concentrated.
- **Covering every surface with foam is enough** → too much absorption deadens the sound, and the lows still need dedicated treatment.
- **A carpet fixes the low end** → carpet absorbs mostly high frequencies.
:::
