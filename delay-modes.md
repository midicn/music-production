---
id: delay-modes
site: prod
cat: A7
title: 延迟的三种走法
title_en: Three Delay Modes
summary: 单声道、立体声与乒乓如何摆放回声，反馈与滤波又改变了什么。
summary_en: How mono, stereo and ping-pong delays place repeats, and what feedback and loop filters do to them.
level: standard
tags: [效果器, 延迟, 空间, 听感]
tags_en: [effects, delay, space, listening]
alias: [延迟, 回声, 乒乓延迟, 单声道延迟, 立体声延迟, delay, ping-pong]
links:
  - "[[glossary:delay]]"
  - "[[glossary:reverb]]"
  - "[[glossary:automation]]"
instances:
  - oga-000002 | 游戏配乐的合成器短句音头清楚，乒乓回声的换边最容易追踪
  - oga-000011 | 头目段落的织体重复性强，反馈量增加时尾迹堆积听得清
  - mutopia-001411 | 钢琴分解和弦间隔均匀，附点八分延迟与拍点是否打架一听便知
sources:
  - Udo Zölzer, DAFX — Digital Audio Effects, delay lines chapter — background checked, not quoted
  - Sound On Sound, delay effects explained — mono, stereo and ping-pong topologies checked, not quoted
updated: 2026-10-28
---

::: zh
## 问题

延迟不只是「加个回声」。单声道、立体声与乒乓把回声放在不同位置，决定了它是填满中间，还是把两侧推开。

## 原理

单声道只有一条延迟线，回声落在中央，最容易与主唱抢位置；立体声用两条时间略有差异的线，回声分居两侧；乒乓让反馈在左右之间交替，每次重复换边。反馈量决定重复次数，环路里的滤波让每次重复更暗。

## 参数与听感

附点八分是常见选择，反馈 25–40% 已够形成尾迹；环路高通放在 200–400 Hz，低通放在 4–8 kHz，回声就不会糊住低频。乒乓很宽，但正中央的干声仍要留住，否则声像会空。

## 听什么

放一段吉他短句，先听单声道回声与干声挤在中间，再切到乒乓，重复会从左跳到右。反馈加到 60% 以上，重复会堆成一片。

```audiolab
{"type":"instrument","gm":"Lead 2 (sawtooth)","synth":"bowed","phrase":["A4","C5","E5","A5"],"label":"合成器短句","label_en":"Synth phrase","hint":"先听干声，再想象回声在左右换边","hint_en":"Hear it dry, then imagine repeats changing sides"}
```

## 常见误解

以为乒乓一定更宽；认为延迟时值必须与速度对齐；把高反馈当成混响。
:::

::: en
## The question

Delay is not just adding an echo. Mono, stereo and ping-pong place repeats differently, and that placement decides whether they fill the centre or open the sides.

## How it works

Mono uses one delay line, so repeats sit in the middle and compete with the lead. Stereo uses two lines with slightly different times, placing repeats on opposite sides. Ping-pong alternates feedback between left and right, so every repeat changes side. Feedback sets how many repeats survive, and filters in the loop make each one darker.

## Settings and what you hear

A dotted eighth is a common choice, with 25 to 40 percent feedback enough for a tail. A high-pass at 200 to 400 Hz and a low-pass at 4 to 8 kHz keep repeats out of the low end. Ping-pong is wide, but the dry signal must stay centred or the image empties out.

## What to listen for

Play a short guitar phrase, first with mono repeats crowding the centre, then switch to ping-pong and hear them jump left and right. Push feedback past 60 percent and the repeats pile into a wash.

```audiolab
{"type": "instrument", "gm": "Lead 2 (sawtooth)", "synth": "bowed", "phrase": ["A4", "C5", "E5", "A5"], "label": "Synth phrase", "label_en": "Synth phrase", "hint": "先听干声，再想象回声在左右换边", "hint_en": "Hear it dry, then imagine repeats changing sides"}
```

## Common misconceptions

That ping-pong is always wider; that delay time must match the tempo; that high feedback is the same as reverb.
:::
