---
id: fm-synthesis
site: prod
cat: B3
title: FM 合成
title_en: FM Synthesis
summary: 一个振荡器推另一个，造出钟、电钢与金属。
summary_en: One oscillator modulates another to make bells, electric pianos and metal.
level: standard
tags: [合成, FM, 调制, 电钢琴]
tags_en: [synthesis, FM, modulation, electric piano]
alias: [FM 合成, 频率调制, 调频合成, FM synthesis, frequency modulation]
links:
  - "[[glossary:timbre]]"
  - "[[instrument:dx7-fm]]"
  - "[[period:modern]]"
instances:
  - oga-000205 | 电钢琴贯穿全曲，金属音头与柔和尾音是 FM 音色的典型组合
  - oga-000211 | 电钢琴与管钟并置，非谐波泛音造成的钟形听感最明显
  - oga-000143 | 管钟与金属铺底，击发瞬间的明亮泛音适合辨 FM 类音色
sources:
  - John Chowning, The Synthesis of Complex Audio Spectra by Means of Frequency Modulation — sideband theory checked, not quoted
  - Gordon Reid, Sound On Sound Synth Secrets — FM ratios and index checked, not quoted
updated: 2026-10-28
---

::: zh
## 问题

只有两个振荡器，为什么能做出电钢琴、管钟、金属打击和厚贝斯？FM 合成用很少的零件，换来极宽的音色范围。

## 原理

一个振荡器当载波，另一个当调制器去推它的频率。调制器每推一次，频谱就多出一对边带，位于载波加减调制频率处。频率比为整数时，边带落在谐波上，声音有音高；为非整数时，边带落在谐波之间，听感接近钟与金属。深度叫指数，越大边带越多，音色越亮也越复杂。包络加在指数上，音头可以先亮后暗。

## 参数与听感

比值决定音色家族，一比一偏木质感，一比二偏空心，非整数比偏钟形。指数从低到高，正弦会逐渐长出边带，先像电钢，再像铜管，最后接近噪声。调制器包络短则音头有金属撞击，长则整段都亮。反馈会让波形更粗糙，常用于贝斯与打击。

## 听什么

先听电钢琴，注意音头的金属感与随后变柔的尾音。再听管钟，比较非谐波边带带来的钟形泛音。最后把指数想象着推高，听音色从干净的正弦走向金属，而不是音高在抖动。

```audiolab
{"type":"instrument","gm":"Electric Piano 1","synth":"struck","phrase":["C4","E4","G4","B4"],"label":"电钢琴的金属音头","label_en":"The metallic head of an electric piano","hint":"先听音头的亮度与尾音的柔度，再想象把调制指数推高，边带会一层层加进来","hint_en":"Hear the bright head and soft tail, then imagine raising the modulation index as sidebands arrive layer by layer"}
```

## 常见误解

把 FM 当成颤音，颤音是慢速推音高，FM 是音频速率推频率；以为 FM 只能做电钢琴，它也能做贝斯与打击；以为加法合成更直接，FM 用更少的振荡器得到同样复杂的谱。
:::

::: en
## The question

With two oscillators, how can one engine produce electric piano, bells, metallic percussion and a fat bass? FM covers a wide range with few parts.

## How it works

One oscillator is the carrier, the other the modulator pushing it. Each push adds sidebands at the carrier plus or minus modulator multiples. When the ratio is an integer, the sidebands land on harmonics and the sound has pitch. When the ratio is non-integer, they fall between harmonics and read as bells or metal. Depth is the index; a larger index means more sidebands and a brighter tone. An envelope on the index lets the attack start bright, then soften.

## Settings and what you hear

The ratio sets the family; one to one leans woody, one to two hollow, non-integer bell-like. As the index rises, a sine grows sidebands, passing from electric piano to brass to noise. A short modulator envelope strikes metallically, a long one keeps the note bright. Feedback roughens the wave and suits bass and percussion.

## What to listen for

Hear the electric piano first, noting the metallic head and the softer tail. Then hear the bells and their non-integer sidebands. Finally imagine raising the index and hear the sine move toward metal, without the pitch wobbling.

```audiolab
{"type":"instrument","gm":"Electric Piano 1","synth":"struck","phrase":["C4","E4","G4","B4"],"label":"The metallic head of an electric piano","label_en":"The metallic head of an electric piano","hint":"Hear the bright head and soft tail, then imagine raising the modulation index as sidebands arrive layer by layer","hint_en":"Hear the bright head and soft tail, then imagine raising the modulation index as sidebands arrive layer by layer"}
```

## Common misconceptions

That FM means vibrato, when FM pushes frequency at audio rate; that FM is only for electric pianos, when it also makes bass; that additive is more direct, when FM reaches a similar spectrum with fewer oscillators.
:::
