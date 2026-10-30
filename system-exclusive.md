---
id: system-exclusive
site: prod
cat: B1
title: 系统专用消息（SysEx）
title_en: System Exclusive
summary: SysEx 是厂商自定义的长消息，用 7 位数据与校验和完成设置。
summary_en: System Exclusive carries manufacturer settings in 7-bit data, closed by a checksum.
level: standard
tags: [MIDI, SysEx, 复位, 校验和]
tags_en: [MIDI, SysEx, reset, checksum]
alias: [系统专用消息, 系统码, SysEx, system exclusive]
links:
  - "[[glossary:midi-protocol]]"
  - "[[glossary:daw]]"
  - "[[instrument:timpani]]"
instances:
  - musicnet-000300 | 开头两条 SysEx，GM System On 之后紧跟 GS 复位
  - musicnet-000301 | 同一组 GM 与 GS 复位，后面接 16 次音色切换
  - musicnet-000302 | 复位之后低音通道在 43 与 45 之间往返
sources:
  - MIDI 1.0 规范对系统专用消息的结构定义，依 MMA 公开规范核查，未抄文本
  - GM System On 与 Roland GS 复位的字节序列，由本地文件解析核对，未抄文本
updated: 2026-10-28
---

::: zh
有些设置不属于任何通道，只能整机对话。这类消息就是系统专用消息。

## 问题

GM 复位、混响类型、采样载入，都不是某个音符的事。用 CC 做不到，用音色切换也做不到，只能走 SysEx。

## 协议或消息

消息以 0xF0 开头，0xF7 结尾，中间是厂商 ID 与 7 位数据。厂商 ID 可以是一字节，也可以是 00 加两字节。接收端可以不响应。校验和由厂商定义。GM System On 是 F0 7E 7F 09 01 F7。Roland GS 复位是 F0 41 10 42 12 40 00 7F 00 41 F7，最后的 41 是校验和。文件里 SysEx 以带长度的 F0 事件保存。

## 参数与做法

在播放前发一次，不要每个音符前重复。确认设备 ID，发错时设备会安静地忽略。导出后检查 SysEx 是否被剥离。不同设备的校验和算法不同，不要照抄。有些音序器默认不记录 SysEx，导出前要确认轨道设置。复位只作用于当前端口，多端口时要逐个发送。

## 听什么

复位后混响与音色回到默认，紧接着的钢琴会更干或更湿，取决于复位前的设置。

## 常见误解

SysEx 不是音频。不是所有设备都响应。校验和也不是加密。

```audiolab
{"type":"instrument","gm":"Timpani","synth":"struck","phrase":["D2","A2","D3"],"label":"复位之后的第一声","label_en":"The first hit after a reset","hint":"听混响尾巴，想象 GS 复位把空间改回默认","hint_en":"Hear the reverb tail and imagine a GS reset returning the space to default"}
```
:::

::: en
Some settings belong to no channel and require a conversation with the whole device. Those are System Exclusive messages.

## The problem

A GM reset, a reverb type or a sample upload is not about one note. CC cannot do it, Program Change cannot do it, so SysEx takes over.

## Protocol or message

The message starts with 0xF0 and ends with 0xF7, with a manufacturer ID and 7-bit data in between. The ID is one byte, or 00 plus two bytes. A receiver may ignore the message. Checksums are defined by the maker. GM System On is F0 7E 7F 09 01 F7. The Roland GS reset is F0 41 10 42 12 40 00 7F 00 41 F7, where the final 41 is a checksum. In a file, SysEx is stored as an F0 event with a length.

## Settings and practice

Send it once before playback, not before every note. Confirm the device ID. Check after export that SysEx was not stripped. Checksum rules differ between devices, so never copy one blindly.

## What to listen for

After a reset, reverb and timbre return to defaults, so the next piano sounds drier or wetter depending on what came before.

## Common misunderstandings

SysEx is not audio. Not every device answers. A checksum is not encryption.

```audiolab
{"type": "instrument", "gm": "Timpani", "synth": "struck", "phrase": ["D2", "A2", "D3"], "label": "The first hit after a reset", "label_en": "The first hit after a reset", "hint": "听混响尾巴，想象 GS 复位把空间改回默认", "hint_en": "Hear the reverb tail and imagine a GS reset returning the space to default"}
```
:::
