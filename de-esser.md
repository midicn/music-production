---
id: de-esser
site: prod
cat: A7
title: 去齿音器
title_en: The De-esser
summary: 只盯住齿音频段，压掉刺耳的 s 而不压扁整个字。
summary_en: Watching only the sibilant band, so a sharp s softens without flattening the whole word.
level: standard
tags: [效果器, 动态, 齿音, 人声]
tags_en: [effects, dynamics, sibilance, vocal]
alias: [去齿音器, 消齿音, 齿音控制, de-esser, desser]
links:
  - "[[glossary:eq]]"
  - "[[glossary:compressor]]"
  - "[[instrument:popular-voice]]"
instances:
  - mutopia-000546 | 艺术歌曲旋律的MIDI参照，不含德语辅音的实际演唱 | Art-song MIDI melody without actual sung German consonants
  - mutopia-000004 | 英语歌曲的音符参照，不能直接检验齿音压制 | English-song notes that do not directly test de-essing
  - mutopia-000038 | 合唱声部叠置参照，不包含真实声部的齿音累积 | Layered choral parts without recorded accumulation of sibilance
sources:
  - "https://www.fabfilter.com/help/pro-ds/using/advancedcontrols"
  - Udo Zölzer, DAFX.
  - Huber and Runstein, Modern Recording Techniques, vocal processing chapter.
updated: 2026-11-02
---

::: zh
## 要解决的事

去齿音器对短促、过强的擦音进行动态衰减。目标频带随声音、语言、话筒和处理链变化，不只限于某个固定的5–10 kHz区间。需要控制的是相对句子过于突出的部分，而非消除正常辅音。

## 背后的机制

检测器先判断何时需要衰减，实际处理可作用于全频信号、分频后的高频带，或特定动态EQ频段。检测频率不一定等于被衰减频带。宽带模式在单人声上也可能自然，分频模式也可能损伤高频细节，两者都应结合原素材比较。

## 旋钮与耳朵

先循环一句有问题的真实人声，使用检测监听定位擦音，再调阈值与最大衰减。回到整句确认正常辅音、元音和气息仍连贯。需要的启动、释放和衰减量依算法与素材而定，过强处理会使发音含混；先用片段增益处理个别极端音节也是可选方法。

## 耳朵要抓的点

在女高音与钢琴的段落里先关掉去齿音器，记住 s 刺耳的位置，再打开并逐渐加深。齿音应该变软，但字头仍要清楚。换到合唱，注意不要把所有高频都压暗。

```audiolab
{"type":"instrument","gm":"Choir Aahs","synth":"vocal","phrase":["A3","E4","A4","E4","A3"],"label":"合唱音色参照","label_en":"Choir-timbre reference","hint":"合成合唱不发出真实歌词辅音。齿音判断须用带擦音的真实或实际合成人声音频，并检查处理旁通。","hint_en":"A choir preset does not pronounce real lyric consonants. Evaluate sibilance with actual recorded or synthesized vocal audio and compare bypass."}
```

## 容易弄错的

以为去齿音器只对人声有用；以为阈值越低越安全；以为它能把所有刺耳感都修掉。
:::

::: en
## The problem to solve

A de-esser dynamically attenuates brief, excessive sibilance. The relevant band depends on voice, language, microphone and processing rather than one fixed 5–10 kHz range. Control what protrudes from the phrase without removing normal consonants.

## The mechanism

A detector decides when attenuation is needed; processing may affect the full signal, a split high band or a dynamic-EQ band. The detection band need not be the attenuated band. Wide-band processing can sound natural on a single vocal, while split-band processing can still harm high-frequency detail; compare both on the source.

## Knobs and ears

Loop a problematic vocal phrase, use detector audition to locate sibilance, then set threshold and maximum reduction. Return to the full phrase and check consonants, vowels and breaths. Timing and reduction depend on algorithm and source; excessive treatment obscures pronunciation. Clip gain is also an option for isolated extreme syllables.

## What the ear should catch

On a soprano with piano, bypass the de-esser and remember where the s bites, then engage it and deepen gradually. The s should soften while the word stays clear. On a choir, take care not to dull the whole top end.

```audiolab
{"type":"instrument","gm":"Choir Aahs","synth":"vocal","phrase":["A3","E4","A4","E4","A3"],"label":"Choir-timbre reference","label_en":"Choir-timbre reference","hint":"A choir preset does not pronounce real lyric consonants. Evaluate sibilance with actual recorded or synthesized vocal audio and compare bypass.","hint_en":"A choir preset does not pronounce real lyric consonants. Evaluate sibilance with actual recorded or synthesized vocal audio and compare bypass."}
```

## Easy to get wrong

That a de-esser is only for vocals; that a lower threshold is always safer; that it can remove every harsh sound.
:::
