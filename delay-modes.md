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
  - oga-000002 | 短乐句的音符素材，尚未施加乒乓延迟 | Short-phrase notes without ping-pong delay processing
  - oga-000011 | 重复织体参照，可另送延迟器检查反馈叠加 | Repeated texture that can be separately sent to a delay to check feedback
  - mutopia-001411 | 分解和弦的节拍参照，未添加附点八分回声 | Arpeggiated beat reference without added dotted-eighth echoes
sources:
  - Udo Zölzer, DAFX.
  - Sound On Sound, delay effects explained.
updated: 2026-11-02
---

::: zh
## 难在哪

延迟不只是「加个回声」。单声道、立体声与乒乓把回声放在不同位置，决定了它是填满中间，还是把两侧推开。

## 背后的机制

单声道只有一条延迟线，回声落在中央，最容易与主唱抢位置；立体声用两条时间略有差异的线，回声分居两侧；乒乓让反馈在左右之间交替，每次重复换边。反馈量决定重复次数，环路里的滤波让每次重复更暗。

## 旋钮与耳朵

四分音符延迟时间为 60000/BPM 毫秒；120 BPM 时是 500 ms，八分音符为 250 ms，附点八分为 375 ms。先用低反馈听清第一遍重复，再增加回声数量，避免强回声盖住下一句。把处理后信号折成单声道，检查左右延迟叠加后是否变空或过响。

## 耳朵要抓的点

放一段吉他短句，先听单声道回声与干声挤在中间，再切到乒乓，重复会从左跳到右。反馈加到 60% 以上，重复会堆成一片。

```audiolab
{"type":"instrument","gm":"Lead 2 (sawtooth)","synth":"bowed","phrase":["A4","C5","E5","A5"],"label":"合成器短句","label_en":"Synthesizer phrase","hint":"注意短句之间留下的空隙。播放器没有乒乓延迟控件；可另将同一音频送入延迟器，检查回声是否占用这些空隙。","hint_en":"Notice gaps between phrases. There is no ping-pong delay control here; send the same audio to a delay separately and check where repeats fall."}
```

## 容易弄错的

以为乒乓一定更宽；认为延迟时值必须与速度对齐；把高反馈当成混响。
:::

::: en
## Where it gets hard

Delay is not just adding an echo. Mono, stereo and ping-pong place repeats differently, and that placement decides whether they fill the centre or open the sides.

## The mechanism

Mono uses one delay line, so repeats sit in the middle and compete with the lead. Stereo uses two lines with slightly different times, placing repeats on opposite sides. Ping-pong alternates feedback between left and right, so every repeat changes side. Feedback sets how many repeats survive, and filters in the loop make each one darker.

## Knobs and ears

A quarter-note delay lasts 60000/BPM milliseconds: at 120 BPM this is 500 ms, with an eighth at 250 ms and a dotted eighth at 375 ms. Begin with low feedback to hear the first repeat clearly, then add repeats without masking the next phrase. Fold the result to mono and check for cancellation or excessive level.

## What the ear should catch

Play a short guitar phrase, first with mono repeats crowding the centre, then switch to ping-pong and hear them jump left and right. Push feedback past 60 percent and the repeats pile into a wash.

```audiolab
{"type":"instrument","gm":"Lead 2 (sawtooth)","synth":"bowed","phrase":["A4","C5","E5","A5"],"label":"Synthesizer phrase","label_en":"Synthesizer phrase","hint":"Notice gaps between phrases. There is no ping-pong delay control here; send the same audio to a delay separately and check where repeats fall.","hint_en":"Notice gaps between phrases. There is no ping-pong delay control here; send the same audio to a delay separately and check where repeats fall."}
```

## Easy to get wrong

That ping-pong is always wider; that delay time must match the tempo; that high feedback is the same as reverb.
:::
