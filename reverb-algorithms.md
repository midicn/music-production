---
id: reverb-algorithms
site: prod
cat: A7
title: 混响算法与卷积
title_en: Reverb Algorithms and Convolution
summary: 房间、厅堂、板式与弹簧各自的声音特征，卷积又补上了什么。
summary_en: How room, hall, plate and spring reverbs differ, and where convolution fits among them.
level: standard
tags: [效果器, 混响, 空间, 听感]
tags_en: [effects, reverb, space, listening]
alias: [混响, 混响算法, 房间混响, 厅堂, 板式, 弹簧, 卷积混响, reverb, convolution]
links:
  - "[[glossary:reverb]]"
  - "[[glossary:bus]]"
  - "[[instrument:organ]]"
instances:
  - cyberhymnal-008348 | 教堂管风琴的和弦尾音长，房间与厅堂的差别一听便知
  - pdmx-000070 | 巴伯《弦乐慢板》持续音多，板式的密度与厅堂的扩散容易对比
  - mutopia-001413 | 萨蒂《裸体歌舞》第三首留白多，混响尾巴不再被音符遮住
sources:
  - Välimäki, Parker and Savioja, Fifty Years of Artificial Reverberation, IEEE TASLP 2012.
  - Udo Zölzer, DAFX.
updated: 2026-10-28
---

::: zh
## 为什么会用到它

「加一点混响」这句话无法执行。房间、厅堂、板式、弹簧与卷积给出的早期反射和密度完全不同，选错类型，参数再细也救不回来。

## 背后的机制

算法混响用延迟线与反馈堆出密度，全通滤波器负责扩散。房间的早期反射近而清楚，厅堂的延迟更长、低频拖得更久，板式密度高、高频亮，弹簧带金属色的色散。卷积混响调用真实空间的脉冲响应，空间可信，可调性却小。

## 数值怎么变成声音

衰减时间决定尾巴长短，尺寸更像空间体积。阻尼让高频先死，混响随之变暗；扩散低时能听出个别反射，像一次拍手。大厅衰减 2–4 秒适合铺底，板式 1–2 秒适合军鼓，弹簧 1 秒左右带明显音高感。

## 耳朵要抓的点

拍一次手，比较房间与厅堂的尾巴。在军鼓上换板式，变化的不只是长度，还有密度。把弹簧放在吉他上，尾音会带出金属味。

```audiolab
{"type":"instrument","gm":"Church Organ","synth":"blown","phrase":["C3","G3","C4","E4"],"label":"管风琴和弦","label_en":"Organ chord","hint":"先听干声，再想象厅堂与板式的尾巴","hint_en":"Hear it dry, then imagine hall and plate tails"}
```

## 容易弄错的

以为衰减越长空间越大；用混响掩盖音准问题；认为卷积一定比算法真实。
:::

::: en
## Why reach for it

Add some reverb cannot be executed. Room, hall, plate, spring and convolution differ in early reflections and density, and the wrong type cannot be rescued by fine settings.

## The mechanism

Algorithmic reverbs build density from delay lines and feedback, with all-pass filters spreading the sound. A room has close, clear early reflections; a hall has longer delays and a longer low end; a plate is dense and bright; a spring carries a metallic dispersion. Convolution calls an impulse response of a real space, credible but less adjustable.

## From numbers to sound

Decay sets tail length, while size suggests volume. Damping lets highs die first and darkens the tail; low diffusion exposes individual reflections, like a hand clap. A two to four second hall suits backgrounds, a one to two second plate suits a snare, and a spring around one second adds audible pitch.

## What the ear should catch

Clap once and compare a room with a hall. Swap a plate onto a snare and hear density change, not only length. Put a spring on guitar and the tail turns metallic.

```audiolab
{"type": "instrument", "gm": "Church Organ", "synth": "blown", "phrase": ["C3", "G3", "C4", "E4"], "label": "Organ chord", "label_en": "Organ chord", "hint": "先听干声，再想象厅堂与板式的尾巴", "hint_en": "Hear it dry, then imagine hall and plate tails"}
```

## Easy to get wrong

That longer decay means a bigger space; that reverb hides tuning problems; that convolution is always more real than an algorithm.
:::
