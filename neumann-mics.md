---
id: neumann-mics
site: prod
cat: C
order: 34
title: Neumann 话筒
title_en: Neumann Microphones
summary: 大振膜电容的行业参照，灵敏度高、底噪低，也因此更挑房间与摆位。
summary_en: The reference large-diaphragm condenser: high sensitivity and low noise, which is exactly why it is fussy about rooms and placement.
level: standard
tags: [话筒, 电容, 人声, 录音]
tags_en: [microphone, condenser, vocals, recording]
alias: [Neumann, 纽曼, U87, U 87, TLM 103, 大振膜]
tool_kind: hardware
tool_vendor: Neumann
tool_form: 硬件
tool_platforms: [不依赖平台]
tool_price: 硬件
tool_jobs: [人声录音, 乐器录音, 配音]
links:
  - "[[glossary:condenser-microphone]]"
  - "[[glossary:microphone]]"
  - "[[instrument:cello]]"
instances:
  - openscore-000007 | 艺术歌曲的人声，大振膜能把气息与咬字一起收住，也把房间一起收进来；这是该工具常见产出的参照，不是该工具的演示
  - musicnet-000020 | 无伴奏大提琴，琴箱的低频与弓毛的细节都要一支低底噪话筒才留得住；这是该工具常见产出的参照，不是该工具的演示
  - giantmidi-007776 | 钢琴变奏曲，两支大振膜做立体声对时要处理相位与房间反射；这是该工具常见产出的参照，不是该工具的演示
  - mutopia-000038 | 合唱作品，主对位置决定整体厚度与空间感，比单支近讲更能听出话筒取向；这是该工具常见产出的参照，不是该工具的演示
sources:
  - 厂商公开的指向性、灵敏度与自噪指标；官方页面是主要依据。
  - 电容话筒的幻象供电与声压余量——依据来自录音惯例。
tool_verified: 2026-10-30
updated: 2026-10-30
---

::: zh
## 能替你做完什么

录一支能直接进混音的主唱人声，不必靠后期堆插件救。用一支大振膜录大提琴或木吉他，近一点就有厚度。给纪录片或有声书做低底噪的旁白，连续录几小时也听不出嘶声。做合奏或合唱的主对，一支就够撑起整体。放在鼓组上方，听到的是整套鼓而不是单个鼓皮。在客厅里也能录出可用的结果，前提是你先处理房间。

## 它怎么工作

电容极头把声压变化换成电压，内置放大电路把信号抬到线路电平，所以它比动圈灵敏得多，话放只需要推一点点。指向性、低切与衰减开关决定它听到多少房间、多少低频、多少强奏余量。变压器版本与无变压器版本的高频与瞬态不同，选型时值得对比，而不是只看型号数字。离轴频响比轴上更影响合奏录音，摆位时要听侧面进来的声音。

## 哪里会坑你

- 灵敏是双向的：空调、电脑风扇、街道噪声都会一起进来，房间不好时它比便宜话筒更暴露。
- 贵不等于万能。某些嗓音用动圈反而更稳，某些乐器用小振膜更准。
- 二手市场仿品多，序列号与包装要核，别只看外壳。
- 需要防震架与防喷网，手持或硬架会把震动录进去。
- 高声压源要开衰减，潮湿环境要防结露，用完放回干燥箱。
- 它不会替你决定距离与角度，摆位错了，贵话筒也只是更清楚地录下错误。

## 换成什么

预算有限，Austrian Audio、Lewitt 或 Audio-Technica 的大振膜能完成大部分活；要更准确的小振膜，DPA 与 Neumann 自家的 KM 系列都值得看。搭配一台干净、增益足够的话放与基本的吸音处理，收益比再换一支更贵的话筒大。

## 先学三件事

先学三件事：距离与近讲效应、指向性与房间声的比例、衰减开关什么时候用。再固定一支话筒练十次摆位。配合读电容话筒、话筒、大提琴三条。

```audiolab
{"type":"instrument","gm":"Cello","synth":"bowed","phrase":["C3","G3","D3","A3","E4","A3","D3","G3"],"label":"大提琴的近讲厚度","label_en":"A cello close up","hint":"听琴箱共鸣与弓毛摩擦，大振膜要留住低频又不糊掉细节","hint_en":"Listen to body resonance and bow noise; a large diaphragm must keep the low end without smearing detail"}
```
:::

::: en
## What it finishes for you

Capture a lead vocal that goes into the mix without a pile of plug-ins rescuing it. Record a cello or an acoustic guitar with weight by placing a large diaphragm close. Deliver low-noise narration for a documentary or audiobook that survives hours of listening. Use one microphone as the main pair for a choir or chamber group, or over a drum kit to hear the whole set. Get a usable result in a living room, provided the room has been dealt with first.

## How it works

The capsule turns pressure into voltage and built-in electronics raise it to line level, so the microphone is far more sensitive than a dynamic and the preamp only needs a little gain. Pattern, low-cut and pad switches decide how much room, how much low end and how much headroom for loud playing you get. Transformer and transformerless versions differ in top end and transient behaviour, which is worth auditioning rather than reading off a model number.

## Where it bites

- Sensitivity cuts both ways. Air conditioning, computer fans and street noise all arrive with the voice, and a poor room is more exposed than with a cheap microphone.
- Expensive is not universal. Some voices sit better on a dynamic, some instruments are more accurate on a small diaphragm.
- The used market carries copies. Check serial numbers and packaging, not just the shell.
- It needs a shock mount and a pop filter. Hand-held or hard-mounted, it records the building.
- Engage the pad on loud sources, guard against condensation, and store it dry.
- It will not choose distance or angle for you. Placed badly, a costly microphone simply records the mistake more clearly.

## What to swap in

On a budget, large diaphragms from Austrian Audio, Lewitt or Audio-Technica cover most work; for a more accurate small diaphragm, look at DPA and Neumann's own KM line. A clean preamp with enough gain and basic absorption will improve results more than another, dearer microphone.

## First three things

Learn distance and proximity effect, how pattern changes the direct-to-room ratio, and when the pad is needed. Then place one microphone ten times and compare. Read the condenser microphone, microphone and cello entries alongside this one.

```audiolab
{"type":"instrument","gm":"Cello","synth":"bowed","phrase":["C3","G3","D3","A3","E4","A3","D3","G3"],"label":"大提琴的近讲厚度","label_en":"A cello close up","hint":"听琴箱共鸣与弓毛摩擦，大振膜要留住低频又不糊掉细节","hint_en":"Listen to body resonance and bow noise; a large diaphragm must keep the low end without smearing detail"}
```
:::
