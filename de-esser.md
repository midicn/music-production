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
  - mutopia-000546 | 女高音唱德语歌词，词尾的 s 与 sch 集中且短促
  - mutopia-000004 | 英语叙事歌曲的字尾齿音清楚，压过头会立刻听出大舌头
  - mutopia-000038 | 合唱圣歌的声部叠加，齿音互相累积后比独唱更刺
sources:
  - Udo Zölzer, DAFX.
  - Huber and Runstein, Modern Recording Techniques, vocal processing chapter.
updated: 2026-10-28
---

::: zh
## 要解决的事

齿音集中在 5–10 kHz，持续时间只有几十毫秒。用全频压缩去压，会把元音和辅音一起压扁；去齿音器只盯住这一段。

## 背后的机制

去齿音器用带通或高通检测齿音能量，超过阈值后衰减一个可调频段。宽带模式衰减整个信号，窄带模式只衰减检测频段，后者更保留字头。分频式设计把信号分成高低两路，只压高频。检测频率要跟着歌手走，男声常在 4–6 kHz，女声常在 6–9 kHz。

## 旋钮与耳朵

频率先扫到齿音最刺的位置，阈值设在正常演唱不触发、只有 s 音触发的位置。range 从 3–6 dB 起，启动尽量快，释放 20–80 ms。压得过多会让 s 变成 th，出现「大舌头」的听感。

## 耳朵要抓的点

在女高音与钢琴的段落里先关掉去齿音器，记住 s 刺耳的位置，再打开并逐渐加深。齿音应该变软，但字头仍要清楚。换到合唱，注意不要把所有高频都压暗。

```audiolab
{"type":"instrument","gm":"Choir Aahs","synth":"vocal","phrase":["A3","E4","A4","E4","A3"],"label":"合唱长音中的齿音","label_en":"Sibilance inside a choral line","hint":"先听干声，再想象只把 6 kHz 附近那一下压短","hint_en":"Hear it dry, then picture shortening only the burst near 6 kHz"}
```

## 容易弄错的

以为去齿音器只对人声有用；以为阈值越低越安全；以为它能把所有刺耳感都修掉。
:::

::: en
## The problem to solve

Sibilance sits between 5 and 10 kHz and lasts a few tens of milliseconds. Full-band compression flattens vowels and consonants together. A de-esser watches only that band.

## The mechanism

A de-esser detects sibilant energy with a band-pass or high-pass filter, then attenuates an adjustable band once the threshold is crossed. Wideband mode turns down the whole signal, while narrowband mode turns down only the detected band, preserving more of the word. A split design compresses only the high path. The detection frequency follows the singer, often 4 to 6 kHz for men and 6 to 9 kHz for women.

## Knobs and ears

Sweep the frequency to the sharpest sibilant, then set the threshold so normal singing does not trigger it and only an s does. Start with 3 to 6 dB of range, a fast attack and a release of 20 to 80 ms. Too much reduction turns s into th and gives a lisping sound.

## What the ear should catch

On a soprano with piano, bypass the de-esser and remember where the s bites, then engage it and deepen gradually. The s should soften while the word stays clear. On a choir, take care not to dull the whole top end.

```audiolab
{"type": "instrument", "gm": "Choir Aahs", "synth": "vocal", "phrase": ["A3", "E4", "A4", "E4", "A3"], "label": "Sibilance inside a choral line", "label_en": "Sibilance inside a choral line", "hint": "先听干声，再想象只把 6 kHz 附近那一下压短", "hint_en": "Hear it dry, then picture shortening only the burst near 6 kHz"}
```

## Easy to get wrong

That a de-esser is only for vocals; that a lower threshold is always safer; that it can remove every harsh sound.
:::
