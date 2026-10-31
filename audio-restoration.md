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
  - cyberhymnal-000003 | 早期赞美诗的管风琴录音，本底噪声与机械声混在长音里（C1）
  - thesession-022200 | 爱尔兰传统曲调，弓弦摩擦与呼吸声在降噪过度后会变成水声（C1）
  - atepp-001111 | 肖邦早期录音转制，钢琴的踏板噪声与磁带嘶声需要分别处理（C1）
sources:
  - 谱减法与频域降噪的原理，参考音频修复公开资料。
  - 去嗡与去咔嗒的处理顺序；录音修复惯例是主要依据。
updated: 2026-10-28
---

::: zh
## 难点在哪

老录音里混着嘶声、嗡声、咔嗒与房间噪声。修复的目标不是把噪声彻底消灭，而是让它在听感上退到背景，同时保住原声的瞬态与音色。修过头的声音会发闷、发水，像隔着一层布。

## 原因

降噪常用频域谱减法：估计噪声的频谱，从信号里减掉。噪声估计越准，残留越少；估计不准就会连音乐一起减，留下金属味的伪影。去嗡针对 50 或 60 Hz 的电源谐波，用窄带陷波逐个削掉。去咔嗒靠检测瞬态并插值填补。去齿音与去呼吸是另外两类问题，处理顺序错了会把问题放大。所有修复都是在信息丢失与噪声残留之间做交换。

## 怎么绕过去

先清洗再降噪，先处理明显事件再处理本底。噪声采样要选纯噪声段。降噪量从小往大试，找到伪影刚出现的临界点再退一步。低频嗡声用陷波，别用宽带降噪。咔嗒用短窗修复，别把整段一起抹。修复后与原版 A/B，确认瞬态还在。存档时保留未修复版本，修复版另存。

## 听这几处

在赞美诗管风琴的长音里听噪声是否退到背景而音色未变闷，在传统曲调的弓弦上听摩擦声处理后是否变成水声，在早期钢琴录音里听踏板噪声是否被误当成音乐成分。好的修复让人忘记噪声存在，而不是让人注意到修复痕迹。

```audiolab
{"type":"instrument","gm":"Violin","synth":"bowed","phrase":["G4","B4","D5","G5","D5","B4","G4","D4"],"label":"弓弦与噪声的边界","label_en":"Where bow meets noise","hint":"弓毛摩擦与琴身噪声频谱接近，降噪过度时这里最先变水","hint_en":"Bow noise sits close to the string spectrum, so over-cleaning turns it watery here"}
```
:::

::: en
## Where it gets hard

Old recordings carry hiss, hum, clicks and room noise. Restoration does not aim to erase noise completely but to push it behind the music while keeping transients and timbre intact. Over-cleaned audio sounds dull or watery, as if heard through cloth.

## The reason

Noise reduction usually works by spectral subtraction: estimate the noise spectrum and subtract it from the signal. A good estimate leaves little residue; a poor one removes music along with noise and leaves metallic artefacts. Hum removal targets the 50 or 60 Hz mains harmonics with narrow notches. Click repair detects transients and interpolates over them. De-essing and breath removal are different problems, and handling them in the wrong order makes things worse. Every restoration move trades lost information against remaining noise.

## How to get around it

Clean obvious events before reducing the noise floor. Sample noise from a genuinely silent stretch. Increase reduction gradually and back off one step from where artefacts appear. Notch low hum rather than treating it with broadband reduction. Repair clicks with short windows instead of smearing a whole passage. A/B against the original to confirm transients survive. Archive the untreated file and save the restored version separately.

## Listen to these

On the organ's long notes, whether noise recedes without dulling the tone; on the fiddle bow, whether friction turns watery after processing; on the early piano transfer, whether pedal noise is mistaken for music. Good restoration makes you forget the noise; bad restoration makes you notice the repair.

```audiolab
{"type":"instrument","gm":"Violin","synth":"bowed","phrase":["G4","B4","D5","G5","D5","B4","G4","D4"],"label":"Where bow meets noise","label_en":"Where bow meets noise","hint":"Bow noise sits close to the string spectrum, so over-cleaning turns it watery here","hint_en":"Bow noise sits close to the string spectrum, so over-cleaning turns it watery here"}
```
:::
