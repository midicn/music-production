---
id: multiband-compression
site: prod
cat: A7
title: 多段压缩
title_en: Multiband Compression
summary: 分频段各自控制动态，让低频不再拖着高频一起抽吸。
summary_en: Separate dynamics per frequency band, so the low end no longer pumps the whole mix.
level: standard
tags: [效果器, 动态, 多段压缩, 分频]
tags_en: [effects, dynamics, multiband, crossover]
alias: [多段压缩, 分频压缩, 多频段压缩, multiband compression, multiband]
links:
  - "[[glossary:compressor]]"
  - "[[glossary:eq]]"
  - "[[instrument:drum-kit]]"
instances:
  - groove-000011 | 放克循环的低频与镲片此起彼伏，分频后能听出各段独立动作
  - oga-000001 | 管弦乐铺底的低音与高音层次清楚，适合观察分频点相位
  - mutopia-000546 | 女声与钢琴的低频容易互相遮挡，分段压缩能减少整体抽吸
sources:
  - Udo Zölzer, DAFX.
  - Giannoulis, Massberg and Reiss, Digital Dynamic Range Compressor Design, JAES 2012.
updated: 2026-10-28
---

::: zh
## 要解决的事

整段压缩会让低频每次敲击都把高频一起拉低。多段压缩把频谱分开，让每一段按自己的动态处理。

## 它怎么工作

分频器把信号拆成两段或更多，常用 Linkwitz-Riley 分频，在交点处保持平坦。每段有独立的阈值、比率、启动与释放，处理后相加。分频点附近的相位变化需要留意，线性相位分频可以避免相位失真，但会有预振铃。多段压缩不是多段 EQ，它改变的是每段的增益包络，而不是固定的频响。

## 数值怎么变成声音

低频段用较慢的启动和释放，保留底鼓的冲击；中频段控制人声的突起；高频段启动可以快一些。分频点常放在 120–200 Hz 与 3–5 kHz。每段只做 2–4 dB 的增益衰减，超过就容易听出频段被单独抽走。

## 耳朵要抓的点

在放克鼓循环上单独听低频段，感受底鼓与贝斯是否一起起伏；回到全频，注意踩镲是否还会随底鼓抽吸。换到人声加钢琴，听 3 kHz 附近的压缩是否让辅音变软。

```audiolab
{"type":"instrument","drum":"36","synth":"perc","phrase":["36","42","38","42","36","42","38","46"],"label":"底鼓与镲片的频段分工","label_en":"Kick and cymbals in separate bands","hint":"先听干声，再想象低频段与高频段各自被压住的样子","hint_en":"Hear it dry, then picture the low and high bands compressed separately"}
```

## 容易弄错的

以为多段压缩等于多段 EQ；以为分得越细越好；以为分频不会带来相位问题。
:::

::: en
## The problem to solve

Full-band compression lets every low hit pull the high end down with it. Multiband compression splits the spectrum so each range can follow its own dynamics.

## How it works

A crossover divides the signal into two or more bands, often with Linkwitz-Riley filters that stay flat at the junction. Each band has its own threshold, ratio, attack and release, and the bands are summed again. Phase change around the crossover matters; linear-phase splitting avoids phase distortion but adds pre-ringing. Multiband compression is not multiband EQ, because it moves a gain envelope per band instead of drawing a fixed response.

## From numbers to sound

Use a slower attack and release on the low band to keep the kick punch. The mid band can control a surging vocal, and the high band can move faster. Crossovers often sit near 120 to 200 Hz and 3 to 5 kHz. Keep gain reduction around 2 to 4 dB per band; beyond that, a band sounds removed.

## What the ear should catch

On a funk drum loop, solo the low band and hear whether kick and bass rise and fall together. Return to full range and notice whether the hats still pump with the kick. On voice and piano, hear whether compression near 3 kHz softens the consonants.

```audiolab
{"type": "instrument", "drum": "36", "synth": "perc", "phrase": ["36", "42", "38", "42", "36", "42", "38", "46"], "label": "Kick and cymbals in separate bands", "label_en": "Kick and cymbals in separate bands", "hint": "先听干声，再想象低频段与高频段各自被压住的样子", "hint_en": "Hear it dry, then picture the low and high bands compressed separately"}
```

## Easy to get wrong

That multiband compression is multiband EQ; that more bands are always better; that splitting introduces no phase problems.
:::
