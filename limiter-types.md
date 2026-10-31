---
id: limiter-types
site: prod
cat: A8
title: 限制器类型
title_en: Limiter Types
summary: 峰值限制、削波与多段限制解决的不是同一个问题。
summary_en: Peak limiting, clipping and multiband limiting solve different problems, and swapping them shows up first in the attack.
level: standard
tags: [母带, 限制器, 削波, 响度]
tags_en: [mastering, limiter, clipping, loudness]
alias: [限制器类型, 砖墙限制, 削波器, 多段限制, limiter types, clipper]
links:
  - "[[glossary:limiter]]"
  - "[[glossary:true-peak-limiter]]"
  - "[[glossary:clipping]]"
  - "[[glossary:lufs]]"
instances:
  - groove-000004 | 八十四拍的放克鼓组，瞬态被限制器压平后律动会变呆
  - mutopia-000497 | 贝多芬第五第一乐章动态跨度大，能听出限制类型对起伏的影响
  - oga-000011 | 首领段落地鼓密集，削波与限制的差别在低频上最先暴露
sources:
  - Giannoulis, Massberg and Reiss, Digital Dynamic Range Compressor Design, JAES 2012.
  - ITU-R BS.1770-4, Algorithms to Measure Audio Programme Loudness and True-peak Level.
  - FabFilter, Pro-L 2 user manual, limiting styles and oversampling.
updated: 2026-10-31
order: 460
---

::: zh
把削波器当限制器用，鼓会先失去起音；把限制器当削波器用，响度总差一截。名字都叫限制，做的事并不相同。

## 四种常见类型

| 类型 | 工作方式 | 听感 | 常见用途 | 风险 |
|---|---|---|---|---|
| 砖墙限制 | 前视加平滑增益 | 干净，可能抽吸 | 交付末端 | 释放过短 |
| 削波器 | 直接削掉尖峰 | 密度高，边缘硬 | 鼓与电子 | 高频混叠 |
| 多段限制 | 分频段各自限峰 | 低频稳，高频少动 | 低频多的素材 | 分频处相位 |
| 真峰值限制 | 过采样检测峰值 | 编码后不削波 | 有损交付 | 延迟与过采样 |

## 选择看交付

响度目标高、素材以合成器为主，削波加限制的组合更有效。原声乐器多、动态本身就是内容，砖墙限制更稳。低频重而中频薄，多段限制能只收低频。要交给流媒体，真峰值检测必须开，ceiling 留在 −1 dBTP 附近。

## 参数与听感

前视越长，瞬态越平；释放越短，低频抽吸越明显。增益推进一次 1–3 dB，超过就换一种类型，而不是继续加。换类型时先把增益归零，再按同一响度对齐，否则比较的只是响度。削波器的过采样打开后，混叠减少，延迟增加。真峰值表读数高于采样峰值，两者不要混用。

```audiolab
{"type":"instrument","drum":"38","synth":"perc","phrase":["36","38","42","38","36","38","49","46"],"label":"底鼓与军鼓的连续击打","label_en":"A run of kick and snare hits","hint":"先听干声，再想峰值被限制或被削掉后，哪一下先失去边缘","hint_en":"Hear it dry, then ask which hit loses its edge first under limiting or clipping"}
```

## 边界与失败模式

限制器不能修复混音的动态失衡。削波器放在限制器之后，会把限制器的平滑增益重新切硬。两级限制串联，第二级通常只在替第一级收拾释放。ceiling 设在 0 dBFS，转成有损格式仍可能削波。过度限制先吃掉的是最静处的细节，不是最响处。
:::

::: en
Use a clipper as a limiter and the drums lose their attack first. Use a limiter as a clipper and loudness always falls short. Both carry the same name and do different jobs.

## Four common types

| Type | How it works | Sound | Typical use | Risk |
|---|---|---|---|---|
| Brickwall limiter | Lookahead plus smoothed gain | Clean, may pump | End of delivery chain | Release too short |
| Clipper | Shaves the spikes directly | Dense, hard edges | Drums and electronic | High-frequency aliasing |
| Multiband limiter | Limits each band separately | Steady lows, less high-end work | Bass-heavy material | Phase at crossovers |
| True-peak limiter | Oversampled peak detection | No clipping after encoding | Lossy delivery | Latency and oversampling |

## The choice follows delivery

With a high loudness target and synth-led material, clipping plus limiting is more efficient. With acoustic instruments and dynamics that carry the music, a brickwall limiter is steadier. When the low end is heavy and the mids are thin, multiband limiting can work only on the bass. For streaming delivery, true-peak detection must be on, with the ceiling near −1 dBTP.

## Reading the controls by ear

Longer lookahead flattens transients more; shorter release makes low-end pumping clearer. Add 1–3 dB of drive at a time, then switch type rather than push further. When switching type, reset gain and match loudness again, otherwise the comparison is only about level. Oversampling in a clipper reduces aliasing and adds latency. A true-peak meter reads above the sample peak, so do not treat the two as the same number.

```audiolab
{"type": "instrument", "drum": "38", "synth": "perc", "phrase": ["36", "38", "42", "38", "36", "38", "49", "46"], "label": "A run of kick and snare hits", "label_en": "A run of kick and snare hits", "hint": "先听干声，再想峰值被限制或被削掉后，哪一下先失去边缘", "hint_en": "Hear it dry, then ask which hit loses its edge first under limiting or clipping"}
```

## Limits and failure modes

A limiter cannot repair dynamic imbalance in the mix. A clipper placed after the limiter cuts the smoothed gain hard again. With two limiters in series, the second usually cleans up the release of the first. A ceiling at 0 dBFS can still clip after lossy encoding. Over-limiting removes detail in the quietest passage before it touches the loudest one.
:::
