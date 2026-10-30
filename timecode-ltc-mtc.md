---
id: timecode-ltc-mtc
site: prod
cat: B2
title: 时间码 LTC 与 MTC
title_en: Timecode, LTC and MTC
summary: 用帧地址对齐画面，LTC 走音频，MTC 走 MIDI。
summary_en: Frame addresses align music to picture, with LTC travelling as audio and MTC as MIDI.
level: standard
tags: [音序, 时间码, 同步, 影视]
tags_en: [sequencing, timecode, sync, film]
alias: [时间码, 帧同步, LTC, MTC, timecode, SMPTE]
links:
  - "[[glossary:tempo]]"
  - "[[glossary:midi-protocol]]"
  - "[[glossary:daw]]"
instances:
  - oga-000002 | 九十秒的关卡配乐，需要按画面打同步点
  - oga-000011 | 一分三十六秒的 boss 曲，段落切换要与画面事件吻合
  - oga-000018 | 城堡场景配乐，进入与退出都要对齐画面
sources:
  - LTC 与 MTC 的帧格式和帧率定义，依时间码与 MIDI 规范核查，未抄文本
  - 影视配乐的追逐与触发同步方式，依后期制作通识核查，未抄文本
updated: 2026-10-28
---

::: zh
时间码给每一个时刻一个帧地址，让音乐、画面与多台机器指向同一个位置。

## 问题

配乐要跟画面，广告要跟镜头，现场要跟视频播放。按小节数拍对不上剪辑软件，必须有一把共同的时间尺。

## 原理

时间码写成时、分、秒、帧，帧率有二十四、二十五、三十与二十九点九七。LTC 把地址调制成音频，录在一条音轨上；MTC 把地址拆成 MIDI 的四分帧消息，每帧发四次。两者都只精确到帧。

## 做法与参数

帧率必须与画面完全一致，二十九点九七要确认是否丢帧；设定统一的起点偏移，chase 模式让从机跟随，trigger 模式只在大位置跳转时对齐；LTC 录在独立音轨，避免被拉伸或变调处理。

## 听什么

听同步点在十分钟后是否仍然吻合。开头对齐、结尾漂移，说明帧率或丢帧设置错了。

## 常见误解

时间码不是速度时钟，它不规定每分钟多少拍；MTC 也不传音频，只传位置。

```audiolab
{"type":"rhythm","sig":"4/4","pattern":"q q q q","bpm":100,"label":"按拍打的参考点","label_en":"Reference points on the beat","hint":"先听拍点，再想它与帧的关系","hint_en":"Hear the beats, then relate them to frames"}
```
:::

::: en
Timecode gives every moment a frame address, so music, picture and several machines can point at the same place.

## The problem

A score must follow picture, a commercial must follow shots, and a live show must follow video playback. Counting bars does not match an editing application, so a shared ruler is needed.

## How it works

Timecode reads hours, minutes, seconds and frames, with rates of twenty-four, twenty-five, thirty and twenty-nine point nine seven. LTC modulates the address into audio and records it on a track; MTC splits it into MIDI quarter-frame messages, four per frame. Both resolve only to a frame.

## Settings and practice

Match the frame rate exactly, and confirm whether twenty-nine point nine seven uses drop frame. Set a common start offset; chase mode follows the master continuously, while trigger mode aligns only on large jumps. Record LTC on its own track and keep it away from stretching or pitch processing.

## What to listen for

Check whether sync points still agree after ten minutes. Aligned at the start and drifting at the end means the frame rate or drop-frame setting is wrong.

## Common misunderstandings

Timecode is not a tempo clock and does not set beats per minute. MTC carries position, not audio.

```audiolab
{"type": "rhythm", "sig": "4/4", "pattern": "q q q q", "bpm": 100, "label": "Reference points on the beat", "label_en": "Reference points on the beat", "hint": "先听拍点，再想它与帧的关系", "hint_en": "Hear the beats, then relate them to frames"}
```
:::
