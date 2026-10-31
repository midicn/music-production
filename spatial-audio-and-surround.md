---
id: spatial-audio-and-surround
site: prod
cat: A9
title: 空间音频与环绕声
title_en: Spatial Audio and Surround
summary: 环绕先决定听者站在哪，再决定声音放在哪。
summary_en: Surround first decides where the listener stands, then where each sound sits.
level: standard
tags: [配乐, 空间音频, 环绕声, 声床, 下混]
tags_en: [scoring, spatial audio, surround, beds, downmix]
alias: [空间音频, 环绕声, 沉浸声, spatial audio, surround sound]
links:
  - "[[glossary:stereo-technique]]"
  - "[[glossary:panning]]"
  - "[[glossary:phase]]"
  - "[[period:contemporary]]"
instances:
  - oga-000009 | 海浪声与弦乐、小号同场，环境声床与前景的分层很清楚
  - oga-000021 | 弦乐、竖琴与定音鼓拉开距离，可听洞穴混响怎样造深度
  - pdmx-000269 | 管弦乐各声部有明确座位，适合判断前后层次与厅堂感
sources:
  - Holman, Tomlinson，Sound for Film and Television（Focal Press）— 环绕声与下混章节核对，未引用
  - Rumsey, Francis，Spatial Audio（Focal Press）— 双耳渲染与距离感章节核对，未引用
updated: 2026-10-28
---

::: zh
## 难在哪
环绕声不是把乐器分到四周。它先要回答听者站在哪里，再决定每个声音放在哪一层，否则只是更宽的立体声。

## 为什么这样有效
影院与游戏常用声床加对象的结构。声床负责环境与音乐，对象负责需要定位的事件。五点一声道里，前置负责对白与主音乐，侧后置负责环境，低频通道只放二十到八十赫兹。双耳渲染用头相关传输函数，把声道折叠成两只耳朵。距离感来自直达与混响比、高频吸收与早期反射，而不是音量。

## 参数与取舍
对白与主旋律永远在前。环境声放后与顶，移动要平滑，避免跳过扬声器。低频通道不做主要低频，否则下混会失衡。做完必须检查立体声与单声道下混，确认深度与对白仍然成立。顶部声道用来做高度，不要拿来重复前排。

## 耳朵要抓的点
前后层次是否清楚，移动是否连续，下混后是否还有深度，对白是否被环境盖住。

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C3","G3","E4","B4","G4","C3"],"label":"跨越音区的弦乐","label_en":"Strings spanning the registers","hint":"先听高低音的距离，再想象同一素材放在前方与后方时远近怎样变化","hint_en":"Hear the distance between low and high notes, then imagine the same material placed front and rear"}
```

## 容易弄错的
以为声道越多越好。没有内容设计，更多声道只会更乱。环绕也不等于声音从后面来，后方的主要职责是环境与包围感。
:::

::: en
## Where it gets hard
Surround is not about spreading instruments around the room. It first answers where the listener stands, then decides which layer each sound occupies; otherwise it is only wider stereo.

## Why it works
Film and games commonly use beds plus objects. Beds carry ambience and music; objects carry events that need a location. In 5.1, the front carries dialogue and main music, the sides and rear carry ambience, and the low-frequency channel takes only twenty to eighty hertz. Binaural rendering folds the channels into two ears with head-related transfer functions. Distance comes from the direct-to-reverb ratio, high-frequency absorption and early reflections, not from level.

## Settings and trade-offs
Dialogue and lead melody stay in front. Ambience goes to the rear and overhead, and movement must be smooth rather than jumping between speakers. Do not put the main bass in the LFE, or the downmix loses balance. Always check stereo and mono downmixes, confirming that depth and dialogue survive. Overhead channels create height; do not use them to duplicate the front.

## What the ear catches
Whether front-to-back layers are clear, whether movement is continuous, whether depth survives the downmix, and whether dialogue is covered by ambience.

```audiolab
{"type": "instrument", "gm": "String Ensemble 1", "synth": "bowed", "phrase": ["C3", "G3", "E4", "B4", "G4", "C3"], "label": "Strings spanning the registers", "label_en": "Strings spanning the registers", "hint": "先听高低音的距离，再想象同一素材放在前方与后方时远近怎样变化", "hint_en": "Hear the distance between low and high notes, then imagine the same material placed front and rear"}
```

## Common misconceptions
That more channels are better. Without content design, extra channels only add confusion. Surround also does not mean sound from behind; the rear exists mainly for ambience and envelopment.
:::
