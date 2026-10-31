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
  - musicnet-000301 | 19 种 CC，光 CC11 就有 8444 条，另有库选择与 RPN 复位
  - oga-000003 | 11 种 CC，RPN 的 101、100、6、38 齐全，弯音范围被显式设置
  - groove-000507 | 鼓轨用 14133 条 CC4 记录踏板连续量，另有 16 到 18 号通用控制器
sources:
  - MIDI 1.0 规范的控制器编号与 RPN、NRPN 机制，参考 MMA 公开规范。
  - 高分辨率控制器的高低字节配对规则；通用 MIDI 规范是主要依据。
updated: 2026-10-28
---

::: zh
同一个推子，在有的音源上是音量，在别处却是滤波。CC 号不是第几个旋钮，而是有约定的地址。

## 问题

把 CC 当万能旋钮，会让踏板的开关值被误当连续量，也会让库选择与音色切换抢同一条通道。编号记错，整条曲线就落到别的参数上。

## 协议或消息

0 到 31 是连续控制器，32 到 63 是它们的高位搭档，合起来成 14 位。7 音量、10 声像、11 表情、1 调制、74 截止、71 共鸣。64 到 69 是开关踏板。0 与 32 选音色库。100 与 101 选 RPN，98 与 99 选 NRPN，6 与 38 写值。120 到 127 是通道模式消息。

## 参数与做法

表情与音量分开，表情做乐句，音量做平衡。开关踏板以 64 为界，低于 64 为关，高于 64 为开。RPN 要先选参数再写值，顺序反了不会生效。高分辨率控制器要成对发送，只发一半会被当成粗值。不同音源的映射表要留档。

## 听什么

CC11 的起伏像呼吸，CC7 只改响度，CC1 让音高轻微摆动，CC64 把断奏连成一片。

## 常见误解

CC 不是自动化曲线。CC 号不是厂商音色参数。所有 CC 都只到 127，14 位要两条消息拼。

```audiolab
{"type":"instrument","gm":"Violin","synth":"bowed","phrase":["G4","A4","B4","D5"],"label":"同一条通道上的手势","label_en":"Gestures on one channel","hint":"听长音的起伏，分辨音量、表情与踏板各管什么","hint_en":"Hear the swell and separate volume, expression and pedal"}
```
:::

::: en
The same fader is volume on one source and cutoff on another. A CC number is an agreed address rather than the third knob.

## The problem

Treating CC as a universal knob turns a pedal switch into a continuous value and lets bank select collide with program change. A wrong number puts the whole curve on another parameter.

## Protocol or message

0 to 31 are continuous controllers, paired with 32 to 63 for 14-bit values. 7 is volume, 10 pan, 11 expression, 1 modulation, 74 cutoff and 71 resonance. 64 to 69 are switch pedals. 0 and 32 select a bank. 100 and 101 pick an RPN, 98 and 99 an NRPN, and 6 and 38 write the value. 120 to 127 are channel mode messages.

## Settings and practice

Keep expression and volume apart, expression for phrasing and volume for balance. Switch pedals turn at 64. Select an RPN before writing it. Send high-resolution pairs together, since one half alone reads as a coarse value. Archive the mapping of each sound source.

## What to listen for

CC11 breathes, CC7 only changes level, CC1 wobbles pitch slightly and CC64 joins detached notes into one surface.

## Common misunderstandings

CC is not an automation curve. A CC number is not a vendor parameter. Every CC stops at 127, so 14 bits need two messages.

```audiolab
{"type": "instrument", "gm": "Violin", "synth": "bowed", "phrase": ["G4", "A4", "B4", "D5"], "label": "Gestures on one channel", "label_en": "Gestures on one channel", "hint": "听长音的起伏，分辨音量、表情与踏板各管什么", "hint_en": "Hear the swell and separate volume, expression and pedal"}
```
:::
