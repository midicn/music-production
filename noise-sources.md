---
id: noise-sources
site: prod
cat: B3
title: 噪声源
title_en: Noise Sources
summary: 噪声没有基频，却是鼓、气声与纹理的原料。
summary_en: Noise has no fundamental, yet it supplies drums, breath and texture.
level: standard
tags: [合成, 噪声, 打击乐, 纹理]
tags_en: [synthesis, noise, percussion, texture]
alias: [噪声源, 白噪声, 粉红噪声, 棕噪声, noise, white noise, pink noise]
links:
  - "[[glossary:timbre]]"
  - "[[glossary:eq]]"
  - "[[instrument:drum-kit]]"
  - "[[period:modern]]"
instances:
  - oga-000009 | 海滩场景直接使用海浪音效，宽频噪声的起伏最适合听
  - oga-000014 | 8-bit 头目曲的鼓组走噪声通道，嘶声与音高感可直接分辨
  - oga-000098 | 废墟场景叠入海浪与掌声采样，宽带噪声铺满背景
sources:
  - Curtis Roads, The Computer Music Tutorial — noise spectra and filtering checked, not quoted
  - Udo Zölzer, DAFX — Digital Audio Effects, noise generation chapter — background checked, not quoted
updated: 2026-10-28
---

::: zh
## 问题

噪声在合成器里为什么和振荡器并列？它没有音高，似乎只能做沙沙声，可鼓组、气声、风声与电影纹理都离不开它。

## 原理

噪声是一串随机样本。白噪声在每一赫兹上能量相同，听感最亮；粉红噪声每升高一个八度能量下降约三分贝，更接近自然界的雨声；棕噪声下降更快，低频更重。把噪声送进带通滤波器并提高共振，会在中心频率附近形成可辨认的音高感，军鼓与镲片就是这样被塑造的。包络决定它是短促一击还是长气流。

## 参数与听感

噪声颜色决定亮暗比例，电平决定它在混音里的存在感，滤波器类型与截止决定厚薄。白噪声像电视雪花，粉红噪声像雨，棕噪声像远处车流。高通让噪声变薄变近，低通让它变闷变远；短衰减适合镲片，长衰减适合风声与铺底。

## 听什么

先听海浪采样，注意高频碎声与低频涌动同时存在。再听 8-bit 鼓组，镲片的嘶声与底鼓的音高形成对照。最后给噪声加一个缓慢扫动的带通，听中心频率移动时「音高感」怎样出现又消失。

```audiolab
{"type":"instrument","drum":"42","synth":"perc","phrase":["42","42","38","42"],"label":"噪声镲片与军鼓","label_en":"Noise hat and snare","hint":"听每一下的嘶声长度，再想象把衰减拉长成一片风；噪声的用法就藏在这个长度里","hint_en":"Hear the hiss length on each hit, then imagine stretching the decay into wind; the use of noise lives in that length"}
```

## 常见误解

以为噪声没有音高就没有用途；以为噪声只是特殊效果，其实它每天都在鼓组与气声里；以为噪声越大越有力量，过量只会把中频糊住。
:::

::: en
## The question

Why does noise sit beside the oscillator on a synth? It has no pitch and seems useful only for hiss, yet drums, breath, wind and film depend on it.

## How it works

Noise is a stream of random samples. White noise carries equal energy per hertz, brightest to the ear. Pink noise falls three decibels per octave, closer to rain. Brown noise falls faster and leans low. Send noise through a band-pass and raise resonance; a recognisable pitch appears near the centre frequency, and that is how snares and cymbals form. An envelope decides short hit or long stream of air.

## Settings and what you hear

Noise colour sets the balance of bright and dark, level sets presence in the mix, and filter type and cutoff set weight. White noise is television snow, pink is rain, brown is distant traffic. A high-pass thins and brings noise forward; a low-pass muffles and pushes it back. Short decays suit cymbals, long decays suit wind and beds.

## What to listen for

Start with the seashore sample and hear spray and low surge at once. Then hear the 8-bit kit, where cymbal hiss contrasts with the pitched kick. Finally sweep a band-pass across noise and notice the sense of pitch appear and vanish as the centre moves.

```audiolab
{"type":"instrument","drum":"42","synth":"perc","phrase":["42","42","38","42"],"label":"Noise hat and snare","label_en":"Noise hat and snare","hint":"Hear the hiss length on each hit, then imagine stretching the decay into wind; the use of noise lives in that length","hint_en":"Hear the hiss length on each hit, then imagine stretching the decay into wind; the use of noise lives in that length"}
```

## Common misconceptions

That noise is useless because it has no pitch; that it is only a special effect, when it is in every kit and breath; that more noise means power, when excess smears the midrange.
:::
