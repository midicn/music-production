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
  - oga-000009 | 曲目可提供海滩场景的配器参考；海浪音色及其频谱取决于渲染音源 | The piece offers beach-scene orchestration; seashore timbre and spectrum depend on the rendering source
  - oga-000014 | 可比较鼓点的有调与噪声成分，具体合成结构仍需查看所用音源 | Compare pitched and noise-like drum components; inspect the sound source before claiming a synthesis structure
  - oga-000098 | 海浪、掌声等 GM 音色可作纹理参考，不等同于原场景音效录音 | Seashore and applause GM patches offer texture references, not original scene recordings
sources:
  - Curtis Roads, The Computer Music Tutorial.
  - Udo Zölzer, DAFX.
updated: 2026-11-02
---

::: zh
## 难在哪

噪声在合成器里为什么和振荡器并列？它没有音高，似乎只能做沙沙声，可鼓组、气声、风声与电影纹理都离不开它。

## 它怎么工作

理想白噪声的功率谱密度在每Hz带宽内相同，因此越高的一个八度包含越宽带宽、总功率越大。粉红噪声的功率谱密度约按1/f下降，即每升一个八度下降3 dB，使每八度总功率近似相等；棕噪声约按1/f²下降，低频比例更高。实际音频必须带限，不能生成无限带宽的理想噪声。

## 数值怎么变成声音

先在相同感知响度下比较噪声颜色，再用滤波和包络塑造用途。短噪声叠在鼓音头上可增加擦击感，长包络可形成气流或环境层。滤波共振可让随机信号呈现音高感；是否“近”或“远”还取决于电平、混响和上下文，不能只由高通或低通决定。

## 耳朵要抓的点

在合成器里先只开噪声源，保持输出电平，给它加缓慢扫动的带通，听中心频率怎样带出音高感。再固定滤波，缩短或延长包络，比较短打击与持续气流。例曲提供节奏或场景参照，具体音色结构需查看所用音源。

```audiolab
{"type":"instrument","drum":"42","synth":"perc","phrase":["42","42","38","42"],"label":"镲片与军鼓的短声","label_en":"Short hat and snare sounds","hint":"比较镲片和军鼓的衰减与明暗；在合成器里用白噪声、滤波与包络重做，才能检验参数的作用。","hint_en":"Compare hat and snare decay and brightness. Rebuild them with white noise, filtering and an envelope in a synth to test those parameters."}
```

## 容易弄错的

以为噪声没有音高就没有用途；以为噪声只是特殊效果，其实它每天都在鼓组与气声里；以为噪声越大越有力量，过量只会把中频糊住。
:::

::: en
## Where it gets hard

Why does noise sit beside the oscillator on a synth? It has no pitch and seems useful only for hiss, yet drums, breath, wind and film depend on it.

## How it works

Ideal white noise has constant power spectral density per Hz, so each higher octave spans more bandwidth and contains more total power. Pink-noise density falls approximately as 1/f, or 3 dB per octave, giving roughly equal total power per octave. Brown noise follows about 1/f² and favours lows. Real audio must be band-limited rather than infinite-bandwidth ideal noise.

## From numbers to sound

Compare noise colours at similar perceived loudness before applying filters and envelopes. Short noise can add a scrape to a drum attack; a longer envelope can suggest airflow or ambience. Resonant filtering can give random sound a pitch impression. Distance also depends on level, reverb and context, not high-pass or low-pass filtering alone.

## What the ear should catch

In a synthesizer, enable only the noise source and sweep a band-pass at stable output level to hear pitch emerge near its centre. Hold filtering fixed and shorten or lengthen the envelope to compare percussion and sustained airflow. The linked pieces supply rhythm or scene references; inspect the actual sound source before describing its synthesis structure.

```audiolab
{"type":"instrument","drum":"42","synth":"perc","phrase":["42","42","38","42"],"label":"Short hat and snare sounds","label_en":"Short hat and snare sounds","hint":"Compare hat and snare decay and brightness. Rebuild them with white noise, filtering and an envelope in a synth to test those parameters.","hint_en":"Compare hat and snare decay and brightness. Rebuild them with white noise, filtering and an envelope in a synth to test those parameters."}
```

## Easy to get wrong

That noise is useless because it has no pitch; that it is only a special effect, when it is in every kit and breath; that more noise means power, when excess smears the midrange.
:::
