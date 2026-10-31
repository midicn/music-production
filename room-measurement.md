---
id: room-measurement
site: prod
cat: A5
title: 房间测量
title_en: Measuring a Room
summary: 一支测量麦加一段扫频，先看清峰谷与衰减，再决定买什么。
summary_en: One measurement mic and a sweep show the peaks, nulls and decay before any money goes on treatment.
level: standard
tags: [房间测量, 扫频, 频响, 混响时间, 测量麦克风]
tags_en: [room measurement, sweep, frequency response, reverberation time, measurement microphone]
alias: [房间测量, 声学测量, 扫频测量, room measurement, REW]
order: 396
links:
  - "[[glossary:room-mode]]"
  - "[[glossary:reference-monitor]]"
  - "[[glossary:absorption]]"
  - "[[glossary:monitoring]]"
instances:
  - cyberhymnal-000785 | 持续和弦与停顿清楚，测量前后可对照房间尾巴的变化（C1）
  - atepp-000369 | 独奏钢琴断句明确，适合验证衰减时间是否被处理改变（C1）
  - pdmx-000801 | 低音提琴低音区连续，用来检查测量得到的谷是否真的听得见（C1）
  - essen-000517 | 单声部民歌，素材干净，适合确认处理后中频没有被吸空（C1）
sources:
  - Everest, F. Alton，Master Handbook of Acoustics（McGraw-Hill）— 房间测量与脉冲响应
  - ISO 3382-2 — 房间混响时间测量方法（标准）
  - Room EQ Wizard，用户指南（厂商文档）— 扫频与瀑布图设置
updated: 2026-10-31
---

::: zh
买陷阱之前先测一次：多数房间的低频问题集中在两三个频率上，凭耳朵猜往往买错尺寸。测量不需要昂贵设备，一支全指向测量麦、一个音频接口和一段扫频就够。

## 工具与信号

用全指向测量麦，加载厂家的校准文件；麦架在听音位、耳高，朝向两只音箱的中间。信号用对数扫频，覆盖二十赫兹到二十千赫兹，长度几秒即可，房间噪声大时多平均几次。测之前关掉空调与风扇，确认接口没有开启任何处理，否则测到的是处理后的结果。

## 四张图看四件事

| 图 | 看什么 | 正常的样子 | 常见问题 |
|---|---|---|---|
| 频响 | 峰与谷的位置 | 低频有几个宽峰，高频缓慢下降 | 深而窄的谷是抵消，不要硬提 |
| 瀑布图 | 衰减随频率 | 低频拖尾不超过几百毫秒 | 某个频率长时间不散 |
| 混响时间 | 各频段衰减 | 各频段接近，低频略长 | 低频明显更长说明吸声不足 |
| 脉冲响应 | 早期反射 | 直达声后紧跟少量反射 | 几毫秒处出现强反射 |

混响时间按 ISO 3382-2 的方法从衰减曲线积分得到。低频段通常比中频长，长出一大截就说明低频吸声不够，而不是均衡没调好。

## 测量流程

先测一只音箱，再测两只同时；先测当前摆位，再挪十厘米复测。每个位置至少测三个点：正中、左右各偏二十厘米。存原始数据，不要只截屏。每轮只改一个变量，否则不知道是哪一步起了作用。

## 读图时容易走偏的地方

单点测量会把某个位置的谷当成房间的谷。平滑设成三分之一倍频程会抹掉窄谷，设成四十八分之一又容易被噪声干扰。门控时间太长会把房间反射算进直达声，太短则低频分辨率不足。测量麦没有校准文件时，高频误差可以到几个分贝。最容易忽略的是：曲线只描述麦所在的那一点，头移动十厘米，结果就变。

## 什么时候不必测

只在一个位置混音、房间已经听过几百小时，测量的用处是确认而不是重新设计，测一次留档即可。以耳机为主的工作流，房间测量解决不了耳机的问题。测量也替代不了试听：图上平直的曲线仍可能听起来发闷，因为时间结构没有被画出来。

```audiolab
{"type":"instrument","gm":"Contrabass","synth":"bowed","phrase":["D1","F1","A1","C2"],"label":"扫频之后，用低音复核","label_en":"After the sweep, confirm with low notes","hint":"测量显示谷的那个音，单独播一遍；听得到才算问题，听不到就只是图上的数字。","hint_en":"Play the note the graph calls a null on its own; if you cannot hear it, it is a number on a chart rather than a problem."}
```
:::

::: en

Most rooms concentrate their low-frequency trouble in two or three places, and guessing by ear usually buys the wrong size of trap. The kit is modest: an omnidirectional measurement mic, an audio interface and a sweep.

## Tools and signal

Use an omni measurement mic with its calibration file, mounted at ear height in the listening position and aimed between the speakers. Feed it a logarithmic sweep from 20 Hz to 20 kHz, a few seconds long, averaging more runs when the room is noisy. Switch off air conditioning and fans first, and make sure no processing is active in the interface, or the measurement describes the processing rather than the room.

## Four plots, four questions

| Plot | What to read | What healthy looks like | Usual trouble |
|---|---|---|---|
| Response | Where peaks and dips sit | A few broad low peaks, a gentle top roll-off | Deep narrow dips are cancellation; do not boost |
| Waterfall | Decay against frequency | Low-frequency tails under a few hundred milliseconds | One frequency that will not fade |
| Reverberation time | Decay per band | Bands close together, bass slightly longer | Much longer bass means too little absorption |
| Impulse | Early reflections | A direct arrival, then a few weak reflections | A strong reflection a few milliseconds late |

Reverberation time comes from integrating the decay curve, following the method in ISO 3382-2. Bass usually decays a little slower than the midrange; a large gap points to insufficient low-frequency absorption, not to a bad EQ setting.

## A repeatable procedure

Measure one speaker, then both. Measure the current layout, then move things ten centimetres and measure again. Take at least three points per position: centre, and twenty centimetres to either side. Keep the raw files rather than screenshots. Change one variable per round, otherwise nothing can be attributed.

## Where reading the graph goes wrong

A single point turns one seat's null into the room's null. Third-octave smoothing hides narrow notches, while forty-eighth-octave smoothing lets noise back in. Too long a gate folds room reflections into the direct sound; too short a gate loses low-frequency resolution. An uncalibrated mic can be several decibels out at the top. The most overlooked point: the curve describes one microphone position, and moving your head ten centimetres changes it.

## When not to measure

If you mix in one spot and have listened in the room for hundreds of hours, a measurement confirms rather than redesigns; take one and file it. In a headphone-first workflow a room measurement cannot answer headphone questions. Nor does it replace listening: a flat curve can still sound dull, because the time structure never appears on the plot.

```audiolab
{"type":"instrument","gm":"Contrabass","synth":"bowed","phrase":["D1","F1","A1","C2"],"label":"After the sweep, confirm with low notes","label_en":"After the sweep, confirm with low notes","hint":"Play the note the graph calls a null on its own; if you cannot hear it, it is a number on a chart rather than a problem.","hint_en":"Play the note the graph calls a null on its own; if you cannot hear it, it is a number on a chart rather than a problem."}
```
:::
