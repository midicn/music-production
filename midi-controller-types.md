---
id: midi-controller-types
site: prod
cat: B1
title: MIDI 控制器类型
title_en: MIDI Controller Types
summary: CC 按用途分连续、开关、库选择与参数四类，编号决定含义。
summary_en: CC falls into continuous, switch, bank and parameter families, and the number fixes the meaning.
level: standard
tags: [MIDI, CC, 控制器, RPN]
tags_en: [MIDI, CC, controller, RPN]
alias: [控制器类型, CC 类型, 连续控制器, 开关控制器]
links:
  - "[[glossary:midi-protocol]]"
  - "[[instrument:midi-controller]]"
  - "[[glossary:velocity]]"
instances:
  - musicnet-000301 | 含 19 种 CC，其中 CC11 有 8444 条，另有库选择与 CC121 控制器复位 | Contains 19 CC types including 8444 CC11 events, plus bank selection and CC121 controller reset
  - oga-000003 | 含 11 种 CC，CC101、100、6、38 用于 RPN 参数设置 | Contains 11 CC types; CC101, 100, 6 and 38 provide RPN parameter setting
  - groove-000507 | 含 14133 条 CC4 踏板事件，以及 CC16、17、18 控制数据；实际映射依音源而定 | Contains 14133 CC4 pedal events plus CC16, 17 and 18 data; their effect depends on the receiver
sources:
  - "https://midi.org/midi-1-0-control-change-messages"
  - MIDI 1.0 规范的控制器编号与 RPN、NRPN 机制，参考 MMA 公开规范。
  - 高分辨率控制器的高低字节配对规则；通用 MIDI 规范是主要依据。
updated: 2026-11-02
---

::: zh
同一个推子，在有的音源上是音量，在别处却是滤波。CC 号不是第几个旋钮，而是有约定的地址。

## 问题

把 CC 当万能旋钮，会让踏板的开关值被误当连续量，也会让库选择与音色切换抢同一条通道。编号记错，整条曲线就落到别的参数上。

## 协议或消息

CC0–31 是高 7 位（MSB），CC32–63 是对应的低 7 位（LSB）；接收端支持时，配对值为 MSB × 128 + LSB。常用编号有 CC7 音量、CC10 声像、CC11 表情和 CC1 调制。CC74 的标准名称是亮度，不保证每个音源都把它映射到滤波截止。CC0/32 选择音色库，随后才发 Program Change；RPN/NRPN 先选参数，再由 Data Entry 写入值。

## 参数与做法

延音踏板 CC64 的开关约定是 0–63 关、64–127 开；半踏板需要音源另行支持。把表情用于乐句起伏、通道音量用于平衡，先在目标音源上验证。高分辨率 CC 是否支持、两半消息如何处理，以及 RPN 是否生效，都要查设备的 MIDI 实现表。

## 听什么

在同一音源中分别改变 CC7、CC11 和 CC1，记录声音与电平如何变化。若 CC1 改的是滤波或层间渐变，而不是颤音，这是该音源的映射，不是消息发送错误。

## 常见误解

CC 不是自动化曲线。CC 号不是厂商音色参数。所有 CC 都只到 127，14 位要两条消息拼。

```audiolab
{"type":"instrument","gm":"Violin","synth":"bowed","phrase":["G4","A4","B4","D5"],"label":"弦乐短句","label_en":"String phrase","hint":"这是固定音符的音色参照，没有独立发送音量、表情或踏板控制器。CC 对照应在支持事件检查的音序器中完成。","hint_en":"This fixed-note phrase is a timbre reference, not separate volume, expression or pedal-controller tests. Compare CC events in a sequencer that exposes them."}
```
:::

::: en
The same fader is volume on one source and cutoff on another. A CC number is an agreed address rather than the third knob.

## The problem

Treating CC as a universal knob turns a pedal switch into a continuous value and lets bank select collide with program change. A wrong number puts the whole curve on another parameter.

## Protocol or message

CC0–31 carry the most significant seven bits; CC32–63 carry the corresponding least significant bits. Where supported, a paired value is MSB × 128 + LSB. Common addresses include CC7 volume, CC10 pan, CC11 expression and CC1 modulation. CC74 is named Brightness; its exact effect depends on the receiver. Bank Select CC0/32 precedes Program Change, while RPN/NRPN selection precedes Data Entry.

## Settings and practice

For sustain CC64, values 0–63 mean off and 64–127 mean on; half-pedalling needs additional receiver support. Use expression for phrasing and channel volume for balance, then test the target instrument. Check its MIDI implementation chart for high-resolution CC and RPN support.

## What to listen for

Change CC7, CC11 and CC1 separately on one instrument and note the sound and level. If CC1 changes a filter or crossfades layers rather than adding vibrato, that is the instrument mapping, not necessarily a transmission fault.

## Common misunderstandings

CC is not an automation curve. A CC number is not a vendor parameter. Every CC stops at 127, so 14 bits need two messages.

```audiolab
{"type":"instrument","gm":"Violin","synth":"bowed","phrase":["G4","A4","B4","D5"],"label":"String phrase","label_en":"String phrase","hint":"This fixed-note phrase is a timbre reference, not separate volume, expression or pedal-controller tests. Compare CC events in a sequencer that exposes them.","hint_en":"This fixed-note phrase is a timbre reference, not separate volume, expression or pedal-controller tests. Compare CC events in a sequencer that exposes them."}
```
:::
