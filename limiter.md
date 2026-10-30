---
id: limiter
site: prod
cat: A7
title: 限制器
title_en: The Limiter
summary: 守住峰值而不改音色，前视、释放与真峰值各自做什么。
summary_en: Holding peaks without changing tone, and what lookahead, release and true peak each do.
level: standard
tags: [效果器, 动态, 限制器, 响度]
tags_en: [effects, dynamics, limiter, loudness]
alias: [限制器, 限幅器, 峰值限制, ceiling, limiter]
links:
  - "[[glossary:true-peak-limiter]]"
  - "[[glossary:clipping]]"
  - "[[instrument:drum-kit]]"
instances:
  - groove-000007 | 慢速摇滚鼓循环的军鼓峰值高，限制器压平瞬态时最容易听出
  - groove-000000 | 放克鼓循环密集，释放太短会让整体随底鼓抽吸
  - oga-000004 | 战斗音乐铜管齐奏多，高频砂纸感会先暴露过量限制
sources:
  - Giannoulis, Massberg and Reiss, Digital Dynamic Range Compressor Design, JAES 2012 — limiter topology checked, not quoted
  - ITU-R BS.1770-4, Algorithms to Measure Audio Programme Loudness and True-peak Level — true-peak method checked, not quoted
updated: 2026-10-28
---

::: zh
## 问题

限制器守在信号链末端，任务是让峰值不越线，同时尽量不改变音色。它和追求整体平均电平的压缩器不是同一件事。

## 原理

限制器用很高的比率和很短的启动，把超过 ceiling 的部分压回去。现代插件用前视延迟提前读取峰值，再用平滑的增益包络处理，所以不会像硬削波那样立刻产生方波。真峰值检测需要过采样，因为采样点之间的峰值可能高于表头读数。释放时间决定增益恢复的速度，也决定低频是否抽吸。

## 参数与听感

ceiling 常设 −1 dBTP，给编码留余量；增益驱动一次加 1–3 dB 就够听出差别。释放 50–200 ms 适合大多数素材，太短会让底鼓每次敲击都把整体拉低。前视越长，瞬态越平；过采样打开后，表头更接近真实峰值。

## 听什么

放慢速摇滚鼓循环，先听军鼓敲击的边缘，再把增益推进 3 dB。军鼓会从「有打击感」变成「贴住天花板」，底鼓同时出现一压一放。换成密集的管弦乐，注意铜管齐奏时高频是否出现砂纸感。

```audiolab
{"type":"instrument","drum":"38","synth":"perc","phrase":["36","38","42","38","36","42","38","46"],"label":"底鼓与军鼓的峰值","label_en":"Kick and snare peaks","hint":"先听干声，再想峰值被压住后哪一下先变平","hint_en":"Hear it dry, then ask which hit flattens first under limiting"}
```

## 常见误解

以为限制器能把响度无限推高；以为 ceiling 设在 0 dBFS 就不会削波；以为限制器只影响峰值、不影响密度。
:::

::: en
## The question

A limiter sits at the end of the chain, keeping peaks under a ceiling while changing tone as little as possible. It is not a compressor, which works on average level.

## How it works

A limiter uses a very high ratio and a short attack to pull down whatever exceeds the ceiling. Modern plugins look ahead and apply a smoothed gain envelope, so the result is not an instant square wave. True-peak detection needs oversampling, since a peak between sample points can sit above the meter. Release sets how fast gain returns and whether the low end pumps.

## Settings and what you hear

Set the ceiling near minus 1 dBTP to leave room for encoding, and add 1 to 3 dB of drive. A release of 50 to 200 ms suits most material; a shorter one makes every kick pull the mix down. Longer lookahead flattens transients more.

## What to listen for

Play a slow rock drum loop and listen to the snare edge, then push the gain by 3 dB. The snare moves from impact to sitting against the ceiling, while the kick makes the rest dip and recover. On dense orchestral music, listen for a sandy edge on brass tuttis.

```audiolab
{"type": "instrument", "drum": "38", "synth": "perc", "phrase": ["36", "38", "42", "38", "36", "42", "38", "46"], "label": "Kick and snare peaks", "label_en": "Kick and snare peaks", "hint": "先听干声，再想峰值被压住后哪一下先变平", "hint_en": "Hear it dry, then ask which hit flattens first under limiting"}
```

## Common misconceptions

That a limiter can push loudness without limit; that a ceiling at 0 dBFS prevents clipping; that limiting changes only peaks and never density.
:::
