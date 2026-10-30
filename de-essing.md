---
id: de-essing
site: prod
cat: A6
title: 齿音处理
title_en: De-essing
summary: 齿音不是一律削掉，只压住过量的那几下，辅音还得留下。
summary_en: De-essing removes only the few excessive sibilants; the consonants still have to survive.
level: standard
tags: [混音, 人声, 齿音, 动态]
tags_en: [mixing, vocal, sibilance, dynamics]
alias: [去齿音, 齿音, de-esser]
links:
  - "[[glossary:de-esser]]"
  - "[[glossary:eq]]"
  - "[[instrument:voice]]"
  - "[[period:romantic]]"
instances:
  - openscore-000007 | 法语艺术歌曲字头密集，齿音与气声容易分辨（C1）
  - openscore-000021 | 西班牙语歌曲辅音清晰，适合检查齿音是否被压过头（C1）
  - openscore-000024 | 女高音高音多，齿音与高频泛音容易混淆（C1）
sources:
  - Bobby Owsinski, The Mixing Engineer's Handbook, vocal sibilance and de-essing — background checked, not quoted
  - David Gibson, The Art of Mixing, vocal consonant preservation — background checked, not quoted
updated: 2026-10-28
---

::: zh
## 问题

近距离拾音与明亮麦克风会把五到八千赫兹的擦音放大，压缩之后更跳。有人用均衡把这一带整体切掉，结果歌词发闷，唇齿音消失，人声像隔着一层布。

## 目标与判断

只压过量的那几下，不动正常的辅音。判断时连续听整段歌词，标记每次刺耳的位置；若刺耳只出现在少数音节，用动态处理；若每个字都刺，先查麦克风距离与增益，而不是继续加去齿音。压完后辅音仍要能分辨词义。

## 做法

先用片段增益或音量自动化把最尖的几下压平，再让去齿音器做细活。分频模式只处理五到八千赫兹，衰减二到六 dB，启动要快、释放中等，避免抽气。宽带模式会连元音一起压，只在极端时短用。处理后用耳机与手机各听一遍。

## 听什么

听 s 与 sh 是否从句子里跳出来，压完后是否变成 lisp，长音是否还在。下面三个高音连续出现，注意高频边缘何时开始刺。

```audiolab
{"type":"instrument","gm":"Voice Oohs","synth":"vocal","phrase":["A4","E5","A5"],"label":"高音区的边缘","label_en":"The edge of the upper register","hint":"听高音的能量，想象擦音在这一带突然冒出","hint_en":"Hear the energy up high and picture a sibilant jumping out there"}
```

## 常见误解

以为去齿音等于切高频；以为所有齿音都必须消掉；以为压得越多越安全。
:::

::: en
## The problem

Close miking and a bright microphone lift fricatives between five and eight thousand hertz, and compression makes them jump further. Cutting that whole region with EQ leaves the lyric muffled, the consonants gone, and the voice sounding as if it sits behind cloth.

## Goal and judgement

Suppress only the few excessive hits and leave normal consonants intact. Listen through a full verse and mark every piercing moment. If only a few syllables sting, use dynamic control. If every word stings, check microphone distance and gain before adding more de-essing. After processing, consonants must still carry the meaning of the words.

## Method

Flatten the worst peaks first with clip gain or volume automation, then let the de-esser do the fine work. In split-band mode, process only five to eight thousand hertz with two to six dB of reduction, a fast attack and a medium release to avoid pumping. Wideband mode pulls vowels down too, so use it briefly and rarely. Check the result on headphones and on a phone.

## What to listen for

Hear whether s and sh jump out of the phrase, whether the result turns into a lisp, and whether long notes survive. The three high notes below repeat; notice when the upper edge starts to sting.

```audiolab
{"type": "instrument", "gm": "Voice Oohs", "synth": "vocal", "phrase": ["A4", "E5", "A5"], "label": "The edge of the upper register", "label_en": "The edge of the upper register", "hint": "听高音的能量，想象擦音在这一带突然冒出", "hint_en": "Hear the energy up high and picture a sibilant jumping out there"}
```

## Common misconceptions

That de-essing means cutting highs; that every sibilant must disappear; that more reduction is always safer.
:::
