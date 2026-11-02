---
id: polar-patterns
site: prod
cat: A4
title: 指向性
title_en: Polar Patterns
summary: 指向性决定话筒对哪个方向敏感，也决定近讲效应与串音
summary_en: A microphone's polar pattern sets what it hears from each direction, and with it bleed and proximity effect.
level: standard
tags: [录音, 话筒, 指向性]
tags_en: [recording, microphone, polar pattern]
alias: [指向性, 拾音模式, 心形, 全指向, 8字形, polar pattern, cardioid]
links:
  - "[[glossary:polar-pattern]]"
  - "[[glossary:microphone]]"
  - "[[instrument:drum-kit]]"
instances:
  - m21-000602 | 合唱织体可帮助规划阵列与声部布局，指向性比较需实际话筒录音 | Choral texture can help plan arrays and part layout; polar-pattern comparison needs real mic recordings
  - openscore-000008 | 声乐素材可作练习曲目，近讲效应需在同一实际话筒改变距离后录制 | Vocal material supplies a practice piece; record one actual mic at different distances to test proximity effect
  - groove-000003 | 鼓组可作摆位练习的节奏参考，后方抑制需实际话筒及离轴声源验证 | Drums provide a rhythmic reference for placement; verify rear rejection with real microphones and off-axis sources
sources:
  - "https://pubs.shure.com/view/guide/KSM313/en-US.pdf"
  - "https://www.shure.com/en-US/insights/microphone-directionality-polar-pattern-basics"
  - Eargle, The Microphone Book, 3rd ed., directivity and proximity chapters
  - Olson, Acoustical Engineering, pressure-gradient microphone theory
updated: 2026-11-02
---

::: zh
## 问题

指向性是话筒对入射方向的响应，不等于声像位置。它影响目标声、串音与房间反射的比例，通常还随频率变化。选型和摆位时应查看具体型号的指向图，再验证实际空间中的结果。

## 信号链

指向图描述不同角度、频率下的灵敏度。理想心形在后方抑制最强，全指向在各方向响应接近；8字形的前后两瓣灵敏，左右侧面接近零点，前后输出极性相反。实际结构和频率响应因型号而异，可切换指向的话筒也不只有一种实现。

## 摆位与参数

先查目标型号的分频段指向图，把需要的声源对准合适方向，把不想收的声音尽量放在抑制方向。用8字形隔离旁边的声源时应利用侧面零点，不能把其后瓣当作隔离区。近讲效应、声源距离与房间反射要一起检查。

```audiolab
{"type":"instrument","drum":"38","synth":"perc","phrase":["38","42","36"],"label":"鼓点音色参照","label_en":"A drum-timbre reference","hint":"这里比较合成与采样音色；要测指向性，需用实际话筒固定距离、旋转声源角度并匹配录音增益。","hint_en":"This compares synthetic and sampled timbres. To test directionality, use a real mic at fixed distance, vary source angle and match recording gain."}
```

## 听什么

绕话筒走一圈拍手，听音量与音色如何变化；再靠近说话，听低频是否变厚。把心形转到 180 度，确认零点是否真的安静。

## 常见误解

- 理想零点不保证实际房间中完全安静，反射与分频段响应仍会影响收音
- 理想压力式全指向没有梯度式近讲效应，但仍可能受声场和结构影响
- 改变角度既可能改变电平，也可能改变音色
- 全指向、心形和8字形都需按具体型号与任务选择
:::

::: en
## The problem

Directivity describes response to arrival direction, not stereo position. It affects the balance of wanted sound, bleed and room reflections, and usually varies with frequency. Consult the actual model’s polar plots and verify the result in the room.

## Signal chain

Polar patterns describe sensitivity by angle and frequency. An ideal cardioid rejects most strongly behind, while an omni is similar around the capsule. A figure-eight has sensitive front and rear lobes, side nulls and opposite front/rear polarity. Actual structures and responses vary by model; switchable patterns have more than one implementation.

## Placement and settings

Consult frequency-specific polar plots for the actual model. Aim wanted sources at the appropriate direction and unwanted sound toward rejection. Use a figure-eight’s side nulls for isolation, not its sensitive rear lobe. Check proximity effect, distance and room reflections together.

```audiolab
{"type":"instrument","drum":"38","synth":"perc","phrase":["38","42","36"],"label":"A drum-timbre reference","label_en":"A drum-timbre reference","hint":"This compares synthetic and sampled timbres. To test directionality, use a real mic at fixed distance, vary source angle and match recording gain.","hint_en":"This compares synthetic and sampled timbres. To test directionality, use a real mic at fixed distance, vary source angle and match recording gain."}
```

## What to listen for

Walk a full circle around the microphone while clapping, and hear how level and tone change. Move in close and speak, listening for a thicker low end. Turn the cardioid to 180 degrees and check that the null is quiet.

## Common misconceptions

- An ideal null does not guarantee silence in a real room; reflections and frequency-dependent response still matter
- An ideal pressure omni lacks gradient proximity effect, while field and construction can still affect response
- Changing angle can alter both level and timbre
- Choose omni, cardioid or figure-eight for the exact model and task
:::
