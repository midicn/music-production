---
id: izotope-ozone
site: prod
cat: C
order: 15
title: Ozone（母带）
title_en: Ozone (Mastering)
summary: 一条现成的母带链，模块齐全，判断仍要自己做。
summary_en: A ready-made mastering chain with all the modules, while the judgement stays yours.
level: standard
tags: [插件, 母带, 响度, 参考]
tags_en: [plugin, mastering, loudness, reference]
alias: [Ozone, iZotope Ozone, 母带插件, mastering suite]
tool_kind: plugin
tool_vendor: iZotope
tool_form: 插件
tool_platforms: [macOS, Windows]
tool_price: 买断
tool_jobs: [母带, 混音, 交付]
tool_verified: 2026-10-30
links:
  - "[[glossary:mastering]]"
  - "[[glossary:limiter]]"
  - "[[glossary:headroom]]"
instances:
  - oga-000001 | 三分多钟的管弦游戏配乐，编制满、段落完整，适合对照母带链收住多少动态（C1，参照不是该插件的演示）
  - groove-000010 | 80 BPM 放克鼓循环，低频与瞬态都清楚，适合检验限幅器是否压扁鼓点（C1，参照不是该插件的演示）
  - oga-000057 | 三分钟的电子游戏曲，峰值密，适合先定响度目标再动最大化器（C1，参照不是该插件的演示）
sources:
  - iZotope 官方产品页的模块、参考匹配与响度说明，对照公开资料整理。
  - 母带链顺序与响度标准的常见做法（母带惯例）。
updated: 2026-10-30
---

::: zh
## 它能完成什么

把一首混好的立体声交成可发布的母带，响度与峰值都达标。用参考曲目对照频响，找出混音里偏多或偏少的一段。在一条链里完成均衡、动态、谐波激励、立体声宽度与限幅。把一批同专辑曲目统一音色与响度，顺序播放时不跳。给单曲与专辑各做一个响度版本，按平台交付。交付前再查一遍单声道、相位、过载与码率。

## 它怎么工作

Ozone 把母带常用模块排成可重排的链，信号自上而下经过。EQ 修整体平衡，动态模块处理整体或分段的电平，激励器加高频谐波，成像器调整宽度与低频单声道化，最大化器做最后一层限幅。参考匹配会分析一首成品曲目的频响与动态，给出目标曲线；助手则从分析出发给一个起点。所有模块都在一个界面里，顺序就是声音的一部分。模块可以单独旁通，A/B 时一次只改一个，因果才听得清。

## 边界与坑

- 助手给的是平均化的起点，直接接受常把有性格的混音压成同一种形状。
- 模块越多、过采样越高，CPU 与延迟越大；母带工程通常只能一次跑一版。
- 参考匹配依赖参考曲目的风格与响度，拿流行参考去套室内乐会得到错误的低频。
- 参考曲目若经过重度压缩，匹配后动态会更少，不要照单全收。
- 响度目标随平台而变，交付前要按发布渠道核对，不是把最大化器推到最响。
- 它修不了混音里的掩蔽与相位问题；母带阶段听到的缺陷，多半要回到分轨解决。
- 插件格式与宿主绑定，换 DAW 前先确认安装器提供的格式。

## 替代与搭配

自己搭链可用 FabFilter Pro-Q 加 Pro-L；要更偏染色的母带看 Waves 的经典限幅与均衡；不想动手时可考虑 LANDR 这类自动母带服务。Ozone 常与 RX 配对：先修复素材，再进母带链。

## 上手路径

先学增益分级与余量，再学限幅器的释放与真峰，最后学参考对照的用法。配合「母带」「限幅器」「动态余量」三篇读。

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C3","G3","D4","A4","E4","C4"],"label":"一段弦乐，待做母带","label_en":"A string passage headed for mastering","hint":"先听渐强的顶，再想限幅器会把哪一段削平、宽度处理会不会让低频变薄","hint_en":"Hear the top of the crescendo first, then imagine where the limiter flattens it and whether width processing thins the low end"}
```
:::

::: en
## What it lets you finish

Turn a finished mix into a release-ready master with peaks and loudness in range. Compare balance against a reference and find the band your mix over- or under-does. Run EQ, dynamics, harmonic excitation, stereo width and limiting in one chain. Unify tone and level across an album so tracks do not jump in sequence. Make separate loudness versions for single and album, each aimed at its platform. Check mono compatibility, phase, clipping and codec behaviour before delivery.

## How it works

Ozone arranges the usual mastering modules in a reorderable chain, and the signal passes from top to bottom. EQ corrects overall balance, dynamics handles level across the programme or in bands, the exciter adds high harmonics, the imager adjusts width and can mono the low end, and the maximiser applies the final limiting. Reference matching analyses a finished track's spectrum and dynamics and proposes a target curve; the assistant uses that to offer a start. Every module sits in one window, and the order is part of the sound. Modules bypass individually, so change one at a time or the cause is lost.

## Limits and traps

- The assistant offers an averaged start; accepting it presses distinctive mixes into one shape.
- More modules and higher oversampling cost CPU and latency; a mastering session usually runs one version at a time.
- Reference matching depends on the genre and loudness of the reference, and a pop reference applied to chamber music yields the wrong low end.
- A heavily compressed reference yields less dynamics after matching; examine the result.
- Loudness targets differ by platform, so check the destination rather than pushing the maximiser to its ceiling.
- It cannot fix masking or phase; faults heard here usually belong to the multitrack.
- Plugin formats come from the installer, so check availability before changing DAW.

## Alternatives and pairings

Building your own chain means FabFilter Pro-Q plus Pro-L. For a more coloured master, look at Waves' classic limiters and equalisers. If you would rather not make the decisions, an automatic service such as LANDR is the other route. Ozone pairs with RX: repair the source first, then enter the mastering chain.

## First three things to learn

Learn gain staging and headroom, then the release and true-peak behaviour of the limiter, then how to use a reference. Read the site's pages on mastering, limiting and headroom alongside it.

```audiolab
{"type":"instrument","gm":"String Ensemble 1","synth":"bowed","phrase":["C3","G3","D4","A4","E4","C4"],"label":"一段弦乐，待做母带","label_en":"A string passage headed for mastering","hint":"先听渐强的顶，再想限幅器会把哪一段削平、宽度处理会不会让低频变薄","hint_en":"Hear the top of the crescendo first, then imagine where the limiter flattens it and whether width processing thins the low end"}
```
:::
