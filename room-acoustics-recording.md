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
  - mutopia-001411 | 钢琴织体的谱面参照，不是某间房间的拾音 | Piano texture as a scored reference, not a microphone recording of a room
  - cyberhymnal-000828 | 管风琴编制参照；MIDI 音源混响不是原教堂的测量 | Organ instrumentation; MIDI-instrument reverb does not measure the original church
  - m21-000602 | 合唱声部参照，不包含不同话筒摆位的录音 | Choral parts without recordings from different microphone positions
sources:
  - Everest, Master Handbook of Acoustics, room modes and reverberation chapters
  - Ballou, Handbook for Sound Engineers, 5th ed., studio acoustics chapters
updated: 2026-11-02
---

::: zh
## 问题

房间会把它自己的声音写进录音。低频驻波让某些音特别响，早期反射让声像变模糊，尾巴长则让快句糊成一片。换话筒之前，先听房间。

## 信号链

话筒先收到直达声，随后是墙面、地面与天花板的早期反射，最后是混响尾巴。房间模式由尺寸决定，低频在固定频率上堆积。RT60 越长，尾巴越难收，也更难用摆位躲开。

## 摆位与参数

先在房间里移动声源和话筒，录制同一短句，再比较直达声、梳状染色和低频突出的位置。离墙一米不是通用安全线，距离要与房间尺寸、乐器和话筒指向性一起考虑。薄吸音材料主要影响较高频率，低频处理通常需要更厚的结构、足够空气层或专门设计。

```audiolab
{"type":"instrument","gm":"Church Organ","synth":"blown","phrase":["C3","G3","C4","G4"],"label":"音色尾音参照","label_en":"Instrument decay reference","hint":"比较音色的衰减即可。合成音与 GM 音色的差别不是同一房间的声学对照，也不能测出 RT60。","hint_en":"Compare instrument decay only. Synth and GM timbres are not controlled recordings of one room and cannot measure RT60."}
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

Move the source and microphone and record the same short phrase at each position, comparing direct sound, comb filtering and prominent bass notes. One metre from a wall is not a universal safe boundary: room size, instrument and microphone pattern matter. Thin absorbers mainly affect higher frequencies; bass treatment generally requires greater depth, an air gap or a dedicated design.

```audiolab
{"type":"instrument","gm":"Church Organ","synth":"blown","phrase":["C3","G3","C4","G4"],"label":"Instrument decay reference","label_en":"Instrument decay reference","hint":"Compare instrument decay only. Synth and GM timbres are not controlled recordings of one room and cannot measure RT60.","hint_en":"Compare instrument decay only. Synth and GM timbres are not controlled recordings of one room and cannot measure RT60."}
```

## What to listen for

Clap and listen for a flutter echo, then speak and listen for low-frequency boom. Record a sustained note and check whether the tail is even or one pitch jumps out.

## Common misconceptions

- **Small rooms need no treatment** → their low-frequency problems are more concentrated.
- **Covering every surface with foam is enough** → too much absorption deadens the sound, and the lows still need dedicated treatment.
- **A carpet fixes the low end** → carpet absorbs mostly high frequencies.
:::
