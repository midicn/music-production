---
id: audio-restoration
site: prod
cat: B5
title: 音频修复
title_en: Audio Restoration
summary: 降噪、去嗡、去咔嗒各有代价，修得越狠，原声丢得越多。
summary_en: Noise reduction, hum removal and click repair all cost something; the harder you clean, the more of the original goes.
level: standard
tags: [音频修复, 降噪, 去嗡, 去咔嗒]
tags_en: [restoration, noise reduction, hum removal, click repair]
alias: [降噪, 音频修复, 去噪, restoration, denoise]
links:
  - "[[glossary:sample-rate]]"
  - "[[glossary:bit-depth]]"
  - "[[glossary:timbre]]"
instances:
  - cyberhymnal-000003 | 管风琴MIDI声部，不包含原录音本底或机械声（C1） | Organ MIDI parts without original recording noise or mechanical sounds (C1)
  - thesession-022200 | 传统曲调的音符参照，不记录弓弦摩擦或呼吸（C1） | Traditional-tune notes without recorded bow friction or breathing (C1)
  - atepp-001111 | 钢琴演奏的音符数据，不包含磁带嘶声或踏板机械噪声（C1） | Piano-performance note data without tape hiss or pedal mechanism noise (C1)
sources:
  - "https://www.izotope.com/community/blog/audio-artifacts"
  - 谱减法与频域降噪的原理，参考音频修复公开资料。
  - 去嗡与去咔嗒的处理顺序；录音修复惯例是主要依据。
updated: 2026-11-02
---

::: zh
## 难点在哪

老录音里混着嘶声、嗡声、咔嗒与房间噪声。修复的目标不是把噪声彻底消灭，而是让它在听感上退到背景，同时保住原声的瞬态与音色。修过头的声音会发闷、发水，像隔着一层布。

## 原因

修复方法因问题而异：去嗡可跟踪窄带基频与谐波，去点击可检测局部异常并插值，宽带降噪可利用噪声统计或学习模型，频谱修复可按时间频率选区处理。不是所有算法都简单地从原频谱减掉一份噪声。原始信息与噪声严重重叠时，处理通常存在残留和误伤的取舍。

## 怎么绕过去

保留原始文件，选一个代表性片段设参数。先处理会干扰后续分析的明显事件是否更合适，要实际比较；没有适用于所有录音的固定顺序。需要噪声样本的工具应选真实底噪，不要把弱音当噪声。每一步都匹配电平做旁通，并监听差分信号，检查是否移除了有用声音。

## 听这几处

用实际录音中的一段持续音、一处瞬态和一段停顿分别检查：噪声是否下降，原音的起落是否保留，是否新增颤动、金属声或断裂。既检查独奏片段，也回到完整节目判断修复是否分散注意力。

```audiolab
{"type":"instrument","gm":"Violin","synth":"bowed","phrase":["G4","B4","D5","G5","D5","B4","G4","D4"],"label":"弦乐音色参照","label_en":"String-timbre reference","hint":"本段只播放合成音色，不含可去除的录音底噪。请用实际带噪音频检查修复后音乐细节是否保留。","hint_en":"This block plays synthesis without recorded background noise to remove. Check detail retention with actual noisy audio."}
```
:::

::: en
## Where it gets hard

Old recordings carry hiss, hum, clicks and room noise. Restoration does not aim to erase noise completely but to push it behind the music while keeping transients and timbre intact. Over-cleaned audio sounds dull or watery, as if heard through cloth.

## The reason

Restoration methods differ: de-hum may track narrow fundamentals and harmonics, de-click may detect local anomalies and interpolate, denoising may use noise statistics or learned models, and spectral repair can target time-frequency regions. Not every algorithm subtracts one noise spectrum. When unwanted and wanted material overlap strongly, residual noise and damage require a trade-off.

## How to get around it

Preserve the original and set parameters on a representative excerpt. Test whether obvious events should be removed before later analysis; no single order suits all recordings. Where a noise sample is required, use genuine background rather than quiet wanted sound. Match levels for bypass comparisons and listen to the removed signal for lost content.

## Listen to these

Check a sustained sound, a transient and a pause in the actual recording: has noise fallen, does the wanted envelope remain, and are there new modulation, metallic or discontinuity artifacts? Inspect excerpts and the complete programme to judge whether the repair distracts.

```audiolab
{"type":"instrument","gm":"Violin","synth":"bowed","phrase":["G4","B4","D5","G5","D5","B4","G4","D4"],"label":"String-timbre reference","label_en":"String-timbre reference","hint":"This block plays synthesis without recorded background noise to remove. Check detail retention with actual noisy audio.","hint_en":"This block plays synthesis without recorded background noise to remove. Check detail retention with actual noisy audio."}
```
:::
