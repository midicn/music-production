---
id: midi-2-0
site: prod
cat: B1
title: MIDI 2.0
title_en: MIDI 2.0
summary: UMP 把消息装进 32 位字，力度与控制器升到 16 位和 32 位。
summary_en: UMP packs messages into 32-bit words, raising velocity to 16 bits and controllers to 32.
level: standard
tags: [MIDI, MIDI 2.0, UMP, 协商]
tags_en: [MIDI, MIDI 2.0, UMP, negotiation]
alias: [MIDI2, MIDI 2.0, UMP, 通用 MIDI 包]
links:
  - "[[glossary:midi-protocol]]"
  - "[[instrument:midi-controller]]"
  - "[[glossary:latency]]"
instances:
  - oga-000087 | 11637 条弯音挤在 14 位范围里，控制器仍只有 0 到 127
  - pdmx-002317 | 55564 条 CC2 只有 0 到 127 的取值，16 个通道全满
  - musicnet-000303 | 15222 条 CC11 挤在 7 位范围里，渐强靠事件密度补足
sources:
  - MIDI 2.0 规范对 UMP、能力询问与协议协商的定义，依 MMA 公开规范核查，未抄文本
  - MIDI 2.0 与 MIDI 1.0 的兼容层设计，依公开技术说明核查，未抄文本
updated: 2026-10-28
---

::: zh
七位数值只有 128 级，长滑音听得出台阶，精细的滤波扫描也画不细。MIDI 2.0 先解决分辨率，再解决设备之间怎么谈。

## 问题

弯音虽然拼成 14 位，控制器却仍停在 0 到 127。通道只有 16 个，开 MPE 就紧张。新旧设备混在一起时，谁来降级、谁来协商，也需要约定。

## 协议或消息

MIDI 2.0 在 2020 年发布，核心是 UMP，每条消息占一个或多个 32 位字。通道语音消息的力度升到 16 位，控制器升到 32 位，弯音也加宽。它保留 MIDI 1.0 消息作为兼容层，双方先做能力询问与协议协商，再决定说哪一种。属性交换用 JSON 描述设备能力，配置用 Profile 声明。

## 参数与做法

新旧设备混用时让系统自动协商，不要手动强制。导出仍以 MIDI 1.0 为底线，接收端不认 2.0 时自动降级。高分辨率控制器要有真实数据，别把 7 位值左移充数。

## 听什么

慢速滑音更平滑，弱奏的层次更细，滤波器扫频少了阶梯感。差异在小幅变化里最明显，大幅动作反而听不出。

## 常见误解

MIDI 2.0 不是新接口，DIN 与 USB 都能承载。它不是音频协议。UMP 不是文件格式，SMF 仍是另一套容器。

```audiolab
{"type":"instrument","gm":"Violin","synth":"bowed","phrase":["A4","B4","C5","D5"],"label":"七位分辨率的天花板","label_en":"The ceiling of seven bits","hint":"听长音的音高，再想 32 位控制器能画出多细的曲线","hint_en":"Hear the held pitch and imagine how finely a 32-bit controller could draw the curve"}
```
:::

::: en
Seven bits give only 128 steps, so a long slide shows stairs and a fine filter sweep cannot be drawn. MIDI 2.0 fixes resolution first, then how devices talk.

## The problem

Pitch bend uses 14 bits, yet controllers still stop at 0 to 127. Sixteen channels run short once MPE is on. Old and new gear also need rules for fallback and negotiation.

## Protocol or message

MIDI 2.0 arrived in 2020 around UMP, where each message occupies one or more 32-bit words. Channel Voice velocity rises to 16 bits, controllers to 32, and pitch bend widens too. MIDI 1.0 messages remain as a compatibility layer. The two sides exchange capability inquiries and negotiate a protocol. Property Exchange describes device abilities in JSON, while Profiles declare behaviour.

## Settings and practice

Let the system negotiate when old and new gear meet, rather than forcing a mode. Keep MIDI 1.0 as the export floor so a receiver can fall back. Make high-resolution controllers carry real data, not padded 7-bit values.

## What to listen for

Slow slides are smoother, soft playing has finer steps, and filter sweeps lose their staircase. The gain is clearest in small movements, while large gestures hide it.

## Common misunderstandings

MIDI 2.0 is not a new connector, since DIN and USB both carry it. It is not an audio protocol. UMP is not a file format, and SMF remains a separate container.

```audiolab
{"type": "instrument", "gm": "Violin", "synth": "bowed", "phrase": ["A4", "B4", "C5", "D5"], "label": "The ceiling of seven bits", "label_en": "The ceiling of seven bits", "hint": "听长音的音高，再想 32 位控制器能画出多细的曲线", "hint_en": "Hear the held pitch and imagine how finely a 32-bit controller could draw the curve"}
```
:::
