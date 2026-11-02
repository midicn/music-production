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
  - openscore-000007 | 法语歌曲的音符参照，不包含字头与气声的录音（C1） | French-song notes without recorded consonant attacks or breath (C1)
  - openscore-000021 | 歌曲旋律参照，不含压制齿音前后的音频（C1） | Song-melody reference without before-and-after de-essing audio (C1)
  - openscore-000024 | 高音声部参照，不能把音符泛音当成真实擦音（C1） | High vocal-part notes; their harmonics are not recorded sibilants (C1)
sources:
  - "https://www.fabfilter.com/help/pro-ds/using/advancedcontrols"
  - Bobby Owsinski, The Mixing Engineer's Handbook, vocal sibilance and de-essing.
  - David Gibson, The Art of Mixing, vocal consonant preservation.
updated: 2026-11-02
---

::: zh
## 问题

近距离拾音与明亮麦克风会把五到八千赫兹的擦音放大，压缩之后更跳。有人用均衡把这一带整体切掉，结果歌词发闷，唇齿音消失，人声像隔着一层布。

## 目标与判断

只压过量的那几下，不动正常的辅音。判断时连续听整段歌词，标记每次刺耳的位置；若刺耳只出现在少数音节，用动态处理；若每个字都刺，先查麦克风距离与增益，而不是继续加去齿音。压完后辅音仍要能分辨词义。

## 做法

先用检测监听定位实际擦音，再比较片段增益、宽带或分频模式。选择能让整句发音自然的方式，并限制最大衰减。不要仅凭人声性别预设频率，也不要把宽带模式限定为极端情况；算法和输入差异会改变结果。处理后在匹配电平下听整句，防止为了消除一个s音而损伤相邻元音。

## 听什么

在同一段实际人声音频中，比较旁通与处理后的s、sh及相邻元音，检查是否含混或过暗。高音音符的频率高，不等于存在语言擦音；判断应针对实际发音而不是音符音区。

```audiolab
{"type":"instrument","gm":"Voice Oohs","synth":"vocal","phrase":["A4","E5","A5"],"label":"高音区旋律参照","label_en":"High-register melody reference","hint":"高音区音符与歌词擦音是不同现象。本段没有歌词发音，也没有去齿音处理。","hint_en":"High notes and sibilant consonants are different phenomena. This block contains neither lyric pronunciation nor de-essing."}
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

Locate actual sibilance with detector audition, then compare clip gain, wide-band and split-band modes. Choose natural phrase-level pronunciation and limit maximum attenuation. Do not set frequency solely from singer gender or reserve wide-band mode for extreme cases; algorithm and input matter. Loudness-match the full phrase and ensure that treating one s does not damage neighbouring vowels.

## What to listen for

Compare s, sh and neighbouring vowels in bypassed and processed versions of the same vocal audio, checking intelligibility and dulling. A high musical note does not by itself contain a sibilant consonant; judge the pronunciation rather than register.

```audiolab
{"type":"instrument","gm":"Voice Oohs","synth":"vocal","phrase":["A4","E5","A5"],"label":"High-register melody reference","label_en":"High-register melody reference","hint":"High notes and sibilant consonants are different phenomena. This block contains neither lyric pronunciation nor de-essing.","hint_en":"High notes and sibilant consonants are different phenomena. This block contains neither lyric pronunciation nor de-essing."}
```

## Common misconceptions

That de-essing means cutting highs; that every sibilant must disappear; that more reduction is always safer.
:::
