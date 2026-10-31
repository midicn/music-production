---
id: mix-completion
site: prod
cat: A6
title: 混音完成度判断
title_en: Judging When a Mix Is Done
summary: 完成不是再也改不动，而是在几套系统上都通过同一张检查表。
summary_en: Done does not mean nothing could change; it means the same checklist passes on several systems.
level: standard
tags: [混音, 完成度, 检查, 决策]
tags_en: [mixing, completion, checks, decision]
alias: [混音完成, 完成度, mix completion]
links:
  - "[[glossary:lufs]]"
  - "[[glossary:headroom]]"
  - "[[glossary:bus]]"
  - "[[instrument:drum-kit]]"
instances:
  - openscore-000008 | 叙事歌曲层次分明，适合检查小音量下歌词是否仍清楚（C1）
  - oga-000004 | 短循环反复听不累，说明平衡经得起重复（C1）
  - musicnet-000069 | 慢乐章尾巴长，适合检查结尾与过渡是否干净（C1）
sources:
  - Bobby Owsinski, The Mixing Engineer's Handbook, mix evaluation and revision.
  - David Gibson, The Art of Mixing, translation across playback systems.
updated: 2026-10-28
---

::: zh
## 问题

混音永远能再改一点：人声再亮一点，军鼓再厚一点。没有停止规则，就会在细节里循环，交付前反而改坏。另一种情况是只在工作室里成立，换到手机或车里，主唱消失、低频爆炸。

## 目标与判断

用一张固定检查表判断完成度：小音量下歌词可懂，单声道不塌，手机上不刺，车里低频不轰，段落过渡没有断点，尾巴不盖下一个字，峰值留够余量。逐项通过才算完成，而不是“听起来差不多了”。若只剩三个以内的问题，记录并判断是否值得再改。

## 做法

先导出二十四位版本，休息一天再听。用参考曲校准响度与频段，不照搬音色。在手机、耳机、车里各听一遍，只记录最明显的三个问题。回到工程只修这三处，再导出对比。确认后冻结工程、整理 stems、写清总线处理与采样率。

## 听什么

听前五秒是否抓人，副歌是否比主歌强，结尾是否自然，循环播放是否疲劳。下面四个音先听整体是否稳，再想换系统会先丢掉哪一层。

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["G3","D4","B4","G5"],"label":"换系统还剩下什么","label_en":"What survives a system change","hint":"先听四声部的平衡，再想象手机喇叭会留下哪一层","hint_en":"Hear the four-part balance, then picture which layer a phone speaker keeps"}
```

## 常见误解

以为完成就是不能再改；以为更响就是更完整；以为客户点头就等于混音成立。
:::

::: en
## The problem

A mix can always change a little more: a brighter vocal, a thicker snare. Without a stopping rule, the work circles through details and often worsens before delivery. Or it only works in the studio; on a phone the vocal vanishes and the low end explodes.

## Goal and judgement

Use a fixed checklist: the lyric stays intelligible at low volume, the mix holds in mono, it does not sting on a phone, transitions have no breaks, tails do not cover the next word, and peaks keep enough headroom. Done means every item passes, not that it sounds about right. If three or fewer issues remain, write them down and decide whether another pass is worth it.

## Method

Print a twenty-four-bit version and rest for a day. Calibrate level and spectrum against a reference without copying its timbre. Listen on a phone, headphones and in a car, and note only the three most obvious problems. Fix those three and print again for comparison. Then freeze the session, prepare stems, and document bus processing and sample rate.

## What to listen for

Hear whether the first five seconds grab attention, whether the chorus is stronger than the verse, whether the ending feels natural, and whether repeat plays cause fatigue. The four notes below should first feel stable as a whole; then imagine which layer a different system would lose.

```audiolab
{"type": "instrument", "gm": "String Ensemble 1", "synth": "bowed", "phrase": ["G3", "D4", "B4", "G5"], "label": "What survives a system change", "label_en": "What survives a system change", "hint": "先听四声部的平衡，再想象手机喇叭会留下哪一层", "hint_en": "Hear the four-part balance, then picture which layer a phone speaker keeps"}
```

## Common misconceptions

That done means nothing can change; that louder means more complete; that a client's approval proves the mix works.
:::
