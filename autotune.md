---
id: autotune
site: prod
cat: C
order: 21
title: Auto-Tune（音高修正）
title_en: Auto-Tune (Pitch Correction)
summary: 实时把音高拉回音阶，速度决定是修音还是效果。
summary_en: Real-time tuning back to a scale, where the speed decides whether it corrects or becomes an effect.
level: standard
tags: [插件, 音高, 修音, 人声]
tags_en: [plugin, pitch, tuning, vocal]
alias: [Auto-Tune, Antares Auto-Tune, 修音, 音高修正, autotune]
tool_kind: plugin
tool_vendor: Antares
tool_form: 插件
tool_platforms: [macOS, Windows]
tool_price: 买断
tool_jobs: [混音, 现场演出, 编曲]
tool_verified: 2026-10-30
links:
  - "[[glossary:pitch]]"
  - "[[instrument:popular-voice]]"
  - "[[instrument:voice]]"
instances:
  - mutopia-000795 | 福雷《梦后》，长句与颤音都明显，修正速度稍快就会听出机械感（C1）。
  - mutopia-000929 | 格里格《我爱你》，短句换气多，音高起点清楚，适合看逐句修正（C1）。
  - mutopia-000546 | 勃拉姆斯《萨福颂》，半音进行多，音阶设错会把经过音拉走（C1）。
  - mutopia-000522 | 贝多芬《欢乐颂》的声乐版本，旋律朴素，跑音位置容易定位（C1）。
sources:
  - Antares 官方产品页的实时修音、共振峰与音阶说明，参考公开资料。
  - 音高检测与共振峰补偿的常见做法；人声制作惯例是主要依据。
updated: 2026-10-30
---

::: zh
## 它能完成什么

- 把一条唱得不错的声乐轨修到可发布，不必重录。
- 在现场实时修正音高，监听里听到的就是修过的声音。
- 用极快的修正速度做刻意的电音效果，当成编曲的一部分。
- 给说唱与念白做音高轮廓的微调，不改节奏。
- 单独移动共振峰，改变声音的粗细而不改音高。
- 用 MIDI 控制目标音高，做和声或机器人式的跟唱。

## 它怎么工作

插件先检测输入的基本频率，把它和设定的音阶比较，算出偏差，再用变调算法把声音移回目标。修正速度决定多快到位：慢速保留颤音与滑音，快速会把它们抹平。共振峰控制让人在移调后仍保持原来的声道特征；Humanize 让到达目标的过程不那么整齐。音阶可以手设，也可以由 Auto-Key 一类工具从素材里分析。它假设输入是单声部的。检测窗口短，快速转音会被当成两个音，必要时手画音高曲线。

## 边界与坑

- 只处理单声部。合唱、和弦与带强烈伴奏的素材会让检测跳音，修出奇怪的滑音。
- 颤音很宽或气声很重的段落，检测容易抓错周期，宁可分段处理也不要一路加速。
- 音阶设错会把经过音与装饰音拉走；转调段落要分段换音阶。
- 极端移调会改变齿音与气声的比例，修完要重做齿音处理。
- 实时模式有延迟，现场监听要把它算进总延迟，否则唱的人会觉得拖。
- 授权依赖 iLok 账户与激活，换机器或协作前要先把授权迁移。

## 替代与搭配

Melodyne 更适合逐音精细编辑与多声部素材；Waves Tune Real-Time 偏现场；Graillon 有免费档可先试。它常与去齿音、压缩串联：先修音高，再管动态与齿音。需要改时值就不要用它，换能编辑音符的工具。

## 上手路径

先学音阶与修正速度的配合，再学共振峰的作用，最后学分段处理转调。配合「音高」「流行唱法」「人声」三篇读。

```audiolab
{"type":"instrument","gm":"Voice Oohs","synth":"vocal","phrase":["G3","A3","B3","D4","B3","A3","G3"],"label":"一条待修的声乐线","label_en":"A vocal line to tune","hint":"先听每个音的起音，再想慢速修音会留下多少滑音","hint_en":"Hear the onset of each note first, then imagine how much glide a slow retune leaves behind"}
```
:::

::: en
## What it lets you finish

- Bring a well-sung vocal take to release quality without recording it again.
- Correct pitch in real time on stage, so the monitors carry the tuned voice.
- Use a very fast retune as a deliberate vocal effect inside the arrangement.
- Nudge the pitch contour of a rap or spoken phrase without touching its timing.
- Shift formants alone to make a voice thicker or thinner without changing pitch.
- Drive target pitches from MIDI for harmonies or a robotic follow.

## How it works

The plugin detects the incoming fundamental, compares it with the chosen scale, calculates the error, and pitch-shifts the signal back to target. Retune speed sets how quickly it arrives: slow settings keep vibrato and glides, fast settings erase them. Formant control preserves the vocal tract character after shifting, and a humanise control makes the arrival less uniform. The scale can be set by hand or analysed from the material by a companion tool. It assumes a monophonic input. The detection window is short, so a fast turn can read as two notes and may need a drawn pitch curve.

## Limits and traps

- It handles one voice only. Choirs, chords and material with strong backing confuse detection and produce odd glides.
- Wide vibrato and breathy passages are easy to misread, so process in sections rather than speeding up the whole take.
- A wrong scale pulls passing tones and ornaments off course; modulate sections need their own scale.
- Extreme shifts change the balance of sibilance and breath, so the de-esser pass has to be redone afterwards.
- Real-time mode adds latency, and live monitoring must count it in or the singer feels dragged.
- Authorisation depends on an iLok account and activation, so migrate it before changing machines or collaborating.

## Alternatives and pairings

Melodyne suits detailed note-by-note work and polyphonic material. Waves Tune Real-Time leans toward live use. Graillon has a free tier for trying the approach. Auto-Tune usually runs before de-essing and compression: fix pitch, then manage dynamics and sibilance. If timing needs changing, this is the wrong tool; use one that edits notes.

## First three things to learn

Learn scale against retune speed, then what formant control does, then how to split a take at modulations. Read the site's pages on pitch, popular voice and the voice alongside it.

```audiolab
{"type":"instrument","gm":"Voice Oohs","synth":"vocal","phrase":["G3","A3","B3","D4","B3","A3","G3"],"label":"一条待修的声乐线","label_en":"A vocal line to tune","hint":"先听每个音的起音，再想慢速修音会留下多少滑音","hint_en":"Hear the onset of each note first, then imagine how much glide a slow retune leaves behind"}
```
:::
