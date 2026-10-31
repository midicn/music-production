---
id: recording-chain
site: prod
cat: A4
title: 录音链导论
title_en: The Recording Chain
summary: 从声源到文件，录音链的每一环都在改变声音，先看懂顺序再动手
summary_en: Every stage from source to file changes the sound. Learn the order before you touch a knob.
level: standard
tags: [录音, 信号链, 入门]
tags_en: [recording, signal chain, basics]
alias: [录音链, 录音流程, 信号流程, recording chain, signal chain]
links:
  - "[[glossary:gain-staging]]"
  - "[[glossary:microphone]]"
  - "[[instrument:piano]]"
instances:
  - atepp-003869 | 钢琴独奏动态范围大，最容易听出链上哪一环先失真
  - openscore-000008 | 人声与钢琴同录，可对照两种声源在同一条链上的电平差
  - mutopia-000497 | 管弦乐强奏段多，适合检查整条链的余量
sources:
  - Ballou, Handbook for Sound Engineers, 5th ed., signal flow and recording chapters
  - AES recommended practice for professional audio, level and interconnection terminology
updated: 2026-10-28
---

::: zh
## 问题

录音里最难改的不是音色，而是空间与噪声。同一支话筒，在沙发上录和在空房间里录，结果像两支不同的话筒。原因往往不在某一个设备，而在整条链的每一环都在给声音加东西。

## 信号链

声音先经过房间，再被话筒换成电压，电压经话筒线送到话放，抬到线路电平，最后由模数转换器变成样本写进硬盘。顺序不能颠倒。话筒输出只有几毫伏，话放要把它放大几十倍，前面任何噪声都会一起被放大。录音前先确认每一环都通，再谈音色。

## 摆位与参数

先定距离，它决定直达声与房间声的比例；再定高度与角度，避开话筒轴向最亮的高频和地面反射；最后定增益，让演奏最强处落在 -12 至 -6 dBFS。48V 只给需要它的电容话筒，铝带话筒先查说明书。

```audiolab
{"type":"instrument","gm":"Acoustic Grand Piano","synth":"struck","phrase":["C3","G3","C4","E4"],"label":"同一条链上的钢琴","label_en":"A piano at the start of the chain","hint":"先听合成近似，再听 GM 采样，注意音头与尾音","hint_en":"Compare the synthetic approximation with the GM sample, listening to attack and tail"}
```

## 听什么

录一段说话或拍手，回放时听三件事：尾巴是否干净、齿音是否刺、底噪是否随增益一起变大。再把话筒移动十厘米重录，比较低频厚度与声像稳定度。

## 常见误解

- **换一支贵话筒就能救房间** → 房间的反射与驻波仍会进话筒，先处理房间。
- **增益越大越专业** → 增益只解决电平，不解决噪声与失真。
- **链上每一环都要加处理** → 录音阶段的目标是干净，不是完成混音。
:::

::: en
## The problem

What is hardest to fix is rarely timbre but space and noise. The same microphone on a sofa and in an empty room can sound like two different models. Every stage of the chain adds something.

## Signal chain

Sound passes through the room; the microphone turns pressure into a tiny voltage; the preamp raises it to line level; the converter writes samples to disk. A microphone output is only a few millivolts, so the preamp amplifies any noise in front of it. Check that every stage passes signal before chasing tone.

## Placement and settings

Set distance first, because it fixes the direct-to-room ratio. Then set height and angle to avoid the brightest on-axis high end and the floor reflection. Set gain last so the loudest passage peaks between -12 and -6 dBFS. Apply 48 V only to condenser microphones that need it, and check the manual before using it on a ribbon.

```audiolab
{"type": "instrument", "gm": "Acoustic Grand Piano", "synth": "struck", "phrase": ["C3", "G3", "C4", "E4"], "label": "A piano at the start of the chain", "label_en": "A piano at the start of the chain", "hint": "先听合成近似，再听 GM 采样，注意音头与尾音", "hint_en": "Compare the synthetic approximation with the GM sample, listening to attack and tail"}
```

## What to listen for

Record speech or hand claps and listen for a clean tail, harsh sibilance, and hiss that rises with gain. Move the microphone ten centimetres and record again, comparing low-end weight and image stability.

## Common misconceptions

- **A more expensive microphone fixes a bad room** → reflections and standing waves still reach the capsule, so treat the room first.
- **More gain sounds more professional** → gain solves level, not noise or distortion.
- **Every stage needs processing** → the goal of tracking is a clean capture, not a finished mix.
:::
